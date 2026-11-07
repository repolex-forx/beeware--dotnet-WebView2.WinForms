# Repolex Knowledge Graph of beeware/dotnet-WebView2.WinForms

RDF knowledge graph data for [beeware/dotnet-WebView2.WinForms](https://github.com/beeware/dotnet-WebView2.WinForms), parsed by [repolex](https://repolex.ai).

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
rlex download beeware/dotnet-WebView2.WinForms
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── f3c1a18615da2bd963c275930eb37bd95030feb9
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── f3c1a18615da2bd963c275930eb37bd95030feb9
│           └── chunk-001.nq.gz
├── blob
│   ├── 015d6cb0376504c4260225d5cc6df1ebf23b93e8.nq.gz
│   ├── 0cec5fae7265f569cee6b20c40ff421795cfa0e4.nq.gz
│   ├── 211cdd00fd5c75fd30f8a16cfc4e127b74257fbc.nq.gz
│   ├── 241175b0e1b54a2e9f53f9970069c1ea28cb0891.nq.gz
│   ├── 2b5889780849daf54d634ad925c9fbaa07778ca7.nq.gz
│   ├── 2e6228b6b2e20f1c22c80c617e71530dfc18cd53.nq.gz
│   ├── 3199844cbdb580d709723a97a3822bd8e7fdf7c7.nq.gz
│   ├── 401cd78bedd917e571b06c1d39a651fe7b19e473.nq.gz
│   ├── 452098a19bd4b697e4ed52450489384bcee83192.nq.gz
│   ├── 4a09c81e23ca735b7d235c71f9ed7feca8081af3.nq.gz
│   ├── 51df2ae34039faea906bdef63eff358c32524ae9.nq.gz
│   ├── 624a2673c51e4d3ee7e5b403fc6c71cb4427b215.nq.gz
│   ├── 70060c49157573ee8d7d59412871cf92921a3037.nq.gz
│   ├── 800ed44ab0afea3b4a9b05cc8f159755251423d3.nq.gz
│   ├── 9eb0b55b180d70b2c9705f26cd46b5a383558dac.nq.gz
│   ├── a5fc00d257fa7bcd065632f250f9938dd2473f00.nq.gz
│   ├── b614af71202c5d62527d2e9d0dfb1ad9cee02085.nq.gz
│   ├── b834affdddcf5014398ca9c16aafe3ea7f2d0422.nq.gz
│   ├── b8da3ecc86f793cf0af7c8439001bdc89aa04ce8.nq.gz
│   ├── b9bcff9ce67bcb72d9851a1e080f12c3c1d9a710.nq.gz
│   ├── bd26d83508060c0a53a0ce1221058c001aecb3f4.nq.gz
│   ├── c4d88e8173e484996f9c1fe716bd0fb7e4c8a73b.nq.gz
│   ├── dc34c2a43f19d123153b96d9380ad080e0f0544e.nq.gz
│   └── fc385611eff86aefacd8cbff9f3cf9cf91ae61fc.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── f3c1a18615da2bd963c275930eb37bd95030feb9.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 32 files
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

[beeware/dotnet-WebView2.WinForms](https://github.com/beeware/dotnet-WebView2.WinForms)

---
*Parsed on 2026-11-07 by [repolex](https://repolex.ai)*
