# Lama Lama exact component/class crawler

This read-only Playwright crawler complements the curated workbook by extracting the exact rendered DOM class vocabulary from `lamalama.com`.

## Run

```bash
mkdir lamalama-audit
cd lamalama-audit
npm init -y
npm install playwright
npx playwright install chromium
cp /path/to/crawl-lamalama-components.mjs .
node crawl-lamalama-components.mjs
```

The script follows internal public links, renders each page at desktop and mobile sizes, scrolls to trigger lazy content, opens a conservative allow-list of non-submitting controls, records class mutations, and scans same-origin CSS/JavaScript resources for dormant component hooks.

## Main outputs

- `class-tokens.csv`: every unique class token, human-friendly name, classification, occurrence count, pages, viewports, phases, tags, and evidence source.
- `class-combinations.csv`: every unique complete `class="…"` signature.
- `custom-class-catalog.csv`: project, state, CMS, and other custom classes separated from Tailwind-style utilities.
- `elements.csv`: element-level DOM inventory with text examples, attributes, and stable CSS paths.
- `interactions.csv`: safe interaction attempts and results.
- `class-mutations.csv`: class additions/removals during interaction states.
- `resources.csv`: same-origin CSS/JavaScript resources and token counts.
- `component-catalog.md`: automatically humanized catalog.
- `snapshots/*.html`: rendered DOM snapshots for manual verification.
- `pages.json`: crawl coverage and status metadata.

## Useful options

```bash
MAX_PAGES=400 MAX_DEPTH=10 INTERACTION_LIMIT=40 node crawl-lamalama-components.mjs
HEADLESS=false node crawl-lamalama-components.mjs
OUTPUT_DIR=./my-output node crawl-lamalama-components.mjs
CRAWL_DELAY_MS=800 NAVIGATION_TIMEOUT_MS=60000 node crawl-lamalama-components.mjs
```

## Safety boundary

The crawler deliberately excludes admin/login/API paths, cart/checkout/account paths, third-party iframe contents, and external navigation. It does not fill or submit forms. Controls with `type="submit"` and action text such as purchase, pay, delete, send, or subscribe are skipped.
