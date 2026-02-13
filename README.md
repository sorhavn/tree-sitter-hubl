# tree-sitter-hubl

A [tree-sitter](https://tree-sitter.github.io/) grammar for **HubL**, the HubSpot templating language.

## Supported Syntax

- **Expressions** — `{{ variable }}`, `{{ obj.attr|filter }}`
- **Statements** — `{% if condition %}`, `{% for item in list %}`, `{% endif %}`
- **Comments** — `{# comment #}`
- **Whitespace trimming** — `{{- expr -}}`, `{%- stmt -%}`, `{#- comment -#}`
- Strings, numbers, booleans, `none`/`null`, operators, filters, and dot-attribute access

## Requirements

- [tree-sitter CLI](https://tree-sitter.github.io/tree-sitter/creating-parsers/tool-overview.html) v0.24+

## Usage

Generate the parser:

```sh
tree-sitter generate
```

Parse a HubL file:

```sh
tree-sitter parse example.hubl
```

Run tests (requires a `test/corpus/` directory):

```sh
tree-sitter test
```

## Project Structure

```
grammar.js          — grammar definition
tree-sitter.json    — tree-sitter metadata & bindings config
src/                — generated parser (parser.c, grammar.json, node-types.json)
```
