---
mapped_pages:
  - https://www.elastic.co/guide/en/ecctl/current/ecctl_deployment_traffic-filter_association_create.html
---

# ecctl deployment traffic-filter association create [ecctl_deployment_traffic-filter_association_create]

Applies the ruleset to the specified deployment.

```
ecctl deployment traffic-filter association create <ruleset id> --deployment-id <deployment-id> [flags]
```


## Options [_options_52]

```
      --deployment-id string   Required deployment ID where the traffic filter will be associated
  -h, --help                   help for create
```


## Options inherited from parent commands [_options_inherited_from_parent_commands_51]

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


## SEE ALSO [_see_also_52]

* [ecctl deployment traffic-filter association](/reference/ecctl_deployment_traffic-filter_association.md)	 - Manages traffic filter ruleset associations

