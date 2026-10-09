# October 9 submission verification

Executed October 7, 2026 in the shared Linux workspace. Baseline source revision:
`4a21043ec238a11adbc9c99f858e438fbc4fad9e`. Preparation changes affect documentation/governance and, where noted,
CI checks; no runtime implementation or public API was changed.

## Local results

Runtime: Node 22.23.2, TypeScript 5.9.3 and pnpm 11.8.0.

- `CI=true npx --yes pnpm@11.8.0 install --frozen-lockfile`: passed.
- `npx --yes pnpm@11.8.0 test`: 49 passed.
- `npx --yes pnpm@11.8.0 typecheck` and `build`: passed.
- API `npm run check:sdk` passed under Node 24.15.0 in an isolated offline
  consumer of the pinned compiled artifact. Existing source/artifact provenance
  is recorded in the API SDK_REVIEW.md; no source/API export changes were made.
- The standalone source matches the web workspace copy byte-for-byte.
- CI now uses frozen-lockfile installation and read-only contents permission.
  Current default-branch CI passed before these preparation changes; the PR
  must supply fresh workflow results for the changed CI configuration.

## Review and publication

- `git diff --check`: passed after preparation edits.
- CI YAML parsed locally. A syntax parse does not replace GitHub execution.
- Six engineering issues were published with bounded acceptance criteria and
  proposed complexity; links are in WAVE_BACKLOG.md. No Wave labels/enrollment
  or contributor assignments were performed.
- Maintainer EthTobi were owner-confirmed; GitHub contact and
  anytime availability apply. GitHub App coverage/application slots still
  require dashboard confirmation.
- Changes will be proposed through a fork PR because the available account
  cannot push directly to the organization's protected branch. Merge decisions
  remain with maintainers. Recheck the final PR checks before applying.

## October 8 recheck

Node 22.23.2: 49 tests and TypeScript build passed again. Preparation PR #10 remained open at this observation.
