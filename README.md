# Template summaries

Index of project templates. Every template is its own repository named `template-*`; this README lists them all
with a one-paragraph summary, so you can find the right one without opening each repository.

## Templates

| Template | Stack | Use it for | Status |
|---|---|---|---|
| [template-sqlmesh-duckdb](https://github.com/CarlosSolrac/template-sqlmesh-duckdb) | Python 3.13, uv, DuckDB, SQLMesh | Batch data pipelines: ingest sources into typed raw tables, transform them with tested SQL models, block bad data with audits | Ready |

### template-sqlmesh-duckdb

Ingestion adapters (ports and adapters) replace typed raw tables; SQLMesh models transform them in plain DuckDB SQL;
blocking audits keep bad rows out of the marts; one composition root wires it together and restates downstream models
on every run. Its `docs/design.md` is the worked example of a design spec.

## Start a project from a template

    gh repo create <your-project> --template CarlosSolrac/<template> --clone

Then, in the new project, ask Claude Code: "Configure this repository to follow the python-code-standards."

## Adding a template

Name the repository `template-<stack>`, starting with a letter after the prefix so this index keeps sorting first.
Mark it as a template (`gh repo edit --template`), and add a row and a summary here in the same change.
