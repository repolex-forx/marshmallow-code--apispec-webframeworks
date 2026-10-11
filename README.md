# Repolex Knowledge Graph of marshmallow-code/apispec-webframeworks

RDF knowledge graph data for [marshmallow-code/apispec-webframeworks](https://github.com/marshmallow-code/apispec-webframeworks), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [rlex](https://github.com/repolex-ai/rlex) query tool:

```bash
cargo install --git https://github.com/repolex-ai/rlex
```

Verify the install:

```bash
rlex --help
```

**rlex is designed to be used primarily by LLMs in a terminal.** Start up your favorite AI assistant and ask it to use rlex. It handles the SPARQL — you just ask questions in plain English.

To load this repo's data:

```bash
rlex download marshmallow-code/apispec-webframeworks
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── b03f02fe2f0cbd4818cae47bcedd2abf8596ad9b
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── b03f02fe2f0cbd4818cae47bcedd2abf8596ad9b
│           └── chunk-001.nq.gz
├── blob
│   ├── 25ee994eda302e582e9054392e6b41caafaade23.nq.gz
│   ├── 39db2144253336d3f819d588d12e50d92b376b6f.nq.gz
│   ├── 3e1b911f357627b5ea5924ef06e247b61d5cb08d.nq.gz
│   ├── 45da63b20218d46cee2ce921c452519260b05959.nq.gz
│   ├── 4d5b97c2dfcab58f6d1307008a219fe4c47461e0.nq.gz
│   ├── 5334b892ad49f366b0c8950814b08e2163ac2ab9.nq.gz
│   ├── 671c1637726284425470c31579bc25005bed3ae2.nq.gz
│   ├── 6ab90133e75ea4d38eb56bf7c082466c140323aa.nq.gz
│   ├── 73521a175594823f2811b11573b248fa6610eafd.nq.gz
│   ├── 799fc04cc4e6cfa1fab3cbb02406852efcc2a1b5.nq.gz
│   ├── 880b058a76967f02bb2a79785561c2e3613ec207.nq.gz
│   ├── 894a44cc066a027465cd26d634948d56d13af9af.nq.gz
│   ├── a8270afd133b66a17ccb9da76f6badad13a53872.nq.gz
│   ├── add53521b67d58634efb5949dd67b770a241a430.nq.gz
│   ├── c3356d4095dfe49e88f0c6d4277a725f4f46dbce.nq.gz
│   ├── c90e5dca5f51889bcab5ee0acc95c6c78e0d4d19.nq.gz
│   ├── d5442b73c4d57b9a1fd828a94cbbc52976e72339.nq.gz
│   ├── da3410b9a63e8ca8313ed5503c774fc614c0eaeb.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── ec2333faebd0cac6e18700ddfff6c3c97e3f420a.nq.gz
│   ├── ee1465e8f880a8911abf21fcfa69c5a66da87364.nq.gz
│   └── f40ce91be5fa3ae6afbf5457462f0d87000e4f1b.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── b03f02fe2f0cbd4818cae47bcedd2abf8596ad9b.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 30 files
```

| Directory | What it contains |
|-----------|-----------------|
| `blob/` | Per-file AST graphs, content-addressed by git blob SHA. Each file in the source repo gets its own graph. |
| `aggregate/ast/` | Combined AST graph per parsed commit. Merges all blob graphs for a snapshot of the entire codebase at that point. |
| `aggregate/lsp/` | Language Server Protocol enrichment: resolved symbols, definitions, references, and type information. |
| `aggregate/dataflow/` | Interprocedural data flow edges between functions and modules. |
| `aggregate/repolex/` | Combined graph (AST + LSP + dataflow) per commit. |
| `commit/` | Git commit metadata (author, date, message, parent links). |
| `branch/` | Branch metadata. |
| `tag/` | Tag metadata. |
| `filetree/` | File tree snapshots per commit (which files existed and their blob SHAs). |
| `audit/` | Code architecture and graph audit reports per commit. |

## Source repository

[marshmallow-code/apispec-webframeworks](https://github.com/marshmallow-code/apispec-webframeworks)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
