# Repolex Knowledge Graph of allenai/molmospaces_policy_zoo

RDF knowledge graph data for [allenai/molmospaces_policy_zoo](https://github.com/allenai/molmospaces_policy_zoo), parsed by [repolex](https://repolex.ai).

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
rlex download allenai/molmospaces_policy_zoo
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── dc54f532b12c414d83c03a0e3733eb1aa9d318bc
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── dc54f532b12c414d83c03a0e3733eb1aa9d318bc
│           └── chunk-001.nq.gz
├── blob
│   ├── 00b0849260372d58bcbf631772694225d9aa098c.nq.gz
│   ├── 20729c6aadde606a41416b2984bef8cecb0eb79d.nq.gz
│   ├── 261eeb9e9f8b2b4b0d119366dda99c6fd7d35c64.nq.gz
│   ├── 2c0733315e415bfb5e5b353f9996ecd964d395b2.nq.gz
│   ├── 2ca1926a4c13ceca134a3a09636d27adbf2c37e5.nq.gz
│   ├── 36978fc907d85235517679613ba52da5d6c37a55.nq.gz
│   ├── 976845d6f18187567615bf041b333d26b52515be.nq.gz
│   ├── a09f351434bc9a81235610d10a6739e6259a1a18.nq.gz
│   ├── a8c22fe549ae229e93487ef60a99c4b9b2ec703e.nq.gz
│   ├── b71d5abe8cd8cb60ea34900c418f87dfc9763691.nq.gz
│   ├── d9ecedb3bd1717a52ab3fef52c1bb7a469b69aee.nq.gz
│   └── f0681843f525095e33f89ebee3e25d308830033b.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── dc54f532b12c414d83c03a0e3733eb1aa9d318bc.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 19 files
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

[allenai/molmospaces_policy_zoo](https://github.com/allenai/molmospaces_policy_zoo)

---
*Parsed on 2026-11-07 by [repolex](https://repolex.ai)*
