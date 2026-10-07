# Wave engineering backlog

Drafted October 7, 2026 for the October 9 submission. These are local issue drafts,
not published GitHub issues or Wave enrollments. Complexity and points are proposed
planning values (trivial 100, medium 150, high 200); maintainers must confirm scope
and actual enrollment in the Drips app. An issue is not evidence its feature exists.

## 1. [jisr-sdk] Router deployment interface provenance

### Complexity & Points

- Tier: High (200 pts proposed)
- Proposed label: `complexity: high`

### Description & Context

Bind contract helpers to a reviewed deployed interface.

### Requirements & Acceptance Criteria

- [ ] Recover and cite original ABI/source and deployment revision.
- [ ] Validate route_payment arguments and events.
- [ ] Test authorization failures.
- [ ] Do not equate mocks with deployed behavior.
- [ ] Relevant automated checks pass; include positive/negative tests for implemented behavior.

### Relevant Files & Architecture

src/payment.ts; README.md

### Contribution Guidelines

Use a focused `feat:`/`fix:`/`docs:` PR, include `Closes #<issue_id>`, and record
actual local and CI results before requesting review.

## 2. [jisr-sdk] Address checksum validation

### Complexity & Points

- Tier: Medium (150 pts proposed)
- Proposed label: `complexity: medium`

### Description & Context

Reject shape-correct addresses with invalid Stellar checksums.

### Requirements & Acceptance Criteria

- [ ] Use Stellar StrKey checksum validation for G/C addresses.
- [ ] Retain existing endpoint restrictions.
- [ ] Test mutated checksums and valid configured addresses.
- [ ] Relevant automated checks pass; include positive/negative tests for implemented behavior.

### Relevant Files & Architecture

src/network-config.ts; src/network-config.test.ts

### Contribution Guidelines

Use a focused `feat:`/`fix:`/`docs:` PR, include `Closes #<issue_id>`, and record
actual local and CI results before requesting review.

## 3. [jisr-sdk] Compiled consumer package test

### Complexity & Points

- Tier: Medium (150 pts proposed)
- Proposed label: `complexity: medium`

### Description & Context

Verify the published artifact outside the source checkout.

### Requirements & Acceptance Criteria

- [ ] Pack compiled JS/declarations.
- [ ] Install in an isolated consumer.
- [ ] Import public subpaths and typecheck.
- [ ] Ensure no workspace/browser dependencies leak.
- [ ] Relevant automated checks pass; include positive/negative tests for implemented behavior.

### Relevant Files & Architecture

package.json; tsconfig.json; .github/workflows/ci.yml

### Contribution Guidelines

Use a focused `feat:`/`fix:`/`docs:` PR, include `Closes #<issue_id>`, and record
actual local and CI results before requesting review.

## 4. [jisr-sdk] Payment evidence adapter

### Complexity & Points

- Tier: High (200 pts proposed)
- Proposed label: `complexity: high`

### Description & Context

Expose verified payment semantics instead of only transaction success.

### Requirements & Acceptance Criteria

- [ ] Specify native and contract verification boundaries.
- [ ] Retain exact amounts.
- [ ] Reject mismatched fields.
- [ ] Test unknown, failed and partial evidence.
- [ ] Coordinate public export changes.
- [ ] Relevant automated checks pass; include positive/negative tests for implemented behavior.

### Relevant Files & Architecture

src/settlement.ts; src/payment.ts

### Contribution Guidelines

Use a focused `feat:`/`fix:`/`docs:` PR, include `Closes #<issue_id>`, and record
actual local and CI results before requesting review.

## 5. [jisr-sdk] Standalone/workspace parity check

### Complexity & Points

- Tier: Medium (150 pts proposed)
- Proposed label: `complexity: medium`

### Description & Context

Prevent untracked drift between standalone and web workspace SDK copies.

### Requirements & Acceptance Criteria

- [ ] Record the authoritative revision and sync method.
- [ ] Compare source/export surfaces.
- [ ] Detect drift automatically.
- [ ] Document artifact handoff to the API.
- [ ] Relevant automated checks pass; include positive/negative tests for implemented behavior.

### Relevant Files & Architecture

src/; package.json; README.md

### Contribution Guidelines

Use a focused `feat:`/`fix:`/`docs:` PR, include `Closes #<issue_id>`, and record
actual local and CI results before requesting review.

## 6. [jisr-sdk] Network support documentation

### Complexity & Points

- Tier: Trivial (100 pts proposed)
- Proposed label: `complexity: trivial`

### Description & Context

Make network and token support explicit for SDK consumers.

### Requirements & Acceptance Criteria

- [ ] Document Testnet passphrase/token constraints and rejected Mainnet settings.
- [ ] Show injected configuration examples.
- [ ] Include migration criteria for future support.
- [ ] Relevant automated checks pass; include positive/negative tests for implemented behavior.

### Relevant Files & Architecture

README.md; src/network-config.ts

### Contribution Guidelines

Use a focused `feat:`/`fix:`/`docs:` PR, include `Closes #<issue_id>`, and record
actual local and CI results before requesting review.

## Published issue links

- [Router deployment interface provenance](https://github.com/jisr-pay/jisr-sdk/issues/4)
- [Address checksum validation](https://github.com/jisr-pay/jisr-sdk/issues/5)
- [Compiled consumer package test](https://github.com/jisr-pay/jisr-sdk/issues/6)
- [Payment evidence adapter](https://github.com/jisr-pay/jisr-sdk/issues/7)
- [Standalone/workspace parity check](https://github.com/jisr-pay/jisr-sdk/issues/8)
- [Network support documentation](https://github.com/jisr-pay/jisr-sdk/issues/9)

These issues are published but have not been enrolled into Drips Wave or assigned.
