# Repolex Knowledge Graph of tiangolo/meinheld-gunicorn-flask-docker

RDF knowledge graph data for [tiangolo/meinheld-gunicorn-flask-docker](https://github.com/tiangolo/meinheld-gunicorn-flask-docker), parsed by [repolex](https://repolex.ai).

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
rlex download tiangolo/meinheld-gunicorn-flask-docker
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── e871de6864887a7b3efba026cc935880a00485cb
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── e871de6864887a7b3efba026cc935880a00485cb
│           └── chunk-001.nq.gz
├── blob
│   ├── 0045fb8182cf94a55db192aa3bc8c4c7e033da47.nq.gz
│   ├── 0b7d7848b6961a01390b355ed15dddc68d04934c.nq.gz
│   ├── 0ffc101a3f23548392499fe5104f3f8cf4d4e91b.nq.gz
│   ├── 1a96da73a0b5ee6ee73b9d84f555498fa633d3aa.nq.gz
│   ├── 389644ea3f9aa447c6105c958ee16f8a2da88d63.nq.gz
│   ├── 451e2c78b1989e169d6db1c5059cce967edaa032.nq.gz
│   ├── 4664343f9e231937e757d08f5228268f68fe4f23.nq.gz
│   ├── 4721375b0e37c8b0da1b19f0d8135dd59e828976.nq.gz
│   ├── 55eec6eb458d17b0a36c90625488d8fafbda90d5.nq.gz
│   ├── 73a4f8524ec9138a81c49ea8bcc29625af3d7625.nq.gz
│   ├── 9a38cf98d021122897504c6a806f5763b8e1c3f2.nq.gz
│   ├── a9d3710fbd980462a221073a683b204ad5450c58.nq.gz
│   ├── af6abf466199d728b7d86a70aa2c9c94686ada74.nq.gz
│   ├── b29b20b8ede069e9aa4c745be63163e32c82cecf.nq.gz
│   ├── cd972a0ba47221bf96acedfaed8f3b5cba819849.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── eb12624efae364c574d3862da30a4a526c0d56e8.nq.gz
│   ├── f4b293369f3cf8cd1bcac1fdf6fa25ed5b23e216.nq.gz
│   └── feec529f1e6a2c68172ce4c39dca6419764cdbfa.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── e871de6864887a7b3efba026cc935880a00485cb.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 27 files
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

[tiangolo/meinheld-gunicorn-flask-docker](https://github.com/tiangolo/meinheld-gunicorn-flask-docker)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
