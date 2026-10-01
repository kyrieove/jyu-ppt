---
name: jyu-ppt
description: One-shot PPT from a research paper (PDF/DOCX): "$jyu-ppt <paper path>" (Codex) or "/jyu-ppt <paper path>" (Claude Code / ZCode) — turn it directly into an English University of Jyväskylä (JYU) academic PPTX with speaker notes, using the bundled ppt-master (quick-generate), brand hulei_jyu, frame deck hulei_jyu_frame and visual style jyu-academic. No confirmation stops after one-time first-run setup.
---

# jyu-ppt

`<skill>` below means the folder that contains this SKILL.md; resolve it to an absolute path first. The bundled ppt-master lives in `<skill>/ppt-master`.

**State files.** `profile.md` and `.deps_ok` live in the skill folder. If the skill folder is read-only, keep them in `~/.jyu-ppt/` instead and check that folder first on every later run.

## Step 0 — first run only

1. **Presenter profile.** If there is no `profile.md` yet, ask the user three questions in one message, then write the answers to `profile.md` in this form and continue:
   ```
   name: <presenter name shown on covers>
   affiliation: <affiliation line>
   interlearn_logo: yes | no
   ```
   (`interlearn_logo`: yes only for members of InterLearn, the Centre of Excellence in Learning Dynamics and Intervention Research.) On later runs read the file and do not ask again.
2. **Dependencies.** If there is no `.deps_ok` yet, run `python -m pip install -r <skill>/ppt-master/requirements.txt` (ask for network permission if the sandbox requires it). When it succeeds, create the empty marker file `.deps_ok`.

## Step 1 — make the deck (no stops)

Run the `ppt-master` skill at `<skill>/ppt-master/SKILL.md` end to end with the **quick-generate** profile (`<skill>/ppt-master/workflows/profiles/quick-generate.md`): no Strategist, no confirmation pages, no approval stops — decide every unspecified choice yourself and continue through the final checker to the exported PPTX.

- Source file: the `<path>` the user gave. If none was given, ask for it.
- Output: an English presentation, 16:9.
- Brand workspace root (install it directly as the one Brand root for this run): `<skill>/ppt-master/templates/brands/hulei_jyu`
- Deck workspace root (install it directly as the one Deck root for this run): `<skill>/ppt-master/templates/decks/hulei_jyu_frame` — a 4-page frame. Build the cover from `01_cover`, section dividers from `02_chapter`, every content page from `03_content` (keep its kicker, title, rule and footer exactly; the content area is empty and composed freely per the visual style), and the last page from `04_ending`.
- Visual style: before writing the first slide, read `<skill>/ppt-master/references/visual-styles/jyu-academic.md` in full, then open the reference pages in `<skill>/ppt-master/references/visual-styles/jyu-academic-examples/` and keep their visual language (type sizes, colours, rules, card and table treatment, footer, cover) on every page. Plan the pages from this paper's own structure and compose each page for its content.
- Enable speaker notes; put explanations and statistical detail there, as the style asks.
- Presenter shown on the cover: `name` — `affiliation` from `profile.md`. The paper's authors are source information, not the presenter. If `interlearn_logo` is `no`, leave the cover's partner-logo slot out.

## Don't

- Don't add content prototypes beyond the 4-page frame (`01_cover`, `02_chapter`, `03_content`, `04_ending`).
- Don't copy the jyu-academic example pages' content, page count, section order or page-by-page compositions — they define the visual language, not this deck's structure.
- Don't substitute another visual style, and don't reuse layouts from other projects in the workspace.
- Don't add talk-type or event labels (e.g. "Journal club") or dates that are not given here.

## If something fails

- **Source path missing or not a file** → stop and ask the user for the correct path; never substitute a different paper.
- **`pip install` fails** (no network / no permission) → report the exact error and stop; do not run ppt-master without its dependencies.
- **The final checker fails** → fix what it names and rerun the checker once; if it still fails, report the failing items — never report an unchecked PPTX as done.
- **`<skill>/ppt-master` or a referenced template/style file is missing** → the install is broken; tell the user to re-clone https://github.com/kyrieove/jyu-ppt rather than improvising substitutes.

Do not pause until the PPTX exists, then report its path — the sanctioned stops are Step 0's first-run questions, a missing source path, and the failure cases above.
