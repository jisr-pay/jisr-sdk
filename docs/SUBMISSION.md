# Reusable Stellar payment and settlement primitives

Prepared for the October 9, 2026 Stellar Wave submission.

## Purpose and implemented utility

The compiled JS/TypeScript package provides exact amount parsing, typed errors, injected network/storage/wallet ports, transfer journaling, and read-only settlement lookups. Jisr API consumes its compiled artifact; the web workspace contains matching source.

## Reproduce the implementation

Node 22.13+; `pnpm install --frozen-lockfile`, `pnpm test`, `pnpm run typecheck`, `pnpm run build`. The package exports compiled JavaScript and declarations and can be packed for an isolated consumer.

## Evidence and supported scope

Standalone source matches the web workspace copy. Existing handoff records 49 SDK tests and installed API consumer verification. Testnet only; contract submission helpers are implemented, but original router source/deployment provenance remains unavailable. Transaction success does not itself verify payment details.

Evidence reference: [https://github.com/jisr-pay/jisr-api/blob/main/SDK_REVIEW.md](https://github.com/jisr-pay/jisr-api/blob/main/SDK_REVIEW.md).
Baseline source revision: `4a21043ec238a11adbc9c99f858e438fbc4fad9e`. Final reviewed preparation revision and CI
results belong in [VERIFICATION_OCT09.md](VERIFICATION_OCT09.md).

## Maintainers and contributor work

Maintainers: xteesamz and EthTobi; contact via GitHub, available anytime.
See [MAINTAINERS.md](../MAINTAINERS.md), [CONTRIBUTING.md](../CONTRIBUTING.md),
[SECURITY.md](../SECURITY.md), and [CODE_OF_CONDUCT.md](../CODE_OF_CONDUCT.md).
The [focused engineering backlog](WAVE_BACKLOG.md) describes real work, relevant
files, tests, and acceptance criteria. Draft complexity values require maintainer
review and app enrollment; they do not establish approval or earned points.

## Before applying

- Confirm the Drips Wave App covers this repository and check application slots.
- Publish the reviewed backlog issues and preserve links to their acceptance checks.
- Publish these preparation changes through a reviewed PR with passing CI.
- Apply under the implemented scope above; no production/adoption claims are implied.
