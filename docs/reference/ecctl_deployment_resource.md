---
mapped_pages:
  - https://www.elastic.co/guide/en/ecctl/current/ecctl_deployment_resource.html
---

# ecctl deployment resource [ecctl_deployment_resource]

Manages deployment resources

```
ecctl deployment resource [flags]
```


## Options [_options_30]

```
  -h, --help   help for resource
```


## Options inherited from parent commands [_options_inherited_from_parent_commands_29]

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


## SEE ALSO [_see_also_30]

* [ecctl deployment](/reference/ecctl_deployment.md)	 - Manages deployments
* [ecctl deployment resource delete](/reference/ecctl_deployment_resource_delete.md)	 - Deletes a previously shut down deployment resource
* [ecctl deployment resource restore](/reference/ecctl_deployment_resource_restore.md)	 - Restores a previously shut down deployment resource
* [ecctl deployment resource shutdown](/reference/ecctl_deployment_resource_shutdown.md)	 - Shuts down a deployment resource by its kind and ref-id
* [ecctl deployment resource start](/reference/ecctl_deployment_resource_start.md)	 - Starts a previously stopped deployment resource
* [ecctl deployment resource start-maintenance](/reference/ecctl_deployment_resource_start-maintenance.md)	 - Starts maintenance mode on a deployment resource
* [ecctl deployment resource stop](/reference/ecctl_deployment_resource_stop.md)	 - Stops a deployment resource
* [ecctl deployment resource stop-maintenance](/reference/ecctl_deployment_resource_stop-maintenance.md)	 - Stops maintenance mode on a deployment resource
* [ecctl deployment resource upgrade](/reference/ecctl_deployment_resource_upgrade.md)	 - Upgrades a deployment resource

