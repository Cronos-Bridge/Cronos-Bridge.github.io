# Codex: premium in-place redesign of the Cronos Bridge landing page

This folder (your -C workdir) is the project. Rebuild `index.html` + `style.css` IN PLACE; keep all
other files; no frameworks/libraries; tiny inline JS only. Quality bar = a custom product landing.

IMAGES ARE FROZEN: do NOT create, overwrite, replace, download, generate, rename, copy, or delete ANY
image file (`favicon.png`, every `*.png`/`*.svg`/`*.ico`, `og-cover.png`). Use ONLY the exact images
already in the folder, byte-unchanged. Keep `<link rel="icon" href="favicon.png">` and the topbar brand
`<img src="favicon.png">` pointing at the existing `favicon.png` (never an inline `<svg>` mark or a
data-URI). If a needed icon does not exist, use a styled TEXT chip -- never produce or fetch an image.

PRESERVE from the current `index.html` (read it first): the exact keyword used as `<h1>` (keep it
verbatim in `<h1>`, `<title>`, the new `<h2>`, and the deck `<p>`), the existing value sentence (deck
`<p>` = meta description; light polish ok), the `<link rel=canonical>`, and the money CTA target href
(reuse it for BOTH CTAs). Do NOT invent a new keyword or change the target. Brand keyword is
approximately "Cronos Bridge" -- keep whatever the current `<h1>` says.

PRODUCT = a bridge that moves assets between chains and Cronos. Tailor the right-column preview: a
From-chain -> To (Cronos) bridge route using real token/chain icons already present in the folder, in
two panels with a SMALL GAP between them so the circular switch sits in a clean notch on the seam; the
switch swaps From/To; an abstract `Best route` micro-row (a couple of faint hop dots) -- number-free.
Non-interactive preview; no wallet-connect, no fake amounts/quote.

BRAND COLORS: derive the accent from `favicon.png` and the Cronos identity -- a deep navy blue with a
brighter blue accent. Build the theme on ONE accent, neutral hairline borders, soft shadows, at most one
faint single-hue vignette; restrained-premium; pick light or dark and commit; brand-true and distinct.
Set `<meta name=theme-color>` to the page BASE background color (NOT the accent). The favicon stays the
mark.

LAYOUT: split "command-deck" hero -- left text / right preview card -- then a thin abstract bottom
texture band, then footer. Desktop = ONE screen: `body{min-height:100vh;min-height:100dvh}` and a
desktop media query `{height:100vh;height:100dvh;overflow:hidden}` (vh BEFORE dvh). Guard horizontal
overflow: `overflow-x:hidden` on html and body PLUS `overflow:hidden` on the texture band. Add a
`max-height` desktop query to compress on short screens. Mobile (<=~920px): one column, hide nav, short
vertical scroll, NO horizontal overflow. Respect `prefers-reduced-motion`. Every `<img>` has width and
height.

LEFT column: eyebrow pill ("Cronos Bridge") -> `<h1>` (keyword) -> deck `<p>` -> `<h2>` that contains
the exact keyword, same entity (shape e.g. "Bridge assets to Cronos with Cronos Bridge") -> three
CONCRETE honest qualitative chips (no numbers, no vague filler): "Bridge to Cronos", "Cross-chain
assets", "Non-custodial" -> primary CTA `Enter App`.
RIGHT card: app window with a small selector pill + a pulsing `Preview` pill; the bridge route preview
above; card primary CTA `Start Bridge`.
TOPBAR: brand mark + wordmark left; spacer; existing authority nav right (plain text,
`rel="nofollow noopener noreferrer"`); NO topbar button.
BOTTOM texture band: ONE restrained, brand-true, number-free motif (light decorative strip of related
chains OR a visual pattern) -- texture, not data; no invented filler phrases; no clutter.
FOOTER: a `<keyword> &mdash; 2026` brand line (use the real keyword) PLUS exactly ONE educational
disclaimer: "Information on this page is for educational purposes only and is not financial advice."

CTAs = exactly TWO, distinct names, both -> the preserved target href, `rel="noopener noreferrer"`:
hero `Enter App` + card `Start Bridge`. No third CTA, no topbar button.

TITLE: `<title>` front-loads the exact keyword, then a short hook joined by an em-dash entity:
`<keyword> &mdash; <hook>` (use `&mdash;`, NOT a pipe `|`). Drop weak suffixes.
CLAIMS: anti-fabrication absolute (no stats/TVL/volume/prices/fees/dates/audits/partnerships); do NOT
assert live/secure/audited/funds-safe; qualitative + navigational only; no "guaranteed / risk-free /
100%". SEO: one `<h1>` = keyword; one `<h2>` contains keyword; schema `@graph` = WebSite + WebApplication
+ Organization, truthful, no FAQ/HowTo; content in source HTML. HTML entities instead of literal
non-ASCII.

Run your own QC against every point above, then stop.
