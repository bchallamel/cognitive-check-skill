# Cognitive Check Report Rendering

Use this reference when the user asks to turn a cognitive-check output into an HTML report, a PDF report, or a reusable visual report format.

## Two-Stage Output

Generate reports in two stages:

1. A self-contained HTML report for interactive review.
2. A polished PDF report generated from the same report data with a dedicated PDF composition renderer.

Use one semantic report data model for both. Do not make the PDF a screenshot of the active HTML tab, and do not rely on the interactive HTML print stylesheet for publication-ready documents unless the user only needs a quick draft.

## HTML Report

Create a single standalone `.html` file with inline CSS and minimal vanilla JavaScript unless the user asks for a framework.

Required structure:

- Top app bar with title, trust stance, generated date, and actions.
- Stable overview dashboard that always appears before the tabs.
- Primary tabs: `Overview`, `Claims`, `Reasoning`, `Upgrades`.
- More menu tabs: `Explorative Sources`, `Alternatives`, `Assumptions`, `Calibration`, `Appendix`.
- Tab panels with one visible panel in screen mode.
- Print stylesheet that shows all panels in PDF mode.

HTML actions:

- Copy overview as Markdown.
- Copy current tab as Markdown.
- Copy claim table as Markdown or CSV when present.
- Export report JSON when a structured object is available.
- Print/save PDF.

Use lucide icons for action buttons, section headers, status chips, tabs, and menu items. In app/framework contexts, import from the `lucide` or `lucide-react` package. For standalone HTML, inline the required lucide SVGs with `stroke="currentColor"`, `stroke-width="2"`, `stroke-linecap="round"`, and `stroke-linejoin="round"` so the report remains portable.

## Visual Style

Use a quiet, Material-inspired editorial style matching the approved visual direction:

- Portrait-first layout for both HTML and PDF previews.
- Black, gray, white, and blue should dominate.
- Use blue gradients only for intentional emphasis, such as the primary trust stance card or PDF cover band.
- Avoid multicolor status palettes; use blue intensity, labels, icons, and dot counts instead of green/red/amber status coding.
- 8px radius for cards and table containers.
- Soft borders over heavy shadows.
- Generous whitespace, clear section rhythm, and strong alignment.
- No decorative blobs, oversized hero sections, or marketing-style composition.

Suggested palette:

- Ink: `#1F2937`
- Muted text: `#64748B`
- Surface: `#FFFFFF`
- Subtle surface: `#F8FAFC`
- Border: `#E2E8F0`
- Primary: `#2563EB`
- Deep navy: `#0F172A`
- Pale blue: `#EFF6FF`
- Blue gradient: `linear-gradient(135deg, #1D4ED8, #60A5FA)`
- Neutral/unknown: `#64748B`

## PDF Report

Generate publication-ready PDFs with a dedicated PDF composition HTML file unless the user only asks for a quick browser print.

The PDF must use a publication flow, not the interactive tab layout. Avoid one-tab-per-page exports. The PDF composition should use explicit pages, internal headers/footers, and deliberately arranged sections so pages feel filled and intentional.

Preferred architecture:

- `report.html`: interactive tabbed review surface.
- `report-pdf.html`: dedicated PDF composition surface using the same report data.
- `report.pdf`: exported from `report-pdf.html` with browser headers and footers disabled.

PDF export must use headless Chrome with `--no-pdf-header-footer` or equivalent. Browser-generated URL/date/page headers are not acceptable in the final PDF.

Print behavior:

- Hide interactive controls, tab buttons, and More menu controls.
- Do not show tab panels directly; map report sections into composed pages.
- Add a compact cover block or cover band.
- Add a table of contents for reports longer than 6 pages.
- Add designed internal footers with report title, date, and page number.
- Repeat table headers where possible.
- Avoid splitting important cards, matrix rows, and assumption entries across pages.
- Pair color chips with text labels so black-and-white output remains legible.
- Use dense print-specific spacing: smaller dashboard cards, tighter panel padding, compact tables, and two-column grids when legible.
- Do not force every major report section onto its own page; reserve forced page breaks for intentionally composed pages.
- Rebalance page count to content volume. Short reports may need 2 designed pages; longer reports may need 3-6 pages. Empty lower-page whitespace is a layout failure, not a luxury margin.

Recommended PDF order:

1. Cover and cognitive dashboard
2. Key findings
3. Claim validation
4. Argument map
5. Evidence and source audit
6. Cognitive diagnostic
7. Explorative sources
8. Alternative hypotheses
9. Assumption ledger
10. Calibration and change conditions
11. Upgrade plan
12. Appendix and citations

## Visual Verification

When a PDF verification skill is available, follow its workflow. Otherwise use the same sequence directly:

1. Generate the PDF.
2. Render pages to PNG with `pdftoppm` when available.
3. Inspect rendered pages for clipping, overlaps, broken tables, unreadable text, weak contrast, and awkward page breaks.
4. Iterate until the rendered pages are clean.

## Accessibility

- Use ARIA roles for tabs and tab panels.
- Keep tab labels short and meaningful.
- Do not rely on color alone; pair colors with labels or icons.
- Use readable body text for screen and print.
- Use horizontal scroll for wide tables in screen mode and simplified layout in print mode.
- Include plain-language summaries before dense tables.
