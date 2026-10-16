# Release verification

Release: 1.0.2.

All four projects passed TypeScript checks, production builds and static preview generation with Node.js 24.19.0. Detailed build results are recorded in qa/v1.0.2-builds.json in the seller repository.

This release migrates demo product identifiers and the sample material label, clarifies AI development and marks specifications/reviews as fictional. Browser verification of the refreshed layouts and product routes is recorded separately before packaging.

Earlier v1.0.1 route testing is historical evidence, not a claim that the entire earlier test matrix was repeated in v1.0.2.

Refreshed browser checks: all 12 home layouts at 1440px and 390px (24 checks), plus listing/detail routes for every layout at 390px (24 checks), passed the targeted legacy-reference, heading/error, visible broken-image and overflow checks. This is not a claim of a full accessibility/security/legal audit.
