---
mapped_pages:
  - https://www.elastic.co/guide/en/ecctl/current/ecctl_deployment_show.html
---

# ecctl deployment show [ecctl_deployment_show]

Shows the specified deployment resources

```
ecctl deployment show <deployment-id> [flags]
```


## Examples [_examples_6]

```
* Shows kibana resource information from a given deployment:
  ecctl deployment show <deployment-id> --kind kibana

* Shows apm resource information from a given deployment with a specified ref-id.
  ecctl deployment show <deployment-id> --kind apm --ref-id apm-server

* Return the current deployment state as a valid update payload.
  ecctl deployment show <deployment id> --generate-update-payload > update.json
```


## Options [_options_42]

```
      --clear-transient           Removes the transient field in order to make read - edit - write loop safer. The default value of clear-transient depends on the value of generate-update-payload. If generate-update-payload is true then clear-transient defaults to true. Otherwise defaults to false.
      --generate-update-payload   Outputs JSON which can be used as an argument for the --file flag with the update command.
  -h, --help                      help for show
      --kind string               Optional deployment resource kind (apm, appsearch, kibana, elasticsearch)
  -m, --metadata                  Shows the deployment metadata
      --plan-defaults             Shows the deployment plan defaults
      --plan-history              Shows the deployment plan history
      --plan-logs                 Shows the deployment plan logs
      --plans                     Shows the deployment plans
      --ref-id string             Optional deployment kind RefId, if not set, the RefId will be auto-discovered
  -s, --settings                  Shows the deployment settings
```


## Options inherited from parent commands [_options_inherited_from_parent_commands_41]

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


## SEE ALSO [_see_also_42]

* [ecctl deployment](/reference/ecctl_deployment.md)	 - Manages deployments

