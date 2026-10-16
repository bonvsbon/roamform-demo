# Start here

Thank you for choosing ROAMFORM Storefront Collection.

Your purchase includes all twelve layouts in this version. The layouts are organized into four independent projects, not twelve separate applications. Concept Set A and Concept Set B each share their catalog and components across five layouts.

## Requirements

Use Node.js 22 or 24 LTS and npm. This release was built and checked with Node.js 24.19.0. Install dependencies with internet access. Vue/Nuxt development knowledge is recommended. Windows users can run the standard dev/build commands from PowerShell; the optional `demo` npm command uses POSIX environment syntax, so set `ROAM_DEMO=1` in your shell before `npx nuxt generate`.

## Install one storefront

Copy the project you want from `source/` into your working directory. Open a terminal in that project's directory:

```sh
npm ci
npm run dev
```

Open the local URL printed by Nuxt. For either concept collection, visit `/concept-01`, `/concept-02`, `/concept-03`, `/concept-04` or `/concept-05`. The concept layouts are variations of a shared project, so updating its catalog updates all five.

## Build and deploy

```sh
npm run typecheck
npm run build
node .output/server/index.mjs
```

Deploy `.output/` to a Node-compatible hosting service. Consult the installed Nuxt version's hosting documentation for platform-specific deployment. This source build uses normal routes and defaults to `/`. Set `DEMO_BASE` only if you intentionally deploy under a subdirectory and update your asset path handling accordingly.

The included `demo/` is a static, hash-routed preview. Serve it over HTTP, not by double-clicking its files. Upload the contents of the public-demo ZIP to a static host to share the complete gallery. Do not upload the buyer/source ZIP to a public demo host.

## Edit your brand and catalog

| Project | Product data | Home content | Colors/type |
| --- | --- | --- | --- |
| Everyday A | `data/products.ts` | `data/homepage.ts`, `data/site.ts` | `assets/css/main.css`, `tailwind.config.ts` |
| Everyday B | `mock/products.ts` | `data/homepage.ts`, `data/site.ts` | `assets/css/main.css` |
| Concept Set A | `data/catalog.ts` | `data/home/c01.ts` through `c05.ts`, `data/content.ts` | `.theme-c01` through `.theme-c05` in `assets/css/main.css` |
| Concept Set B | `data/products.ts` | `data/concepts.ts` | concept selectors in `assets/css/main.css` |

Change the ROAMFORM wordmark components, favicon, titles and meta descriptions. Replace image files under `public/images/`; update source paths and alt text if filenames or subjects change. Font definitions are in `assets/css/local-fonts.css`; keep included license notices when redistributing fonts.

Catalog mapping at the end of each product data file sets the demo's signature colors, images, codes and prices. Edit that mapping or remove it and edit the records directly for a real catalog. Do not retain both an old mapping and new record values that it overrides.

Prices, reviews, availability, store addresses and product benefits are fictional examples. Replace them with your own verified data. DEMO FOAM is a descriptive demo material label. All specifications, comparisons and reviews are illustrative, not certified technology or laboratory results.

Development used Claude Code and Codex; demo photos are AI-generated.

## Language and regional settings

All twelve layouts and supporting pages use English copy, including filters, forms, dialogs, accessibility labels, editorial content and store data. Document language and date/number formatting use English. Demo prices remain in Thai baht (THB) and sample store locations remain in Thailand; edit those separately for your target market. Some legacy content field names such as `th`, `thai` and `labelTh` are retained for schema compatibility, but their values are English.

## What works locally

Product browsing, layout switching and the demonstrated filter/search/cart/wishlist flows use sample data and browser state. Features vary by project. Everyday B and Concept Set B include a local content studio; it edits preview content and exports JSON, not a hosted CMS. Product previews reuse a single angle per sample model, not a complete product photography set.

## Connect before taking real orders

Implement server-side prices/stock validation, authentication, payment processing, order creation, transactional email and durable storage. Replace mock account/checkout behavior. Add your own privacy and store policies. Store locator and social links are sample UI. The demo does not charge customers or send orders, and it must not be advertised as having these services already integrated.

## Troubleshooting

If styles or fonts are missing, confirm you installed dependencies in the correct project and serve the demo over HTTP. If local preview edits persist, clear the ROAMFORM keys in browser local storage. If a port is occupied, run `npm run dev -- --port 3010`. For a clean rebuild, remove only the selected project's generated `.nuxt` and `.output` directories and rerun the build.

## License and support

Read `LICENSE.txt` and `THIRD-PARTY-NOTICES.md`. Your marketplace purchase terms may take precedence. The included release is v1.0.2. No lifetime updates, hosting or custom integration services are included. Ask the seller through the purchase channel for reproducible template bugs and installation questions; the seller's published support/refund policy governs that service.
