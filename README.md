# Repolex Knowledge Graph of NousResearch/hermes-telegram-business

RDF knowledge graph data for [NousResearch/hermes-telegram-business](https://github.com/NousResearch/hermes-telegram-business), parsed by [repolex](https://repolex.ai).

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
rlex download NousResearch/hermes-telegram-business
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 98c60afc00d36c885bb040ebe973b1aa908886c0
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 98c60afc00d36c885bb040ebe973b1aa908886c0.nq.gz
│   └── repolex
│       └── 98c60afc00d36c885bb040ebe973b1aa908886c0
│           └── chunk-001.nq.gz
├── blob
│   ├── 005051938234322cebd8b8f79300688239d25f27.nq.gz
│   ├── 2881b974da44dae31d25824b3eac1198ba176c82.nq.gz
│   ├── 4095dce9c7f601267a8960d88d4259933932b0ad.nq.gz
│   ├── 54974bce2ab1c0b95e2e7104d9720fb6b610c100.nq.gz
│   ├── 65c4539bb8ed787b4c6c82144f828b6c03e428d1.nq.gz
│   ├── 75410e73319c72cd3e991a501c5455eb78f38375.nq.gz
│   ├── 8728fd8c8e1f8891a7d2754c0ea9abd032d5a1d5.nq.gz
│   ├── 8d4b1062a696cbb392047fd221ca0827fc9f64f2.nq.gz
│   ├── a2efc66815503da82a0d03c5504e1db234c62b55.nq.gz
│   ├── ce62c5b832b5256dbf5d344450906f37cc3968e9.nq.gz
│   └── e78a8541ebad175483a7b07f27bedc6d3d88f088.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 98c60afc00d36c885bb040ebe973b1aa908886c0.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

14 directories, 20 files
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

[NousResearch/hermes-telegram-business](https://github.com/NousResearch/hermes-telegram-business)

---
*Parsed on 2026-10-02 by [repolex](https://repolex.ai)*
