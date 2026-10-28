# Repolex Knowledge Graph of databrickslabs/access-insights

RDF knowledge graph data for [databrickslabs/access-insights](https://github.com/databrickslabs/access-insights), parsed by [repolex](https://repolex.ai).

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
rlex download databrickslabs/access-insights
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── cec80229e8277f55abdf39280ce5fa3820a22c56
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── cec80229e8277f55abdf39280ce5fa3820a22c56
│           └── chunk-001.nq.gz
├── blob
│   ├── 07908820d58595b6b6dd737326b55f000f4cc6ac.nq.gz
│   ├── 0a3999d9bc51d1f02dd8320ea63b2526179cbd84.nq.gz
│   ├── 1ba13b7d343c269ab081c6c345f68bc4e13284f1.nq.gz
│   ├── 1c69ecedfcf492b6c4c02705c00c1fec1eb0ca5d.nq.gz
│   ├── 201540bf51bb8b7a9ef9b48fe89d388a6ff6283e.nq.gz
│   ├── 327840c728821541122b7de63793025be9772f4d.nq.gz
│   ├── 5478f3fff37cc5282ec30e7223cf1f404fc2d8d3.nq.gz
│   ├── 5cd84d5a47b7198f03dcecb31b42d3b105d45a1d.nq.gz
│   ├── 5d017b7fa3de0da89c375f05aba0741eecbcb2a0.nq.gz
│   ├── 624b1c28a07802e7bd2ba2eef779dcff924b60ba.nq.gz
│   ├── 62c68b6bbb70f010166e9ba955e1a473e3ca47fd.nq.gz
│   ├── 6486fd9c69b444d9df12b97c96e0444ebbf3f649.nq.gz
│   ├── 72e42524809c763d9cf1308c89ba8f46cecf02d4.nq.gz
│   ├── 77bd836a4a4ceb3d9df3c60f5da713c75fd5850a.nq.gz
│   ├── 78222ce8fc1dde318ee9963b28cf6b293395262a.nq.gz
│   ├── 8c9f5012222cac3bea29b24640e37544c17f35ef.nq.gz
│   ├── 921c49d9cb84f01ddb9f36bad227597a9d2f831a.nq.gz
│   ├── 93aa3c90041980814d85cc8ce6c4445a191ef62a.nq.gz
│   ├── 95d5643d1aca50fdf6d996d53d727b9cc894abb9.nq.gz
│   ├── a25781eabee705cefb1218ea8ca02ba39af7a7bd.nq.gz
│   ├── a9304c3c43f19fddf761b6a7a28067a2d9eb3b81.nq.gz
│   ├── acefd7e8e7180bece4e426a39b131f72095263b4.nq.gz
│   ├── b8802735707e9a21b7dd765ad409da1fad57072a.nq.gz
│   ├── bb0bc5b4ce4fd865171d215b1cd5197b76d8d76e.nq.gz
│   ├── bca953872f27ad59fb34a97c8dcb286704ae09b9.nq.gz
│   ├── c077e39a4ddeffeb60e1d1d7f575e1480600b524.nq.gz
│   ├── c0dad87aa359b66ad02925173f5ef91327ae9f4c.nq.gz
│   ├── c6431a91bac3b005af8c9f6b962b9b19de36d4bd.nq.gz
│   ├── cc40e8bbfe16384b3cde5bd141091c117b3f7f68.nq.gz
│   ├── e1f20bd5fa6aa4d52c5743b6578884f6d0271308.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── f12d219b6f96e7d1611e50a56ae2638b7e9bdcbd.nq.gz
│   └── fd851c4d5eee791ad6210632a1141b4e068020ae.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── cec80229e8277f55abdf39280ce5fa3820a22c56.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 41 files
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

[databrickslabs/access-insights](https://github.com/databrickslabs/access-insights)

---
*Parsed on 2026-10-28 by [repolex](https://repolex.ai)*
