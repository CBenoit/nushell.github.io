---
title: mkdir
categories: |
  filesystem
version: 0.86.0
filesystem: |
  Make directories, creates intermediary directories as required.
usage: |
  Make directories, creates intermediary directories as required.
---
<!-- This file is automatically generated. Please edit the command in https://github.com/nushell/nushell instead. -->

# <code>{{ $frontmatter.title }}</code> for filesystem

<div class='command-title'>{{ $frontmatter.filesystem }}</div>

## Signature

```> mkdir {flags} ...rest```

## Flags

 -  `--verbose, -v`: print created path(s).

## Parameters

 -  `...rest`: the name(s) of the path(s) to create


## Input/output types:

| input   | output  |
| ------- | ------- |
| nothing | nothing |

## Examples

Make a directory named foo
```nu
> mkdir foo

```

Make multiple directories and show the paths created
```nu
> mkdir -v foo/bar foo2

```
