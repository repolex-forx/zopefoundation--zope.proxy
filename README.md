# Repolex Knowledge Graph of zopefoundation/zope.proxy

RDF knowledge graph data for [zopefoundation/zope.proxy](https://github.com/zopefoundation/zope.proxy), parsed by [repolex](https://repolex.ai).

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
rlex download zopefoundation/zope.proxy
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 2a8e64eec89bdb2610b2cf3d46105e541b5a0c15
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 2a8e64eec89bdb2610b2cf3d46105e541b5a0c15
│           └── chunk-001.nq.gz
├── blob
│   ├── 0c8758c4bc5c70211e93cd3467bf8be58ac68900.nq.gz
│   ├── 10e5b5bc5331d61a200ad620476fbb23bacc987e.nq.gz
│   ├── 136dce6aa161a696f3a0a762e7e6323ea6b87833.nq.gz
│   ├── 15421e1567282d1ad720ef95d637893055272ab7.nq.gz
│   ├── 178687ef2816491ba8f22f63e938cf5ca76c2686.nq.gz
│   ├── 20a30020c0876f9bc282180fa9f8519f243330e8.nq.gz
│   ├── 23f228fb2ad91253bd00475ba95f9daa01a174e8.nq.gz
│   ├── 3ce56bef6a90131648199066767f461d4736a7f0.nq.gz
│   ├── 50a05474490bac6eb3d5f854cb7a972c5c3d5725.nq.gz
│   ├── 63f25b331fbf78693b4ce97ea68deadd4e7b131d.nq.gz
│   ├── 66f5962322eefc7190cd713ac7091f2be9f91d52.nq.gz
│   ├── 70cd903fe32abadc88f78f2aaf71f630303ff331.nq.gz
│   ├── 77f3c744e601e8cdd746df3914bf9c9c8ea5365f.nq.gz
│   ├── 786a94698c74bb6f440ecf7c311c4630f365afde.nq.gz
│   ├── 79859e06010bf4967c5b4b044afea6ef39742938.nq.gz
│   ├── 7c0cff4708bf547d5064aa77f2f316a3dee9aafb.nq.gz
│   ├── 80035993aaef1cb71f9841d1f643a0ce50b38af5.nq.gz
│   ├── 8043da76b239489164439523f5c8ba805c37b1ed.nq.gz
│   ├── 858a4c0e2f6cd8252744d8b39b0920008247cb7e.nq.gz
│   ├── ae36613303e0d433581c953532d85363e5b9a1f1.nq.gz
│   ├── b157da8387f294feeef9aeac1f7e70d4bf2261ac.nq.gz
│   ├── b711d3609fdefd7664f2982d225d96f5e53be9c0.nq.gz
│   ├── ba6f7b368fd6c6b8f3b353eba3705bb7e7eba74b.nq.gz
│   ├── bab7f94be5ef86cce49612e6cdab326a57143d7d.nq.gz
│   ├── c1a986628202a71eb9a36f04e27670ae38c8368b.nq.gz
│   ├── c32423560f78ae960a5d7f3ff78c44ffe587fa76.nq.gz
│   ├── c9557a8ec5ecb246861af64c258aef6f456687be.nq.gz
│   ├── ca5826688a534884d4645d37f8b95487a352e4cf.nq.gz
│   ├── d25c6853140bc727e6bc6d2830ab886c9f31ce76.nq.gz
│   ├── d4b7cab16a152ff785fe83f619d3fa7de4dabbe0.nq.gz
│   ├── d7f30737ed15c773b35753faef4b6e5f68c1e69d.nq.gz
│   ├── d9e113ec685b92b018297dd2f200341d1fba01f9.nq.gz
│   ├── dc88bda8280a2169b5f3aa64d6dd51b1fc2fc950.nq.gz
│   ├── e195dc129606a34ea5ca18d59a51421cb25d1cd2.nq.gz
│   ├── e1f9ad7b3b48377bfbfaa1b380c384ddea24060f.nq.gz
│   ├── e62eec2685820226d926dae3ba92518b526a522e.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e86bb0827e323a682b909b67cb9f905a58d95799.nq.gz
│   └── f20f4572860b370633c99b5d5a4e314f1ab712de.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 2a8e64eec89bdb2610b2cf3d46105e541b5a0c15.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 47 files
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

[zopefoundation/zope.proxy](https://github.com/zopefoundation/zope.proxy)

---
*Parsed on 2026-11-06 by [repolex](https://repolex.ai)*
