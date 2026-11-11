# Nebula-YW fork of graphviz-rust

Branch `nebula` = upstream `0.9.9` (`42ccd454`) plus DOT parsing fixes used by
Nebula-YW/automotive-platform until they are released upstream.

- `src/grammar/dot.pest`: UTF-8 IDs, DOT numerals, quoted ID concatenation,
  nested HTML IDs, case-insensitive keyword boundaries, compass points on any ID,
  anonymous subgraphs and subgraphs as edge endpoints.
- `src/parser.rs`: concatenated quoted parts, backslash-newline continuation,
  subgraph keyword token and quoted compass handling.
- `src/printer.rs`: keep `;` between inline statements.

Reference: <https://graphviz.org/doc/info/lang.html>. Run the library tests with
`cargo test --no-default-features --lib`; the crate doctest needs `graphviz-exec`.
Delete this branch once an upstream release contains the fixes.
