# Repolex Knowledge Graph of asimov-modules/asimov-readwise-module

RDF knowledge graph data for [asimov-modules/asimov-readwise-module](https://github.com/asimov-modules/asimov-readwise-module), parsed by [repolex](https://repolex.ai).

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
rlex download asimov-modules/asimov-readwise-module
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── d584c58a357ff628278db508e1a75bcb55c9201f
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── d584c58a357ff628278db508e1a75bcb55c9201f.nq.gz
│   └── repolex
│       └── d584c58a357ff628278db508e1a75bcb55c9201f
│           └── chunk-001.nq.gz
├── blob
│   ├── 0521e4d628230fe61807a6b95d317691c3309aeb.nq.gz
│   ├── 096b8dc9970ec70f1043f366594cc59e27aefa43.nq.gz
│   ├── 10b359dd05935c73efb064470f9ecda90f6d28aa.nq.gz
│   ├── 153d47943cc8338cf18167a0b03d8e2f4214803c.nq.gz
│   ├── 2e16d3efe30522c155001fb35841091cc4907e75.nq.gz
│   ├── 50fdb78ded6b140587e08eb2c6d9d21a6bae7d98.nq.gz
│   ├── 5706be67bfd142a5791f90e0e303a7abb04b6f6e.nq.gz
│   ├── 5a758e05d74a3cd70187e3227634df5f53b540c2.nq.gz
│   ├── 62004bd9941f3437b1d028e91d2a826a853bfb6a.nq.gz
│   ├── 645bb06b13ceb855baa2d88d181ead408d728a1e.nq.gz
│   ├── 661f05f317c22362497c756a1685c09123cc9b09.nq.gz
│   ├── 6b23d61018f43b840f8d2ff3b45a1c02d76df38d.nq.gz
│   ├── 6d7043789b028d88f3cd033cfe0595bdb3df5e26.nq.gz
│   ├── 6e8bf73aa550d4c57f6f35830f1bcdc7a4a62f38.nq.gz
│   ├── 75e3b65f99b29f48ab230e3eab3de8d0b7a9229f.nq.gz
│   ├── 76b67eafba62aa6b4b8ea639dbf85c1568648c6a.nq.gz
│   ├── 78302e1b8de7ab8808e9d82013fd6e1ae4e2d4e8.nq.gz
│   ├── 783e5b6e7914cba5a33f77a7276d578f052e47bc.nq.gz
│   ├── 7dd09e82557c4c77216fd59397ec9ffac89d6465.nq.gz
│   ├── 891996d9f2d56e8bc055b87fe77fdb5c061a2edf.nq.gz
│   ├── 9219b8ee51230fa859824dd9a514cc0a6590de9f.nq.gz
│   ├── 9790929ac37703a0e1aaa6deced74f637613d5cd.nq.gz
│   ├── 9fe50de16e59d550235aa6d7d15ee12ddf054414.nq.gz
│   ├── a36fedab8db68b26a76fbbf1de1f549e4a12261b.nq.gz
│   ├── a3c33a72d00e97b5b00a8240fdfcd207593f2516.nq.gz
│   ├── af9908b08f4b33c32a0080af73f53bc0fa0cdce4.nq.gz
│   ├── cf42f6893594e2f8be2b722de51123d65e4d61c4.nq.gz
│   ├── dfaa5845305e0bbc21e9f6ef11af19e56011c2e5.nq.gz
│   ├── e3e57a8ce4ccbf74759a6df8fa4a3980ff1c9209.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── efb98088164f5786b17e83ed384971fc3c74f93c.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── d584c58a357ff628278db508e1a75bcb55c9201f.nq.gz
├── filetree
│   └── d584c58a357ff628278db508e1a75bcb55c9201f.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

14 directories, 40 files
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

[asimov-modules/asimov-readwise-module](https://github.com/asimov-modules/asimov-readwise-module)

---
*Parsed on 2026-09-28 by [repolex](https://repolex.ai)*
