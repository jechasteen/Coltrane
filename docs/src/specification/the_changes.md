# The Changes

This section is where the Coltrane language itself is used.
The changes is line break delimited, each line constitutes a **statement**.
These statements can be measures, control flow, or comments

It is required that there be no more than one *measure* statement per line, but there can be any number of *chord* expressions within that line.

These statements can either be control flow or measures.

## Statement vs Expression

Just as in programming languages, Coltrane makes a distinction between a statement and an expression.
Simply put, an statement is composed of an expression or multiple expressions.

A control flow expression is statement composed of exactly 1 expression.
Many chord expressions can be combined in a single line to form 1 measure statement.

The distinction is not important for Coltrane composers, but it bears mentioning because of the importance of the line break.
For the composer, it suffices to understand the importance of statements each being on their own line.

## Comments

Coltrane supports single line comments marked by a `$` at the beginning of the line.
Anything after the `$` is disregarded by the parser.
A comment can be used in any part of the source file, not just in `[changes]`.

```
[changes]
$ introduction: bass line
1:bVII7
1:vi
```