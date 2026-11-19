# Security

## Reporting a vulnerability

**Don't open a public issue for a security problem.** Report it privately instead: [open a security advisory](../../security/advisories/new) (Security tab → **Report a vulnerability**). Only the maintainer can see it.

Include:

- the extension version, VS Code version and operating system,
- what an attacker could do, and what they'd need first (for example a crafted model file in a workspace you open, or control of a database you connect to),
- steps or a file that shows it.

You'll get a reply within 7 days. Fixes for confirmed problems are released as soon as they're ready, and the advisory is published afterwards, crediting you unless you'd rather not be named.

## Supported versions

Only the latest stable release and the latest pre-release get security fixes. Update before reporting, if you can.

## What's in scope

Problems in the extension itself, such as:

- running code or commands from a workspace's model files or settings,
- leaking database credentials or connection strings (to logs, settings, storage or the network),
- SQL or command injection through model names, field names or settings,
- Docker containers created with unsafe settings beyond the documented development defaults.

Out of scope: vulnerabilities in VS Code, Docker or the database servers themselves, and the documented default container passwords, which are public and meant for local development only.
