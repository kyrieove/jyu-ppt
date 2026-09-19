# Visual style: jyu-academic

Evidence-led academic talk in the University of Jyväskylä identity. This style is defined by a **reference deck**: reproduce its visual language on every new deck. Its text is placeholder ("Page title stating the claim", "Body text lorem ipsum", zeroed numbers) — take nothing from it but the page structure.

**Reference deck (read before writing the first slide):** `./jyu-academic-examples/*.svg` — 23 pages: cover, roadmap, theory, research questions, methods, results with figures, synthesis, conclusions, ending (01–16), plus further compositions (17–23): a light in-flow question page, a 2×2 figure grid with row labels, a definition block (labelled fields beside a figure), a text-only framework in columns, three figures in a row with a shared legend, a staggered trial sequence, and key references. Take from them the fixed grammar: header, footer, margins, type sizes, colours, rules, card and table treatment, caption style. Their content-area compositions are samples of what suits this style, not a menu to fill: compose each page for its own content, and reuse a reference composition only when the content really has the same shape. Page count, section order and pages per section come from the source paper, not from the reference deck — papers differ in structure and length. Image files referenced inside the examples (`figure_N.jpeg`, logos) are not bundled; each `figure_N` frame marks where a paper figure sits.

---

## 1. Shape & decoration

- Content pages, top to bottom: small uppercase kicker (section · topic) at y≈56 → title at y≈92, one or two lines → full-width thin grey rule at y≈146 → content zone from y≈180 → footer at y≈700. Margins 48 px left and right; content width 1184 px.
- Compositions that suit this style (examples, not a closed list — invent others when the content calls for it): two columns (text | figure, or two contrasted panels); a figure on the right with numbered findings on the left; two to four figures in a grid with small captions; a row of 3–4 bordered cards (conditions, stages, conclusions); a table with a takeaway column; a horizontal procedure flow of boxes with small arrows; a numbered roadmap with 4 columns.
- Open layout is the default: text sits directly on white, grouped by subheadings, whitespace and thin rules, next to figures or native diagrams. Cards and takeaway bars are occasional tools, not the page's container — when most pages wrap their text in boxes, every page looks the same and nothing stands out (the main complaint about earlier decks).
- Use a card when the content is a few parallel units that are compared side by side (conditions, stages, hypotheses). Cards are outlined, not grey slabs: light fill (`surface`), 1.5 px primary-colour border, small corner radius; the contrasted item uses a pale accent tint with an accent border.
- A full-width primary-colour bar with white text is for the few pages whose one conclusion must stand out (typically a results synthesis or the conclusions); elsewhere a bold line of body text carries the takeaway.
- Before export, look at the deck as a whole: if boxes or bars appear on most content pages, rework some of those pages into open layouts.
- Decoration is minimal: thin rules, small gold rules on dark pages, small arrows. No gradients, shadows or badges; never alter colour scales or shading inside scientific figures.
- Cover and ending: primary-colour field, one centred vertical axis — vertical white JYU logo at the top, short gold rule, title, subtitle, presenter block — with the coral / gold / grey strip along the bottom edge (each segment 320 px wide, starting at x=320). The ending page repeats the same frame with "Thank You" and a short line inviting questions.

## 2. Typography character

- Titles: brand serif (Aleo), bold, primary colour, 34 px; usually two lines stating the page's claim.
- Kicker: brand sans (Lato), 14 px, bold, accent colour, uppercase with wide letter-spacing, e.g. "RESULTS · MAIN EFFECT".
- Subheadings inside content: serif bold 22–24 px in primary colour; the contrasted side in accent colour.
- Body: sans 16–18 px in the dark text colour; short bullet lines, not paragraphs. If a page's content only fits below 16 px, move detail to the speaker notes or split the page instead of shrinking type or boxing it. Key phrases in bold primary or bold accent. Numbered findings ("1. Main effect of condition:") in bold.
- Figure captions: 11–12 px muted colour directly under the figure, one or two lines ("Fig. 2: Mean accuracy by group and condition …").
- Footer (content pages): 14 px muted colour — left: page number, then the source for this page ("Author et al. (Year) · Section 3.2 (Figs. 2 & 3)"); right-aligned: "JYU SINCE 1863."
- Cover (all centred on x=640): vertical white logo at y≈44 (≈187×121), gold rule 80×3 at y≈186, title 38 px bold white serif from y≈246 (up to three lines), subtitle 26 px white, presenter 24 px bold white at y≈474, affiliation 18 px light grey at y≈536, paper citation 14 px muted at y≈618.
- Summarise and rewrite the source faithfully; never invent research facts, statistics or identities.

## 3. Using the deck's colors

- Content pages are white. Primary for titles, subheadings, card borders and takeaway bars; accent for kickers, the contrasted condition and warnings; gold only for thin rules and small labels; muted for captions and footers.
- Keep condition colours stable across the deck (e.g. High = primary, Low = accent).

> Specific colour values come from the brand; this style defines colour roles only.

## 4. Texture / elevation

Flat. Thin borders (1–1.5 px), small corner radius (≈4 px), no shadows.

## 5. Figures & evidence

- Paper figures sit on white, unframed, at their own aspect ratio, usually in the right half or as a 2×2 grid; the left column carries numbered findings with the statistics (F, p, η²).
- Tables are drawn natively: primary-colour header row with white text, light banding, the key row highlighted with a pale accent tint and accent text.
- Every claim maps onto the evidence shown and keeps the study's qualifiers; do not turn correlation into causation or a non-significant result into "no effect".

## 6. Paired image-rendering

`minimalist-swiss` — if AI images are ever used, keep them quiet and diagrammatic.

## 7. Illustration propensity

**sparse** — paper figures and simple native diagrams (boxes and arrows for models, paradigms and flows) are the visuals; no decorative illustrations.

## 8. Identity and labels

- Cover: presenter block is the presenter's name (bold) and affiliation from the skill's `profile.md`; the paper's authors, year and journal go on the one smaller citation line; InterLearn logo at the bottom right only if the presenter profile asks for it — as in `01_cover.svg`.
- Never add talk-type, event or date labels ("Journal club", a month) unless the user supplied them — also not in the footer, the ending page or speaker notes.
