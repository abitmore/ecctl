# Releasing a new version

This guide aims to provide guidance on how to release new versions of the `ecctl` binary as well as updating all the necessary parts to make it successful. The release will happen automatically via GitHub actions, but there are a few prerequisites to tick before that can be started.

- [Releasing a new version](#releasing-a-new-version)
  - [Prerequisites](#prerequisites)
    - [Verify a release in `cloud-sdk-go` has been made](#verify-a-release-in-cloud-sdk-go-has-been-made)
    - [Make sure the version has been updated](#make-sure-the-version-has-been-updated)
    - [Generating a changelog for the new version](#generating-a-changelog-for-the-new-version)
  - [Executing the release](#executing-the-release)
  - [Post release requirements](#post-release-requirements)
    - [Approve the updated `homebrew-tap` formula.](#approve-the-updated-homebrew-tap-formula)
    - [Create documentation specific to the release (Minor and Major only)](#create-documentation-specific-to-the-release-minor-and-major-only)
    - [Update downloads website](#update-downloads-website)

## Prerequisites

Before starting any release, make sure to open a release checklist [issue](https://github.com/elastic/ecctl/issues/403) using the provided release [template](https://github.com/elastic/ecctl/issues/new?assignees=&labels=Team%3ADelivery&template=RELEASE_CHECKLIST.md).

Releasing a new version of the binary implies that there have been changes in the source code which are meant to be released for wider consumption. Before releasing a new version there's some prerequisites that have to be checked.

### Update `cloud-sdk-go` if applicable

If applicable, update the `cloud-sdk-go` dependency in `go.mod`. In the past the cloud-sdk-go version was tied to the ecctl version. This is no longer the case as the two are released independently.

### Make sure the version has been updated

**Since the version updates are now automated via github actions, this is just a double check**

Since the source has changed, we need to update the current committed version to a higher version so that the release is published.

The version is currently defined in the [Makefile](./Makefile) as an exported environment variable called `VERSION` in the [SEMVER](https://semver.org) format: `MAJOR.MINOR.PATCH`

```Makefile
SHELL := /bin/bash
export VERSION ?= v1.0.0
```

Say we want to perform a minor version release (i.e. no breaking changes and only new features and bug fixes are being included); in which case we'll update the _MINOR_ part of the version, this can be done with the `make minor` target, but it should have been updated automatically via GitHub actions.

```Makefile
SHELL := /bin/bash
export VERSION ?= v1.1.0
```

If a patch version needs to be released, the release will be done from the minor branch. For example, if we want to release `v1.5.1`, we will check out the `1.5` branch and perform any changes in that branch. The VERSION variable in the Makefile should already be up to date, but in case it's not, it can be bumped with the `make patch` target.

### Generating a changelog for the new version

Steps 
* Add a new changelog entry to docs/release-notes/index.md (this powers the release notes [docs page](https://www.elastic.co/docs/release-notes/ecctl)) See prior release within file as an example.
* Run `make changelog` to create a new file in `notes/*.md` (supports the [release notes](https://github.com/elastic/ecctl/releases) within the github repo)

After the release notes have been manually curated, a new pull request can be opened with the changelog and release notes.

## Executing the release

After the new changelog and version have been merged to master, the only thing remaining is to run `make tag`. This is the makefile target which will push the GitHub tag and will trigger the corresponding [GitHub action](.github/workflows/release.yml) which will release ecctl.

## Post release requirements

After a release has been performed there are still a few things we need to do.

### Approve the updated `homebrew-tap` formula.

The release process will open a pull request against the [`homebrew-tap`](https://github.com/elastic/homebrew-tap/pulls) repository, which needs to be approved and merged, see <https://github.com/elastic/homebrew-tap/pull/98> as an example.

### Create documentation specific to the release (Minor and Major only)

Previously this required special action to trigger a full docs rebuild. Currently after PR has been merged documentation should be automatically updated within ~30 minutes.

### Update downloads website

Once the release is done and the documentation is live, you'll need to get in touch with the marketing team to update the [downloads website](https://www.elastic.co/downloads/ecctl) with the correct links and information.

To do this you'll need to open up an issue similar to [this](https://github.com/elastic/website-www.elastic.co/issues/7163) one. In that issue you'll see a link to a google doc, do **NOT** directly edit this doc, but rather add as suggestions the changes to the links and information. The marketing team is pretty quick to answer, but should they miss this issue for some reason you can ping them in the #marketing channel.

There is an open [issue](https://github.com/elastic/ecctl/issues/428) to automate this process, but we've not had the bandwidth to dedicate time to work on this.
