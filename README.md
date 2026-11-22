# Repolex Knowledge Graph of jaraco/jaraco.envs

RDF knowledge graph data for [jaraco/jaraco.envs](https://github.com/jaraco/jaraco.envs), parsed by [repolex](https://repolex.ai).

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
rlex download jaraco/jaraco.envs
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   ├── 3da05f25098b22e1b46acb72849c1b95d8433fc4
│   │   │   └── chunk-001.nq.gz
│   │   └── c888dd198b345d1a0e7c381f7bc410495ee36c90
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── c888dd198b345d1a0e7c381f7bc410495ee36c90.nq.gz
│   └── repolex
│       ├── 3da05f25098b22e1b46acb72849c1b95d8433fc4
│       │   └── chunk-001.nq.gz
│       └── c888dd198b345d1a0e7c381f7bc410495ee36c90
│           └── chunk-001.nq.gz
├── blob
│   ├── 02879483d75ae9c6446e89efef6705158f817ae5.nq.gz
│   ├── 053c728715869f89a5b87da64e26cf43ecb4ac86.nq.gz
│   ├── 1bb5a44356f00884a71ceeefd24ded6caaba2418.nq.gz
│   ├── 1f2aa7533b0423a8eb943f6f4ec02498e39581a0.nq.gz
│   ├── 21865d9728e320523933766119e04f867fbc3505.nq.gz
│   ├── 21b7ba2f2b3055aaee2ffd553293c7e160aa2d14.nq.gz
│   ├── 235d98cbb40a278e616ba342f705b4d3dca8e3ee.nq.gz
│   ├── 240329c3604d8ead4c10aa8c88352caa8e4ce7b2.nq.gz
│   ├── 28e36786791c9c11a6030bb433fc132bf14966c3.nq.gz
│   ├── 2e3f4dd791a6372b427d618eb0baa8c4dc58e5f0.nq.gz
│   ├── 304196f81e11a168c9894f966e4a617ebf4ed53c.nq.gz
│   ├── 32150488de655c2c2ef3b26c0a8519e7365584b3.nq.gz
│   ├── 33da3deb0801e1c014c1aa1330fac487fd70cd32.nq.gz
│   ├── 375602d7bca46cdde4e3e6cae3e6a7ac3719bcc5.nq.gz
│   ├── 54c9000ec94341dd65c2053251b85b124017b9b5.nq.gz
│   ├── 54cc8303b22089e12053e552d4e6cb852a865b8a.nq.gz
│   ├── 577e87a793a20e413f7321f4f17ec1eba2ea1962.nq.gz
│   ├── 58f88383104dc7a97b1ee6c5b4572ea0eac3a346.nq.gz
│   ├── 5bdc232005af9be104a00437ae9bc64417a4c1cc.nq.gz
│   ├── 5c05f9e27d57a4b7a3c3a9fdfecf8cddb8be499f.nq.gz
│   ├── 64378f09c962e1f3a2934c83adadadf2e6a4249e.nq.gz
│   ├── 6fa480e44f38768722368d7a986607adacf41d99.nq.gz
│   ├── 700235be57c1b2872455c0be5333f59cf568e252.nq.gz
│   ├── 724370638fc188317bbc7dc868f1a571995fd796.nq.gz
│   ├── 89ff33961ba3d6f9cda89322a1fdbf1ac2e35513.nq.gz
│   ├── 92707eaa45889a28d045ee884f5f2e9590485c4d.nq.gz
│   ├── 9a0f3bce1395ae3819030b822e5d9076c85068ea.nq.gz
│   ├── af50201060a0071f6abbef8e994784252fbdd9aa.nq.gz
│   ├── b6f972769e61a5e65f9f45015b363cc362487e55.nq.gz
│   ├── b979eb71c6f1f460b5cb712cf992e406fe32ac38.nq.gz
│   ├── cef985d5d752fa132670c048c6bccaf602b685a3.nq.gz
│   ├── d9a15ed19a2371862140f960add17c93318d8b35.nq.gz
│   ├── dce944dfc3cd4008203c1a71d431447d6911b0af.nq.gz
│   ├── e05a3d4a2ab888e32952006d8cd380864368db5f.nq.gz
│   ├── efcb8cbc2043faa7caf4f92fc7488bd6914c934c.nq.gz
│   └── faf84fc56bc6d8133cab672ccb248d86e8b28150.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   ├── 3da05f25098b22e1b46acb72849c1b95d8433fc4.nq.gz
│   └── c888dd198b345d1a0e7c381f7bc410495ee36c90.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

16 directories, 48 files
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

[jaraco/jaraco.envs](https://github.com/jaraco/jaraco.envs)

---
*Parsed on 2026-11-22 by [repolex](https://repolex.ai)*
