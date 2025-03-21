---
mapped_pages:
  - https://www.elastic.co/guide/en/ecctl/current/ecctl_deployment_resource_shutdown.html
---

# ecctl deployment resource shutdown [ecctl_deployment_resource_shutdown]

Shuts down a deployment resource by its kind and ref-id


## Synopsis [_synopsis_3]

Shuts down a deployment resource kind (APM, Appsearch, Elasticsearch, Kibana). Shutting down a kind doesn’t necessarily shut down the deployment itself but rather a specific  resource.

```
ecctl deployment resource shutdown <deployment id> --kind <kind> --ref-id <ref-id> [flags]
```


## Options [_options_33]

```
  -h, --help            help for shutdown
      --hide            Optionally hides the deployment resource from being listed by default
      --kind string     Required deployment resource kind (apm, appsearch, kibana, elasticsearch)
      --ref-id string   Optional deployment RefId, auto-discovered if not specified
      --skip-snapshot   Optional flag to toggle skipping the resource snapshot before shutting it down
```


## Options inherited from parent commands [_options_inherited_from_parent_commands_32]

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


## SEE ALSO [_see_also_33]

* [ecctl deployment resource](/reference/ecctl_deployment_resource.md)	 - Manages deployment resources

