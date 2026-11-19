# Mock Data Generator — Community

This is the public home of the [Mock Data Generator](https://marketplace.visualstudio.com/items?itemName=BuddieKodex.mock-data-generator) extension for VS Code. The extension's source code is private; this repository is where you report bugs, ask for features, ask questions, suggest code changes and test new builds.

The extension reads the models already in your project (TypeScript, JavaScript, Prisma, Mongoose, TypeORM, Drizzle and Zod), generates related records whose foreign keys agree, and writes them as JSON, SQL, CSV and other formats, or inserts them into MySQL, PostgreSQL, SQLite, SQL Server, Oracle or MongoDB.

## Where to go

| You want to… | Go here |
| --- | --- |
| Report something that doesn't work | [Open a bug report](../../issues/new?template=bug_report.yml) |
| Ask for a new feature or model format | [Open a feature request](../../issues/new?template=feature_request.yml) |
| Ask how to do something | [Q&A discussions](../../discussions/categories/q-a) |
| Share an idea before it's a request | [Ideas discussions](../../discussions/categories/ideas) |
| Suggest a code change or send a patch | [Open a code suggestion](../../issues/new?template=code_suggestion.yml) — see [CONTRIBUTING.md](CONTRIBUTING.md) |
| Try a pre-release and report back | [Testing discussions](../../discussions/categories/testing) |
| Report a security problem | [Report it privately](../../security/advisories/new) — see [SECURITY.md](SECURITY.md) |

Search the existing issues and discussions first; adding a 👍 to an existing issue helps decide what gets worked on.

## Getting the extension

- **Stable**: install "Mock Data Generator" from the Extensions view in VS Code (`Ctrl+Shift+X` / `Cmd+Shift+X`).
- **Pre-release**: on the extension's page in VS Code, click **Switch to Pre-Release Version**. Pre-releases have an odd minor version (2.3.x, 2.5.x).
- **A specific build**: every version's `.vsix` is attached to [Releases](../../releases). Install it with **Extensions → … → Install from VSIX…**, or `code --install-extension mock-data-generator-<version>.vsix`.

## Documentation

- The extension's full guide is on its [Marketplace page](https://marketplace.visualstudio.com/items?itemName=BuddieKodex.mock-data-generator).
- [Database containers (Docker)](docs/docker-setup.md)
- What changed in each version: [Releases](../../releases)

## License

The extension is proprietary software, free to use under the terms of its license, which ships with the extension and is shown on the Marketplace page. The files in this repository (issue templates and documentation) are there so you can take part; contributions you make here are covered by [CLA.md](CLA.md).
