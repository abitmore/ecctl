---
mapped_pages:
  - https://www.elastic.co/guide/en/ecctl/current/ecctl_user_key_show.html
applies_to:
  deployment:
    ess: all
    ece: all
---

# ecctl user key show [ecctl_user_key_show]

Shows the API key details for the specified user.

```
ecctl user key show --user=<user id> <key id> [flags]
```


## Options [_options_133]

```
  -h, --help          help for show
      --user string   user id for the specified action
```


## Options inherited from parent commands [_options_inherited_from_parent_commands_132]

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
      --region string         Elastic Cloud Hosted region
      --timeout duration      Timeout to use on all HTTP calls (default 30s)
      --trace                 Enables tracing saves the trace to trace-20060102150405
      --verbose               Enable verbose mode
      --verbose-credentials   When set, Authorization headers on the request/response trail will be displayed as plain text
      --verbose-file string   When set, the verbose request/response trail will be written to the defined file
```


## See also [_see_also_133]

* [ecctl user key](/reference/ecctl_user_key.md) - Manages the API keys of a platform user

