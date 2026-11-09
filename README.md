# Repolex Knowledge Graph of rust-lang/rustc-hash

RDF knowledge graph data for [rust-lang/rustc-hash](https://github.com/rust-lang/rustc-hash), parsed by [repolex](https://repolex.ai).

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
rlex download rust-lang/rustc-hash
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── f16da569fcb867fa1bc3b5dba18c9b8f7ca99483
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── f16da569fcb867fa1bc3b5dba18c9b8f7ca99483
│           └── chunk-001.nq.gz
├── blob
│   ├── 468cd79a8f6e50f2b24558c41ed3abafa5bb40ae.nq.gz
│   ├── 5f151c9390dc6df01bea6a5e2adb4df7faceebc9.nq.gz
│   ├── 6d76b7c163afe4bc858c3b4af5e393d59235ee6f.nq.gz
│   ├── 84c47ed70dfbfe643b6552613fccf90b0f06aa1f.nq.gz
│   ├── 9230d4e77362f2e705ab36e33b8c73f39d1c3dac.nq.gz
│   ├── a7e77cb28d386ec6eddeaabf441f91473ddefa1e.nq.gz
│   ├── aba98d31f58a80e1bf5a2ac607a1bb14da74e7b5.nq.gz
│   ├── ba5f3635446efa6b537c6580738a33423e840aff.nq.gz
│   ├── bcac3455ac90d6e48533eb77c417d6f00f64a94a.nq.gz
│   ├── d6d774281213a9fd2e1f1fc8b2271bfe56062063.nq.gz
│   ├── e205064e5b26e877465ee5c53331b0f49c728e0d.nq.gz
│   └── e84190625939e81c859cc0f2ca6b5c634fe93a11.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── f16da569fcb867fa1bc3b5dba18c9b8f7ca99483.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 20 files
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

[rust-lang/rustc-hash](https://github.com/rust-lang/rustc-hash)

---
*Parsed on 2026-11-09 by [repolex](https://repolex.ai)*
