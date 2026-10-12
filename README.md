# Repolex Knowledge Graph of scrapy/xtractmime

RDF knowledge graph data for [scrapy/xtractmime](https://github.com/scrapy/xtractmime), parsed by [repolex](https://repolex.ai).

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
rlex download scrapy/xtractmime
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 9d50fcb0d7abd7a96f7dee746d9285faba4af6db
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 9d50fcb0d7abd7a96f7dee746d9285faba4af6db
│           └── chunk-001.nq.gz
├── blob
│   ├── 0245b07ff7c5ef82ab2d9c116ff4dd6aa865dac2.nq.gz
│   ├── 0639b98ba1c5c9418dc5ce945423e33762de6d35.nq.gz
│   ├── 0a6eee067f4b81c4c0f97221cc0246b3e2201612.nq.gz
│   ├── 0f354e1ba64798495095c15bb631b4b9a69e0d29.nq.gz
│   ├── 1ff803385af2d1616d294c4034e5ff22e6e62d9a.nq.gz
│   ├── 25e7b847215c4e44dddc56427a30d113d90f0f20.nq.gz
│   ├── 2bcec7c0e5491d292f0ea3160dd63b53b4f5b9b9.nq.gz
│   ├── 3f4715b64e4cd8b73611b9d89838db01a7fc1bc6.nq.gz
│   ├── 489069c6ab6ee33df27833c39ac2294e609180af.nq.gz
│   ├── 4dfe5637e12622c1f0bd65235a1422672b656dc9.nq.gz
│   ├── 4ef6504ce1bf567e54147e876a92690261adc055.nq.gz
│   ├── 59e5f8e5c92c571ae9179f0e9987068213b39abc.nq.gz
│   ├── 645ccc2d6726ab7275a56f1441315e3e84f444b7.nq.gz
│   ├── 7456528682f20eb88fcf446e70b42c91448ffb29.nq.gz
│   ├── 7653731f88e1ce693f5df1f86bc7ef19ecd87c2d.nq.gz
│   ├── 7729e1535d76b1ca4a8ec6bf49ba1fc7b2b97877.nq.gz
│   ├── 87a99a4855c8a2ad87062295c26912038f6c6f50.nq.gz
│   ├── 9ebc9c571eb73c486de12020350f8f3a7463d4c9.nq.gz
│   ├── a302ae01da6536138bed46cbeeed8dd2ebadd77c.nq.gz
│   ├── a795db98cec5956f5ca8a12b1cf6e0ad85c9b855.nq.gz
│   ├── b11552f9cb6937d59b18518e3c1cd023ea50359b.nq.gz
│   ├── b192f957756c837ea00f71f329fa66936378ef84.nq.gz
│   ├── b26680f47d4db4dad19317862e06339474ddd686.nq.gz
│   ├── b911e757141996c0e2d31fc8033a40da1e51ee9c.nq.gz
│   ├── ba42661681f3258ec98dac75dc6f6a19b0c12e72.nq.gz
│   ├── bf15ca732f58894c717fe9b4fc595f72802a162d.nq.gz
│   ├── c691f0f0628066eaa50c3d099e7f4d672f8c468c.nq.gz
│   ├── d134f76dafdb4740836d0f9619efef755816cb0b.nq.gz
│   ├── d3e1d0e0de8b366880c2c8cc07bd0367b9535c19.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── f74ca14ecf37072af3b993971e5fd103858169a5.nq.gz
│   └── fd120c3ab2b03e5f75f84c3fdb15bde10c1f76d8.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 9d50fcb0d7abd7a96f7dee746d9285faba4af6db.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 40 files
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

[scrapy/xtractmime](https://github.com/scrapy/xtractmime)

---
*Parsed on 2026-10-12 by [repolex](https://repolex.ai)*
