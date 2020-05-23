# DASHT-DOCSETS-REMOVE 1        2020-05-16                            2.4.0

## NAME

dasht-docsets-remove - removes installed [Dash] docsets

## SYNOPSIS

`dasht-docsets-remove` [*OPTION*...] [*NAME*...]

### Examples

`dasht-docsets-remove`
  Removes all installed [Dash] docsets.

`dasht-docsets-remove` sh
  Removes installed [Dash] docsets whose names contain "sh".

`dasht-docsets-remove` sh 'c$'
  Removes installed [Dash] docsets whose names contain "sh" or end in "c".

## DESCRIPTION

Removes installed [Dash] docsets whose names match the *NAME* regex(7)
patterns.  If no *NAME*s are given, all installed docsets are matched.
Unless forced, this operation prompts you to confirm it for every match.

## OPTIONS

`-f`, `--force`
  Forces the operation by overriding the interactive confirmation prompt.

## ENVIRONMENT

`DASHT_DOCSETS_DIR`
  Defines the filesystem location where your [Dash] docsets are installed.
  If undefined, its value is assumed to be `$XDG_DATA_HOME/dasht/docsets/`
  or, if `XDG_DATA_HOME` is undefined, `$HOME/.local/share/dasht/docsets/`.

## SEE ALSO

dasht-docsets-install(1), dasht-docsets-update(1), dasht-docsets(1), [Dash]

[Dash]: https://kapeli.com/dash

## AUTHOR

Written in 2016 by Suraj N. Kurapati <https://github.com/sunaku/dasht>
Distributed under the terms of the ISC license (refer to README file).