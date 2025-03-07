---
title: split-by
categories: |
  filters
version: 0.86.0
filters: |
  Create a new table split.
usage: |
  Create a new table split.
---
<!-- This file is automatically generated. Please edit the command in https://github.com/nushell/nushell instead. -->

# <code>{{ $frontmatter.title }}</code> for filters

<div class='command-title'>{{ $frontmatter.filters }}</div>

## Signature

```> split-by {flags} (splitter)```

## Parameters

 -  `splitter`: the splitter value to use


## Input/output types:

| input  | output |
| ------ | ------ |
| record | record |

## Examples

split items by column named "lang"
```nu
> {
        '2019': [
          { name: 'andres', lang: 'rb', year: '2019' },
          { name: 'jt', lang: 'rs', year: '2019' }
        ],
        '2021': [
          { name: 'storm', lang: 'rs', 'year': '2021' }
        ]
    } | split-by lang
╭────┬─────────────────────────────────────────╮
│    │ ╭──────┬──────────────────────────────╮ │
│ rb │ │      │ ╭───┬────────┬──────┬──────╮ │ │
│    │ │ 2019 │ │ # │  name  │ lang │ year │ │ │
│    │ │      │ ├───┼────────┼──────┼──────┤ │ │
│    │ │      │ │ 0 │ andres │ rb   │ 2019 │ │ │
│    │ │      │ ╰───┴────────┴──────┴──────╯ │ │
│    │ ╰──────┴──────────────────────────────╯ │
│    │ ╭──────┬─────────────────────────────╮  │
│ rs │ │      │ ╭───┬──────┬──────┬──────╮  │  │
│    │ │ 2019 │ │ # │ name │ lang │ year │  │  │
│    │ │      │ ├───┼──────┼──────┼──────┤  │  │
│    │ │      │ │ 0 │ jt   │ rs   │ 2019 │  │  │
│    │ │      │ ╰───┴──────┴──────┴──────╯  │  │
│    │ │      │ ╭───┬───────┬──────┬──────╮ │  │
│    │ │ 2021 │ │ # │ name  │ lang │ year │ │  │
│    │ │      │ ├───┼───────┼──────┼──────┤ │  │
│    │ │      │ │ 0 │ storm │ rs   │ 2021 │ │  │
│    │ │      │ ╰───┴───────┴──────┴──────╯ │  │
│    │ ╰──────┴─────────────────────────────╯  │
╰────┴─────────────────────────────────────────╯
```
