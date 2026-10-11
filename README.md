# Repolex Knowledge Graph of pallets-eco/flask-social

RDF knowledge graph data for [pallets-eco/flask-social](https://github.com/pallets-eco/flask-social), parsed by [repolex](https://repolex.ai).

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
rlex download pallets-eco/flask-social
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 36f5790c8fb6d4d9a5120d099419ba30fd73e897
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 36f5790c8fb6d4d9a5120d099419ba30fd73e897
│           └── chunk-001.nq.gz
├── blob
│   ├── 0bafeda307ac5af27d651c415d2f91a22efc0a87.nq.gz
│   ├── 136ecce57383eebf730bc34461b45f80f9616bd5.nq.gz
│   ├── 1a2116fb04f3c46be6f9f198c0ebc75d200f43c2.nq.gz
│   ├── 1aafcc6f9d9a78bef6d88180b774fedbe8b8ff62.nq.gz
│   ├── 1d1332185b29ae5c3a558924c0ac0a68fe713d9b.nq.gz
│   ├── 235c7174f021fd341fbdfa96cdcdb1daa3c51fe7.nq.gz
│   ├── 2a0d1594dd9913d7841467f17ebc0d5cc897e29a.nq.gz
│   ├── 2b1a4f0b9c203602ddb36d0d6ba3939d49e86e11.nq.gz
│   ├── 2bbaa4e09a4cb136b1b2f85cd3b6d32ff4f7b561.nq.gz
│   ├── 3266f52cc2fd821c9752c4695b4744095f9f557f.nq.gz
│   ├── 3f4ce4fa14ba214a436db9ce8e0a561c96c80dcb.nq.gz
│   ├── 4657401b5f751409e01c5772d9485f940a32f3d4.nq.gz
│   ├── 474366cc7ca6e3ab57830a9ae557aa3d42d4a837.nq.gz
│   ├── 47fc7410aa9616a311f3456f72f2b783b3cc3bbf.nq.gz
│   ├── 57a4f7326a960f198360ece30ddd7f08977369f5.nq.gz
│   ├── 5b6f3d8dc28a14e4b542a5154c9ee1a537893acc.nq.gz
│   ├── 6eaab61760afff097aadd773deaf48ed4b5515ae.nq.gz
│   ├── 736bfed3854da0e0d86488103811404b7c0b08ab.nq.gz
│   ├── 7528f7f8d400d462448bd63588cc2639079b6079.nq.gz
│   ├── 7aeac3e698d6cd41aef6d14d3c414e067c6a85bc.nq.gz
│   ├── 7e7523168049d768ea399dca3e606d48a0ec49e3.nq.gz
│   ├── 88cac7a2cc7c6c5a547100f6ee64375ccbb8a114.nq.gz
│   ├── 8a05a51e8698babbed33230457f17c9073042d81.nq.gz
│   ├── 94d2c750597394905af3d82fa6906e3928e0eb32.nq.gz
│   ├── 9cfe388a21bde4c3901005b2f132a246148dc21d.nq.gz
│   ├── 9de208ac1aff47910cf3e634936a09435b183bf8.nq.gz
│   ├── b8e085d29e031820e61a5fc2b4d526608802992f.nq.gz
│   ├── bf7b494fc7044e1395c1c821f2babc309277bf78.nq.gz
│   ├── cfa64f9abfd9a06c9fd10e3ab27e17a384c20822.nq.gz
│   ├── d47d8eec5baf3ffc9b56d66b4845b08b2ee4a2f3.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── eb46254900186a2e2c6d505f14146d4b5bafb5d2.nq.gz
│   ├── f3400fa66a2aa0f972f1b400fdfdd3d5fcee083a.nq.gz
│   └── fd37021689b47fac258d42dce5738976e47300e2.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 36f5790c8fb6d4d9a5120d099419ba30fd73e897.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 42 files
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

[pallets-eco/flask-social](https://github.com/pallets-eco/flask-social)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
