# DASHT-QUERY-HTML 1            2020-05-16                            2.4.0

## NAME

dasht-query-html - searches [Dash] docsets and emits HTML table rows

## SYNOPSIS

`dasht-query-html` [*PATTERN*] [*DOCSET*]...

### Examples

`dasht-query-html`
  Topics (A-Z) from each installed docset.

`dasht-query-html` 'c - x'
  Search for "c - x" in all installed docsets.

`dasht-query-html` 'c - x' bash
  Search for "c - x" only in the "bash" docset.

`dasht-query-html` 'c - x' bash css
  Search for "c - x" only in the "bash" and "css" docsets.

## DESCRIPTION

Searches for *PATTERN* in all installed [Dash] docsets, optionally searching
only in those whose names match *DOCSET*s, by calling dasht-query-line(1).
The results are then printed, one per line, to stdout as HTML table rows.
However, if no results were found, this program exits with a nonzero status.

### Searching

Whitespace characters in *PATTERN* are treated as wildcards, whereas the
SQL LIKE wildcard characters `%` and `_` are not: they are taken literally.

Before searching, *PATTERN* is surrounded by whitespace wildcards so that it
can match anywhere: beginning, middle, or end.  As a result, if *PATTERN* is
undefined, it becomes a whitespace wildcard and thereby matches everything.

## ENVIRONMENT

`DASHT_DOCSETS_DIR`
  Defines the filesystem location where your [Dash] docsets are installed.
  If undefined, its value is assumed to be `$XDG_DATA_HOME/dasht/docsets/`
  or, if `XDG_DATA_HOME` is undefined, `$HOME/.local/share/dasht/docsets/`.

## EXIT STATUS

44
  No results were found.

## SEE ALSO

dasht-query-line(1), dasht-docsets(1), dasht(1), [Dash]

[Dash]: https://kapeli.com/dash

## AUTHOR

Written in 2016 by Suraj N. Kurapati <https://github.com/sunaku/dasht>
Distributed under the terms of the ISC license (see the LICENSE file).