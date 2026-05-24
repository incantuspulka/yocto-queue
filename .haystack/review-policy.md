# Review Policies

## Public API contract surface
- **Paths**: `index.js`, `index.d.ts`, `readme.md`, `test.js`
- **Severity**: high
- **Reason**: This library’s value is a tiny stable API; AI-generated edits can pass CI while still introducing runtime/type/doc contract drift for downstream consumers.

## Instructions
- If a PR changes queue method behavior or signatures, require human judgment that the compatibility tradeoff is acceptable for existing users.
- If a PR touches iterator or drain behavior, require human confirmation that non-destructive iteration versus destructive draining remains intentional.
- If a PR changes how empty-queue cases are represented, require human judgment on consumer impact, especially where undefined can also be a valid queued value.
