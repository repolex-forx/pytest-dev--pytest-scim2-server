# Repolex Knowledge Graph of pytest-dev/pytest-scim2-server

RDF knowledge graph data for [pytest-dev/pytest-scim2-server](https://github.com/pytest-dev/pytest-scim2-server), parsed by [repolex](https://repolex.ai).

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
rlex download pytest-dev/pytest-scim2-server
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 0aad249a5609bbeab4c30f42b9709e3b35345c3b
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 0aad249a5609bbeab4c30f42b9709e3b35345c3b
│           └── chunk-001.nq.gz
├── blob
│   ├── 15201acc113da01edf6fa2fb2708b2e9076b6bc5.nq.gz
│   ├── 24ee5b1be9961e38a503c8e764b7385dbb6ba124.nq.gz
│   ├── 2d83771d2f8ed3b479b708ed7a52039581048feb.nq.gz
│   ├── 390ae0d44349f19f1eecd6570ffdb61e438fd39f.nq.gz
│   ├── 39d721e79baf67be9dac0b76ff0ce96b7f26132e.nq.gz
│   ├── 498f590baa9b39779fb667e209ac2121f124e386.nq.gz
│   ├── 57a758b72d5ca49f7f6975a9500356a94d458def.nq.gz
│   ├── 584651d28e9a542f6db823810ae1ec188f986634.nq.gz
│   ├── 71fbeb3a882b3317aede3538815c51ca91647243.nq.gz
│   ├── a40e9a1e02226009014dc95c89f9c9455d866d57.nq.gz
│   ├── c6481d5f740462ec9fd3edcb32aa56806e316c77.nq.gz
│   ├── c725d1e338031214b52dcb1220f76e32519adf65.nq.gz
│   ├── c83bf0d75e5b65157a802c12ca68f654a9351194.nq.gz
│   ├── cf30ec1e3431a0c9251591a7a312653967b7ca70.nq.gz
│   ├── d13481fff83b004b9e1937e29f9d3528bc4d2121.nq.gz
│   └── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 0aad249a5609bbeab4c30f42b9709e3b35345c3b.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 23 files
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

[pytest-dev/pytest-scim2-server](https://github.com/pytest-dev/pytest-scim2-server)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
