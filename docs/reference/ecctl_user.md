---
mapped_pages:
  - https://www.elastic.co/guide/en/ecctl/current/ecctl_user.html
---

# ecctl user [ecctl_user]

Manages the platform users ![logo cloud ece](https://doc-icons.s3.us-east-2.amazonaws.com/logo_cloud_ece.svg "Supported on {{ece}}") (Available for ECE only)

```
ecctl user [flags]
```


## Options [_options_125]

```
  -h, --help   help for user
```


## Options inherited from parent commands [_options_inherited_from_parent_commands_124]

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


## SEE ALSO [_see_also_125]

* [ecctl](/reference/ecctl.md)	 - Elastic Cloud Control
* [ecctl user create](/reference/ecctl_user_create.md)	 - Creates a new platform user ![logo cloud ece](https://doc-icons.s3.us-east-2.amazonaws.com/logo_cloud_ece.svg "Supported on {{ece}}") (Available for ECE only)
* [ecctl user delete](/reference/ecctl_user_delete.md)	 - Deletes one or more platform users ![logo cloud ece](https://doc-icons.s3.us-east-2.amazonaws.com/logo_cloud_ece.svg "Supported on {{ece}}") (Available for ECE only)
* [ecctl user disable](/reference/ecctl_user_disable.md)	 - Disables a platform user ![logo cloud ece](https://doc-icons.s3.us-east-2.amazonaws.com/logo_cloud_ece.svg "Supported on {{ece}}") (Available for ECE only)
* [ecctl user enable](/reference/ecctl_user_enable.md)	 - Enables a previously disabled platform user ![logo cloud ece](https://doc-icons.s3.us-east-2.amazonaws.com/logo_cloud_ece.svg "Supported on {{ece}}") (Available for ECE only)
* [ecctl user key](/reference/ecctl_user_key.md)	 - Manages the API keys of a platform user
* [ecctl user list](/reference/ecctl_user_list.md)	 - Lists all platform users ![logo cloud ece](https://doc-icons.s3.us-east-2.amazonaws.com/logo_cloud_ece.svg "Supported on {{ece}}") (Available for ECE only)
* [ecctl user show](/reference/ecctl_user_show.md)	 - Shows details of a specified user ![logo cloud ece](https://doc-icons.s3.us-east-2.amazonaws.com/logo_cloud_ece.svg "Supported on {{ece}}") (Available for ECE only)
* [ecctl user update](/reference/ecctl_user_update.md)	 - Updates a platform user ![logo cloud ece](https://doc-icons.s3.us-east-2.amazonaws.com/logo_cloud_ece.svg "Supported on {{ece}}") (Available for ECE only)

