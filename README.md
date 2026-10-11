# Repolex Knowledge Graph of agronholm/aioredlock

RDF knowledge graph data for [agronholm/aioredlock](https://github.com/agronholm/aioredlock), parsed by [repolex](https://repolex.ai).

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
rlex download agronholm/aioredlock
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 258fbf7790a4e2da2efdb4527a414862471eeee2
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 258fbf7790a4e2da2efdb4527a414862471eeee2
│           └── chunk-001.nq.gz
├── blob
│   ├── 0b4553cdf7fb62143e1d0a11d1ad5dcc9a552066.nq.gz
│   ├── 1e8e4d5edefb579bcb50f79c4b86c4aa1789f36f.nq.gz
│   ├── 3b2a093c71ca6352387cbcb4f530aeac9844ff29.nq.gz
│   ├── 3cb3175bb66630204ca2e7faa8d4d298bd93198a.nq.gz
│   ├── 4f0d356bf7d8b2a27ea521304c1c7fd181901199.nq.gz
│   ├── 57822098c754e4e49a069f90760bf9055779b96f.nq.gz
│   ├── 690f2178419ea5d0e2f05e74488e69cdd698cc3b.nq.gz
│   ├── 71005aecfc52c8ddffc3897cfef997be57366443.nq.gz
│   ├── 75359de2d5559efc40b06051a24a577081880a32.nq.gz
│   ├── 76f6ba7ae03b9eae19a294992926b082e317b6c6.nq.gz
│   ├── 7bab6af0dd38eaefac0b8aec00424cc8014dba8e.nq.gz
│   ├── 8bfb95f7ef16198351be4fd233b98d0b30d2c2f3.nq.gz
│   ├── 95d6fdb8eb8dead00e7443309a28bb1915c283f3.nq.gz
│   ├── 97b4a9f1801d10ca25d5223e37fa465fde4d996b.nq.gz
│   ├── 9f8f29d747acef469e8f7086490c2afa7ac73790.nq.gz
│   ├── a5aadfed223cd0f62dd287e6bf22bb84af37b3ee.nq.gz
│   ├── b06a93deefd2000e1a61adcae3de98b73467d947.nq.gz
│   ├── c554ebad6b2306ebe40c427db5bbf0fe2e427961.nq.gz
│   ├── ce5833b8c12a37d81cb6061c07536a0b4ec411d4.nq.gz
│   ├── dbce810b47a9e029ce5d3d5f1de78a5120e9a781.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e90b12a9a442fe25bd6d24ce58b44487326c5671.nq.gz
│   └── eab3507c14e44847e33b7da941f9bf130b5120f4.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 258fbf7790a4e2da2efdb4527a414862471eeee2.nq.gz
└── tag
    └── tag.nq.gz

11 directories, 29 files
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

[agronholm/aioredlock](https://github.com/agronholm/aioredlock)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
