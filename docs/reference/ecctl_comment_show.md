---
mapped_pages:
  - https://www.elastic.co/guide/en/ecctl/current/ecctl_comment_show.html
applies_to:
  deployment:
    ece: all
---

# ecctl comment show [ecctl_comment_show]

Shows information about a resource comment.

```
ecctl comment show <comment id> --resource-type <resource-type> --resource-id <resource-id> [flags]
```


## Options [_options_12]

```
  -h, --help                   help for show
      --resource-id string     ID of the resource that the comment belongs to.
      --resource-type string   The kind of resource that a comment belongs to. Should be one of [elasticsearch, kibana, apm, appsearch, enterprise_search, allocator, constructor, runner, proxy].
```


## Options inherited from parent commands [_options_inherited_from_parent_commands_11]

:::{include} _snippets/inherited-options.md
:::


## See also [_see_also_12]

* [ecctl comment](/reference/ecctl_comment.md)	 - Manages resource comments
