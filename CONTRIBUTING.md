# Contributing

Thanks for helping make Mock Data Generator better. The source code is private, so contributing looks a little different from an open-source project. Everything goes through this repository.

## Reporting a bug

Use the [bug report form](../../issues/new?template=bug_report.yml). The most useful thing you can include is **the smallest model file that shows the problem**: two or three models with the fields involved, with anything private renamed. Most bugs are about how a particular model was read, and with the model they can usually be reproduced in minutes.

Logs help too. Set `"mockDataGenerator.logLevel": "debug"` in your settings, run the command again, then copy the **Mock Data Generator** output channel (View → Output, pick it from the list). Remove connection strings, hostnames and passwords before pasting.

## Asking for a feature

Use the [feature request form](../../issues/new?template=feature_request.yml). Describe the problem you have rather than only the solution you picture; there may be a way to do it already, or a better fit for how the extension works. If you're not sure it's a feature yet, start in [Ideas](../../discussions/categories/ideas).

## Suggesting code changes and patches

You can't open a pull request against the extension's code, but you can still send code:

1. Open a [code suggestion](../../issues/new?template=code_suggestion.yml).
2. Describe the problem and the change. If you worked out a fix, paste it: a snippet, pseudo-code, or a standalone function that does the job. A test case (a model file and the output you expect) is just as valuable as code.
3. Tick the box agreeing to [CLA.md](CLA.md). Without it, the suggestion can't be used.

The maintainer writes the change in the private source, credits you in the release notes (unless you ask not to be), and links the release in your issue.

Pull requests to **this** repository are welcome for its own files: documentation, issue templates and typo fixes. They're covered by [CLA.md](CLA.md) as well.

## Testing pre-releases

Pre-releases (odd minor versions, such as 2.3.x) are where new features land first.

1. On the extension's page in VS Code, click **Switch to Pre-Release Version**, or install the `.vsix` from [Releases](../../releases).
2. Try it on a real project: your own models are the best test there is.
3. Post what you tried and how it went in that version's thread in [Testing](../../discussions/categories/testing), even if everything worked. "Prisma + PostgreSQL, 40 models, fine" is useful.
4. If something broke, open a bug report and mention the pre-release version.

To go back to the stable version, click **Switch to Release Version**.

## Labels

| Label | Meaning |
| --- | --- |
| `bug` | Something doesn't work as documented |
| `enhancement` | A new feature or a change to an existing one |
| `code-suggestion` | Comes with a proposed change or patch |
| `needs-repro` | Waiting for a model file or steps that show the problem |
| `confirmed` | Reproduced by the maintainer |
| `planned` | Accepted and on the roadmap |
| `fixed-in-prerelease` | Fixed in a pre-release; please test it |
| `released` | Fixed or shipped in a stable release |
| `wontfix` | Won't be changed; the issue says why |

## Conduct

Everyone taking part is expected to follow the [Code of Conduct](CODE_OF_CONDUCT.md).
