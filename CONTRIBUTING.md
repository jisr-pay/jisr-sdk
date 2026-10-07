# Contributing to Jisr SDK

Use Node 22.13+ and the pnpm version used by CI. Install with
`pnpm install --frozen-lockfile`, then run `pnpm test`, `pnpm run typecheck`,
and `pnpm run build`. Tests use Node's built-in runner; add positive and negative
cases for changed amounts, configuration, payment, journal, or settlement behavior.

Use `feat/<topic>`, `fix/<topic>`, `docs/<topic>`, or `test/<topic>` branches.
PRs explain the problem, resulting behavior, actual command results, and
compatibility changes. Include `Closes #<issue_id>` for the issue implemented;
open a tracking issue first if needed. Required CI must pass before merging.

Coordinate public-interface changes with web and API maintainers. Keep SDK imports
browser-free, inject wallet/network/storage dependencies, preserve exact decimal
amounts and immutable transfer identity, and retain pending outcomes on uncertain
network responses. Never store credentials or signed transaction payloads.

Follow the organization [security policy](https://github.com/jisr-pay/.github/blob/main/SECURITY.md)
and [code of conduct](https://github.com/jisr-pay/.github/blob/main/CODE_OF_CONDUCT.md).
