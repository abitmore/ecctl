---
mapped_pages:
  - https://www.elastic.co/guide/en/ecctl/current/ecctl_user_update.html
---

# ecctl user update [ecctl_user_update]

Updates a platform user ![logo cloud ece](https://doc-icons.s3.us-east-2.amazonaws.com/logo_cloud_ece.svg "Supported on {{ece}}") (Available for ECE only)

```
ecctl user update <username> --role <role> [flags]
```


## Examples [_examples_14]

```
  * Update a platform user
	ecctl user update --username xochitl --role ece_platform_viewer --email xo@example.com

  * Update the current platform user
    ecctl user update --current --email xo@example.com --password
```


## Options [_options_136]

```
      --current                    updates details of the current user
      --email string               user's email address (must be in a valid email format)
      --fullname string            user's full name
  -h, --help                       help for update
      --insecure-password string   [INSECURE] user plaintext password
      --password                   if set, updates the user's password securely
                                   (must use a minimum of 8 characters )
      --role strings               role or roles assigned to the user. Available roles:
                                   ece_platform_admin, ece_platform_viewer, ece_deployment_manager, ece_deployment_viewer
```


## Options inherited from parent commands [_options_inherited_from_parent_commands_135]

```
      --api-key string        API key to use to authenticate (If empty will look for EC_API_KEY environment variable)
      --config string         Config name, used to have multiple configs in $HOME/.ecctl/<env> (default "config")
      --force                 Do not ask for confirmation
      --format string         Formats the output using a Go template
      --host string           Base URL to use
      --insecure              Skips all TLS validation
      --message string        A message to set on cluster operation
      --output string         Output format [text|json] (default "text")
      --pass string           Password to use to authenticate (If empty will look for EC_PASS environment variable)
      --pprof                 Enables pprofing and saves the profile to pprof-20060102150405
  -q, --quiet                 Suppresses the configuration file used for the run, if any
      --region string         Elasticsearch Service region
      --timeout duration      Timeout to use on all HTTP calls (default 30s)
      --trace                 Enables tracing saves the trace to trace-20060102150405
      --user string           Username to use to authenticate (If empty will look for EC_USER environment variable)
      --verbose               Enable verbose mode
      --verbose-credentials   When set, Authorization headers on the request/response trail will be displayed as plain text
      --verbose-file string   When set, the verbose request/response trail will be written to the defined file
```


## SEE ALSO [_see_also_136]

* [ecctl user](/reference/ecctl_user.md)	 - Manages the platform users ![logo cloud ece](https://doc-icons.s3.us-east-2.amazonaws.com/logo_cloud_ece.svg "Supported on {{ece}}") (Available for ECE only)

