---
deck_id: hulei_jyu_frame
kind: deck
category: brand
summary: JYU frame for Presenter Name's academic talks — fixed cover, section, content header/footer and ending; content area composed freely with visual style jyu-academic.
keywords: [academic, JYU, frame, research-talk]
primary_color: "#002957"
canvas_format: ppt169
canvas_width: 1280
canvas_height: 720
canvas_viewbox: "0 0 1280 720"
source_canvas_width: 1280
source_canvas_height: 720
source_viewbox: "0 0 1280 720"
replication_mode: standard
native_structure_mode: structured
page_count: 4
placeholders:
  01_cover: ["{{TITLE}}", "{{SUBTITLE}}", "{{AUTHOR}}", "{{AFFILIATION}}", "{{SOURCE}}"]
  02_chapter: ["{{CHAPTER_NUM}}", "{{CHAPTER_TITLE}}", "{{CHAPTER_DESC}}"]
  03_content: ["{{SECTION_NAME}}", "{{PAGE_TITLE}}", "{{SOURCE}}", "{{PAGE_NUM}}"]
  04_ending: ["{{THANK_YOU}}", "{{ENDING_SUBTITLE}}", "{{AUTHOR}}", "{{AFFILIATION}}"]
---

# Presenter Name · JYU Frame — Design Specification

## I. Template Overview

| Application context | Definition |
|---|---|
| Recurring presentation family | Presenter Name's research talks at the University of Jyväskylä: paper presentations, lab meetings, conference talks, defenses |
| Intended audiences and outcomes | Supervisors, lab members and academic audiences who follow a spoken, evidence-led argument |
| Delivery and reading assumptions | Presented live; explanations and statistical detail go to speaker notes |
| Representative narrative/page roles | Cover, section dividers, content pages, ending |

- This deck is a **frame only**: it fixes the cover, section, content header/footer and ending. The content area of `03_content` (y 170–670) is intentionally empty — compose it freely for each page following visual style `jyu-academic` and its reference pages. Use it together with brand `hulei_jyu`.
- Reuse every page from its prototype: all content pages share `03_content`; do not add other content prototypes or boxes around the content area.

## II. Color Scheme

| Role | HEX | Use |
|---|---|---|
| Primary | `#002957` | Dark pages, content titles |
| Accent | `#F1563F` | Kicker, section numbers, strip segment |
| Gold | `#C29A5B` | Gold rules, ending subtitle, strip segment |
| Neutral | `#C7C9C8` | Title rule, affiliation on dark pages, strip segment |
| Muted | `#8094AB` | Footer, cover citation |
| Text | `#1A1A1A` | Body text in the content area |
| White | `#FFFFFF` | Content pages; text on dark pages |

## III. Typography

| Role | Stack | Size |
|---|---|---|
| Titles | `Aleo, Georgia, serif`, bold | Cover 38 px, content 34 px (two lines max), ending 42 px |
| Kicker | `Lato, Microsoft YaHei, Arial, sans-serif`, bold, uppercase, letter-spacing 1.5 | 14 px |
| Cover / ending text | same sans | subtitle 26 px, presenter 24 px bold, affiliation 18 px, citation 14 px |
| Footer | same sans | 14 px |

## IV. Signature Design Elements

- Dark pages: navy field, coral / gold / grey strip along the bottom (320 px segments from x=320), centred vertical white JYU logo and an 80×3 gold rule on cover and ending.
- Content pages: white field, coral uppercase kicker at y≈56, serif title at y≈92, full-width 1 px grey rule at y=146, footer at y≈701 with page number and the page's source on the left and "JYU SINCE 1863." on the right. No logo, bar or other chrome.
- Cover identity: presenter name (default Presenter Name) and affiliation form the identity block; the paper citation is one small line; InterLearn logo bottom-right only if the presenter profile asks for it. Never add talk-type, event or date labels unless the user supplies them.

## V. Page Roster

| File | Master | Layout key / picker name | Role and slots |
|---|---|---|---|
| `01_cover.svg` | `hj_dark` | `cover` / Title Cover | Centred: logo, gold rule, title, subtitle, presenter, affiliation, citation; InterLearn object slot bottom-right |
| `02_chapter.svg` | `hj_dark` | `chapter` / Section Divider | Coral section number, "PART" label, white section title and description, slate torch watermark |
| `03_content.svg` | `hj_light` | `content` / Content Frame | Kicker, title, rule, footer (page number, source, brand line); empty content area |
| `04_ending.svg` | `hj_dark` | `ending` / Thank You | Centred: logo, gold rule, "Thank You", invitation line, presenter and affiliation |

## VI. Assets

| File | Use |
|---|---|
| `images/jyu_logo_vertical_white.svg` | Cover and ending logo |
| `images/jyu_logo_horizontal_white.svg` | Section page logo |
| `images/jyu_torch_slate.svg` | Section page watermark |
| `images/interlearn_logo.png` | Cover partner logo |

## VII. Placeholder Overrides

`{{SECTION_NAME}}` is the content-page kicker; `{{SOURCE}}` is the per-page source line in the footer and the citation line on the cover; `{{AFFILIATION}}` is the presenter's affiliation; `{{ENDING_SUBTITLE}}` is the invitation line on the ending page.
