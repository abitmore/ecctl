---
mapped_pages:
  - https://www.elastic.co/guide/en/ecctl/current/ecctl_platform_allocator_vacate.html
applies_to:
  deployment:
    ece: all
---

# ecctl platform allocator vacate [ecctl_platform_allocator_vacate]

Moves all the resources from the specified allocator.

```
ecctl platform allocator vacate <allocator-id> [flags]
```


## Examples [_examples_9]

```
  ecctl platform allocator vacate i-05e245252362f7f1d
  # Move everything from multiple allocators
  ecctl platform allocator vacate i-05e245252362f7f1d i-2362f7f1d252362f7

  # filter by a resource kind
  ecctl platform allocator vacate -k kibana i-05e245252362f7f1d

  # Only move specific resource IDs
  ecctl platform allocator vacate -r f521dedb07194c478fbbc6624f3bbf8f -r f404eea372cc4ea5bd553d47a09705cd i-05e245252362f7f1d

  # Specify multiple allocator targets
  ecctl platform allocator vacate -t i-05e245252362f7f2d -t i-2362f7f1d252362f7 i-05e245252362f7f1d
  ecctl platform allocator vacate --target i-05e245252362f7f2d --target i-2362f7f1d252362f7 --kind kibana i-05e245252362f7f1d

  # Set the allocators to maintenance mode before vacating them
  ecctl platform allocator vacate --maintenance -t i-05e245252362f7f2d -t i-2362f7f1d252362f7 i-05e245252362f7f1d

  # Set the amount of maximum moves to happen at any time
  ecctl platform allocator vacate --concurrency 10 i-05e245252362f7f1d

  # Override the allocator health auto discovery
  ecctl platform allocator vacate --allocator-down=true i-05e245252362f7f1d

  # Override the skip_snapshot setting
  ecctl platform allocator vacate --skip-snapshot=true i-05e245252362f7f1d -r f521dedb07194c478fbbc6624f3bbf8f

  # Override the skip_data_migration setting
  ecctl platform allocator vacate --skip-data-migration=true i-05e245252362f7f1d -r f521dedb07194c478fbbc6624f3bbf8f

  # Skips tracking the vacate progress which will cause the command to return almost immediately.
  # Not recommended since it can lead to failed vacates without the operator knowing about them.
  ecctl platform allocator vacate --skip-tracking i-05e245252362f7f1d
```


## Options [_options_74]

```
      --allocator-down string        Disables the allocator health auto-discovery, setting the allocator-down to either [true|false]
      --concurrency uint             Maximum number of concurrent moves to perform at any time (default 8)
  -h, --help                         help for vacate
  -k, --kind string                  Kind of workload to vacate (elasticsearch|kibana|apm|appsearch|enterprise_search)
  -m, --maintenance                  Whether to set the allocator(s) in maintenance before performing the vacate
      --max-poll-retries int         Optional maximum plan tracking retries (default 2)
      --move-only                    Keeps the resource in its current -possibly broken- state and just does the bare minimum to move the requested instances across to another allocator. [true|false] (default true)
      --override-failsafe            If false (the default) then the plan will fail out if it believes the requested sequence of operations can result in data loss - this flag will override some of these restraints. [true|false]
      --poll-frequency duration      Optional polling frequency to check for plan change updates (default 10s)
  -r, --resource-id strings          Resource IDs to include in the vacate
      --skip-data-migration string   Skips the data-migration operation on the specified resource IDs. ONLY available when the resource IDs are specified and --move-only is true. [true|false]
      --skip-snapshot string         Skips the snapshot operation on the specified resource IDs. ONLY available when the resource IDs are specified. [true|false]
      --skip-tracking                Skips tracking the vacate progress causing the command to return after the move operation has been executed. Not recommended.
  -t, --target strings               Target allocator(s) on which to place the vacated workload
```


## Options inherited from parent commands [_options_inherited_from_parent_commands_73]

:::{include} _snippets/inherited-options.md
:::


## See also [_see_also_74]

* [ecctl platform allocator](/reference/ecctl_platform_allocator.md) - Manages allocators
