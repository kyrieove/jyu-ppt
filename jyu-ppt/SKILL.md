---
name: jyu-ppt
description: One-shot "$jyu-ppt <paper path>" — turn a research paper (PDF) directly into an English University of Jyväskylä (JYU) academic PPTX with speaker notes, using the bundled ppt-master (quick-generate), brand hulei_jyu, frame deck hulei_jyu_frame and visual style jyu-academic. No confirmation stops.
---

# jyu-ppt

`<skill>` below means the folder that contains this SKILL.md; resolve it to an absolute path first. The bundled ppt-master lives in `<skill>/ppt-master`.

## Step 0 — first run only

1. **Presenter profile.** If `<skill>/profile.md` does not exist, ask the user three questions in one message, then write the answers to `<skill>/profile.md` in this form and continue:
   ```
   name: <presenter name shown on covers>
   affiliation: <affiliation line>
   interlearn_logo: yes | no
   ```
   (`interlearn_logo`: yes only for members of InterLearn, the Centre of Excellence in Learning Dynamics and Intervention Research.) On later runs read the file and do not ask again.
2. **Dependencies.** If `<skill>/.deps_ok` does not exist, run `python -m pip install -r <skill>/ppt-master/requirements.txt` (ask for network permission if the sandbox requires it). When it succeeds, create the empty file `<skill>/.deps_ok`.

## Step 1 — make the deck (no stops)

Run the `ppt-master` skill at `<skill>/ppt-master/SKILL.md` end to end with the **quick-generate** profile (`<skill>/ppt-master/workflows/profiles/quick-generate.md`): no Strategist, no confirmation pages, no approval stops — decide every unspecified choice yourself and continue through the final checker to the exported PPTX.

- Source file: the `<path>` the user gave. If none was given, ask for it.
- Output: an English presentation, 16:9.
- Brand workspace root (install it directly as the one Brand root for this run): `<skill>/ppt-master/templates/brands/hulei_jyu`
- Deck workspace root (install it directly as the one Deck root for this run): `<skill>/ppt-master/templates/decks/hulei_jyu_frame` — a 4-page frame. Build the cover from `01_cover`, section dividers from `02_chapter`, every content page from `03_content` (keep its kicker, title, rule and footer exactly; the content area is empty and composed freely per the visual style), and the last page from `04_ending`. Do not add other content prototypes.
- Visual style: before writing the first slide, read `<skill>/ppt-master/references/visual-styles/jyu-academic.md` in full, then open the reference pages in `<skill>/ppt-master/references/visual-styles/jyu-academic-examples/` and keep their visual language (type sizes, colours, rules, card and table treatment, footer, cover) on every page. Do not copy their content, page count, section order or page-by-page compositions: plan the pages from this paper's own structure and compose each page for its content. Do not substitute another visual style and do not reuse layouts from other projects in the workspace.
- Enable speaker notes; put explanations and statistical detail there, as the style asks.
- Presenter shown on the cover: `name` — `affiliation` from `profile.md`. The paper's authors are source information, not the presenter. If `interlearn_logo` is `no`, leave the cover's partner-logo slot out.
- Do not add talk-type or event labels (e.g. "Journal club") or dates that are not given here.

Do not pause until the PPTX exists, then report its path.
