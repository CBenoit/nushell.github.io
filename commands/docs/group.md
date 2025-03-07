---
title: group
categories: |
  filters
version: 0.86.0
filters: |
  Groups input into groups of `group_size`.
usage: |
  Groups input into groups of `group_size`.
---
<!-- This file is automatically generated. Please edit the command in https://github.com/nushell/nushell instead. -->

# <code>{{ $frontmatter.title }}</code> for filters

<div class='command-title'>{{ $frontmatter.filters }}</div>

## Signature

```> group {flags} (group_size)```

## Parameters

 -  `group_size`: the size of each group


## Input/output types:

| input     | output          |
| --------- | --------------- |
| list\<any\> | list\<list\<any\>\> |

## Examples

Group the a list by pairs
```nu
> [1 2 3 4] | group 2
╭───┬───────────╮
│ 0 │ ╭───┬───╮ │
│   │ │ 0 │ 1 │ │
│   │ │ 1 │ 2 │ │
│   │ ╰───┴───╯ │
│ 1 │ ╭───┬───╮ │
│   │ │ 0 │ 3 │ │
│   │ │ 1 │ 4 │ │
│   │ ╰───┴───╯ │
╰───┴───────────╯

```
