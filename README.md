# Repolex Knowledge Graph of florimondmanca/asgi-htmx

RDF knowledge graph data for [florimondmanca/asgi-htmx](https://github.com/florimondmanca/asgi-htmx), parsed by [repolex](https://repolex.ai).

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
rlex download florimondmanca/asgi-htmx
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── c433c294db285bc0ce33b1f32fe7d824443b3844
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── c433c294db285bc0ce33b1f32fe7d824443b3844
│           └── chunk-001.nq.gz
├── blob
│   ├── 0254bf0210c1231a673ff9529e65a13273707ce8.nq.gz
│   ├── 15608b6742ca4cbc1eb9ada0b24d2d16d865bfdf.nq.gz
│   ├── 20a4723fcd68451d17492f9aa60dab1279be12b4.nq.gz
│   ├── 26ee97e903b9f300b292e9908df1193dd80169eb.nq.gz
│   ├── 3419e796a02ba5372a9238c05c76f2b24dc5d5a2.nq.gz
│   ├── 3abd87404074d2a2ac60020c42c7ed9bc5f976c7.nq.gz
│   ├── 405f33e98e0e5cfd13d7acd8a88dd467687779a5.nq.gz
│   ├── 49139e012b8905b8b421e488415d4e509f1838bc.nq.gz
│   ├── 4def141ce105fbf0aa86cc6615bfea8101066426.nq.gz
│   ├── 53e032f1368bd8d29dfa20a709c046b6eafe079a.nq.gz
│   ├── 5580482f3fefe5620609489b3e1682dddde5cdbc.nq.gz
│   ├── 6ffbb1a97562b9929262c35dc4ce1527309be2aa.nq.gz
│   ├── 73958326b284fe166441713a00cea87b810354b9.nq.gz
│   ├── 77653d3caa46de4f1cf77d536bb0445d962ce774.nq.gz
│   ├── 89231a3ed3ed726f19549853dad5d71fdfb5bdc3.nq.gz
│   ├── 97a9ecfc2a5adefb1713c0860f371d5af08153c6.nq.gz
│   ├── 9b96a66c9d376037383e55f414d7100f249bf9fa.nq.gz
│   ├── 9cf96838af150525d192e0b52060ce3a20676e17.nq.gz
│   ├── acba6d2eccac1b9ab667c399df9e367a9a256292.nq.gz
│   ├── ca8509b225240452480105b74669f3c5d8d94254.nq.gz
│   ├── d88f5debc4e21bd21c77583a14f38c4742dc39e3.nq.gz
│   ├── dd07cfab7465fdb61f43f897f61fb3c1096083b6.nq.gz
│   ├── e13f07b49a1989b515117a1712b9533ca5b2f424.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── f82325c3a5051f43e11e9060424b210b9c3087d1.nq.gz
│   └── fd056d1edde4b4fb2870382b4b3010560151c988.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── c433c294db285bc0ce33b1f32fe7d824443b3844.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 34 files
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

[florimondmanca/asgi-htmx](https://github.com/florimondmanca/asgi-htmx)

---
*Parsed on 2026-10-20 by [repolex](https://repolex.ai)*
