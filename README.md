# Repolex Knowledge Graph of pyecharts/pyecharts-extras

RDF knowledge graph data for [pyecharts/pyecharts-extras](https://github.com/pyecharts/pyecharts-extras), parsed by [repolex](https://repolex.ai).

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
rlex download pyecharts/pyecharts-extras
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── a3a67417aae0a482e81dd78ce9bbbf3d58be5a7b
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── a3a67417aae0a482e81dd78ce9bbbf3d58be5a7b
│           └── chunk-001.nq.gz
├── blob
│   ├── 01f45d2249a7bf446356d31496424c61baf6b65c.nq.gz
│   ├── 05ac46f6b31d288e7c020babcb84d9841a32dc58.nq.gz
│   ├── 0c10c6ea25bcb2c39000a5c51b21a6440eb62d06.nq.gz
│   ├── 1af1e8f29754ab6f3671baddc956db0cf6fd1e17.nq.gz
│   ├── 205781f6e6a5d1c5be6152311cdc07f81a55bca0.nq.gz
│   ├── 2a9acf13daa95e85642ea255d3e3bd1ef8252804.nq.gz
│   ├── 30ee514f914eab6c3ee240661fc076ed494d2394.nq.gz
│   ├── 3e0ee51423673045d76cf8604c03cc0c6432c58a.nq.gz
│   ├── 42d4f08526f72d54dca92017152d1e93b18ac1b8.nq.gz
│   ├── 457ec1365973a1327e3a7635a0135f5bdc837ac9.nq.gz
│   ├── 59ec574a57d38d54a613574347e0ba02fcaaf164.nq.gz
│   ├── 5a40457a9aef5878e42bcca5a5be88771eb16ee5.nq.gz
│   ├── 5f13ef040f26a35f377fb13a2a48b1a07f973ba0.nq.gz
│   ├── 5f7092223a510c70577655fab5671c27e49ead1c.nq.gz
│   ├── 706fd82535514113b60a10590909aff92ded3461.nq.gz
│   ├── 707df576a8c5fe53cdabc3fac05a4528684622ce.nq.gz
│   ├── 721bf797ccdf3e6efa0aa48b2e6b478b02338adf.nq.gz
│   ├── 7eb0c54a800c9bb20495e6b323b9ae99745c644d.nq.gz
│   ├── 83802c09161941aa9f1726856717aae73e09b2dd.nq.gz
│   ├── 8a042df57e22d8f3a6449e55e450388cc4d58894.nq.gz
│   ├── 904844ddf4a5d322dc097ea6b8e85a618ffb98e1.nq.gz
│   ├── 96454d3615f8f4e8fe5f880d966c833e58e7685c.nq.gz
│   ├── 98e2086176e0b15d418c173b2ed906a275d9e608.nq.gz
│   ├── 9e7ec429162d50a2024d99a660b9995aec80075e.nq.gz
│   ├── ab519b2a4fffc9500f4b854c45760839463f7e6f.nq.gz
│   ├── b1656b3f10b105e0250f4404dac2acbd884e4705.nq.gz
│   ├── b32358b56aed5ed3d7170f7e4c66e3e9bda304ce.nq.gz
│   ├── b6e010400145ade26a91e5e76f8eeb98813ca1b0.nq.gz
│   ├── b70c2782aa78ff135cc4dadbe992727e9a67596b.nq.gz
│   ├── c0bd2f4a9abd1f9e0e0e436dd76167c08eb64d0e.nq.gz
│   ├── d31eeaa644fa18b29af15f226cc02daa5ad59227.nq.gz
│   └── ef74e28684ce01b6c40841973ad32f9ff8619fcd.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── a3a67417aae0a482e81dd78ce9bbbf3d58be5a7b.nq.gz
├── issue
│   └── issue.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 39 files
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

[pyecharts/pyecharts-extras](https://github.com/pyecharts/pyecharts-extras)

---
*Parsed on 2026-10-28 by [repolex](https://repolex.ai)*
