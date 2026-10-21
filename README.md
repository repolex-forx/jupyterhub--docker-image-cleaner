# Repolex Knowledge Graph of jupyterhub/docker-image-cleaner

RDF knowledge graph data for [jupyterhub/docker-image-cleaner](https://github.com/jupyterhub/docker-image-cleaner), parsed by [repolex](https://repolex.ai).

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
rlex download jupyterhub/docker-image-cleaner
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── b305d4fd0fd20c0ea38b2fbb6f93c83d3faaed19
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── b305d4fd0fd20c0ea38b2fbb6f93c83d3faaed19
│           └── chunk-001.nq.gz
├── blob
│   ├── 022bc12f0e70a6267515caab940ad220dd902196.nq.gz
│   ├── 112384716893c94c2cd47ccc84d6d22d7ddbdf51.nq.gz
│   ├── 14fd90183e0dc6306acbc4643839343867e6ece9.nq.gz
│   ├── 166af91e07437f80b5e5a45183d0d9cf807349f8.nq.gz
│   ├── 31293bb81f3e3377049b5bebc7c6ae117d997caf.nq.gz
│   ├── 3a01234989a8bfdbce46200a7fdf9e40b56e1cf5.nq.gz
│   ├── 582391ebeb30478f5124f89e64ec810e30fdeb47.nq.gz
│   ├── 5d539474bd6aafd67601d9845c70269fa60cb040.nq.gz
│   ├── 6bfc7d7a598dfb518999eddccec6cf4353d4b2f8.nq.gz
│   ├── 80121ee4b98ec77ad96c794184738baa17ae9c95.nq.gz
│   ├── 850b06229ac30ccbd1c1ea2e96bb7462d4dc7dbb.nq.gz
│   ├── 94dbd57b34ac8fa4b7ddb89d9c21380e968024c7.nq.gz
│   ├── a0e1e05e178775f0a3e8a8d81534c62b8cbf2340.nq.gz
│   ├── a77889c8b93ec4d0ebb73c64619e64ccd95d6c04.nq.gz
│   ├── b369eff202f37816c893908451d946f510e83fa2.nq.gz
│   ├── d42a32aed056b167ec4ff4ea51c2dea09882e7cc.nq.gz
│   ├── d5175cd8ee9dda262431edb59f80affda8edbe11.nq.gz
│   ├── e14168a24d4a0e86f82716ea7c60d07fe1fbdeae.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e834ca9d28a8df732751579823b3612e22dde650.nq.gz
│   └── e88d46af7d6a4df9c83f24532b2dc891d3e254a9.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── b305d4fd0fd20c0ea38b2fbb6f93c83d3faaed19.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 29 files
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

[jupyterhub/docker-image-cleaner](https://github.com/jupyterhub/docker-image-cleaner)

---
*Parsed on 2026-10-21 by [repolex](https://repolex.ai)*
