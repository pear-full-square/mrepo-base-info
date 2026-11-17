# get

Answers a page of the mrepo's info by its keywords, with the keywords below it.

## Signature

`get(exec, { args })`: requested as `info/get [<keywords>]`, at the
mrepo itself.

## Arguments

- `keywords`: a path from the top, `boot/deploy`, or its words,
  `boot deploy`; none: the top.

## Returns

`{ keyword, choices }`: each choice a page the keyword reaches, `{
title, oneliner, page, below, see?, generated? }`: its text without its
menus (a section: its text), and each keyword below it, `{ keyword,
oneliner, choices }`.

## Errors

- No info extracted yet.
- A keyword that is not there: the nearest one above it, and what is
  below that.
