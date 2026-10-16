# English edition verification / 15 October 2026

Release: 1.0.1.

- All four source projects passed TypeScript checks and production builds with Node.js 24.19.0.
- English audit scanned 482 source, demo, documentation and seller text files, excluding dependencies and generated development folders. No Thai letters were found. The Thai baht currency symbol is intentionally retained.
- All 57 page routes checked at 1440px and 390px: 114 rendered-page checks for English document language, Thai text in page content/accessibility attributes, JavaScript errors and horizontal overflow. Coverage includes every layout home/list/detail, supporting pages, stories, overview and studio pages.
- Menu, search, cart and size dialogs checked where those controls are present on audited pages.
- All twelve home layouts checked at both widths: no missing images, HTTP resource failures, JavaScript errors or horizontal overflow. Previews regenerated and visually inspected.
- All twenty-four listing/detail routes checked in the static demo; cart addition and persistence after reload checked across all four source projects.
- Twelve production SSR home/list/detail routes passed independently across all four projects.
- Concept Set A layout 03 product columns constrained to their available width; desktop and mobile checked again after the fix.
- Gallery filters passed for Set A (5 layouts) and all layouts (12).
- Original project hashes checked: 673 files unchanged.
- Seller screenshots, English listing copy and buyer documentation refreshed for this release. Release ZIP integrity and excluded development folders checked by the packaging script.

These checks cover the template preview and English copy. They do not certify a production payment system or WCAG compliance. Commerce integrations use mock data and browser state.
