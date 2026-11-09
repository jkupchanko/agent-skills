# Brand system

## Evidence and precedence

The November 2026 Couchbase homepage, AI Data Plane page and Database TCO calculator were inspected in-browser, including computed styles and selected states. These values are a dated reference, not a promise of permanent official branding. If exact current website parity is requested, remeasure the live reference and record differences; do not silently replace John's approved preferences.

## Color roles

| Role | Light | Dark | Authority |
|---|---|---|---|
| Primary action | #EC1218 | #EC1218 | Measured TCO |
| Primary hover / pressed | #7C0206 / #560003 | same | Measured TCO |
| Hero / savings highlight | #FFF0DA | #FFF0DA | Brand color; placement preference |
| Hero ink / supporting text | #211E19 / #655747 | same | Approved demo |
| Canvas | #FFFFFF | #000000 | Approved demo |
| Card | #FFFFFF | #242424 | Approved demo |
| Control surface | cream or white | #303030 | Approved demo |
| Selected dark control | — | #3B3B3B | Approved demo |
| Main text | #181818 | #F5F5F5 | Approved demo |
| Supporting text | #595953 | #C5C5C5 | Approved demo |
| Dividers | #DEDDD8 | #444444 | Approved demo |
| Input edge | #AAA89F | #777777 | Approved demo |
| Selected checkbox | #21EA2A | #21EA2A | Measured TCO |
| Decorative accent | #547D91 | #789AAA | Personal design preference, not official |

Use red for action and limited selection emphasis, green for selected workload checks, cream for hero/result surfaces, and steel blue only for background art. No decorative accent on text or cost panels by default. In dark mode use neutral selected-card borders (#777/#999); red outlines are appropriate for edit buttons, not every panel. Validate rendered contrast rather than assuming a named brand color passes every use.

## Typography

- Heading/workload labels: **Centra No2 Medium**, weight 500. Inputs also use Centra No2 500 at 16px.
- Body/supporting copy: **Inter**, usually 400; actions 500 and presets 700. Explicitly verify font loading; a fallback is not an exact match.
- Reference fluid scale: h1 32–48px, h2 24–32px, section titles 18–24px. Heading line heights roughly 1.08–1.25; body 1.5. Letter spacing around -0.02em for headings only.
- Essential body and control text generally 16px. Secondary labels may be 14–15px with adequate contrast. Fix density and wording before scaling text up.
- Amounts use tabular numerals, wrapping only at sensible boundaries. Do not shrink the entire estimate to avoid overflow.

## Assets

Bundled: `assets/couchbase-logo.svg` for light surfaces; `assets/couchbase-logo-dark.svg` for dark surfaces; `assets/couchbase-favicon.svg` for the browser tab.

Preserve logo geometry, aspect ratio, red symbol and clear space. Link the top-left brand to https://www.couchbase.com/ in standalone demos. The dark wordmark is a local color variant with unchanged geometry. The favicon is the official couch symbol extracted from the wordmark, not a new logo. Test it at tab size and verify the served URL.

Do not regenerate the logo through image generation or substitute an emoji. For authorized Couchbase work use these existing assets; their inclusion is not a new trademark or redistribution license.

Centra source observed: https://www.couchbase.com/wp-content/themes/couchbase-com-2026/assets/fonts/CentraNo2/Medium/CentraNo2-Medium.woff2 . The calculator has a licensed-use-context asset already; this skill deliberately does not redistribute the proprietary font. Reuse the project's approved font or a permitted official asset. State a fallback when that resource is unavailable. Inter must likewise be loaded explicitly through an approved local or remote source.
