---
brand_id: hulei_jyu
kind: brand
summary: University of Jyväskylä academic talks by Presenter Name — lab meetings, journal clubs, conference talks, thesis defenses
primary_color: "#002957"
---

# Presenter Name · University of Jyväskylä Brand Specification

> Identity-only preset. No SVG page roster — pages are composed freely under these constraints.

## I. Brand Overview
| Property | Value |
|---|---|
| Brand Name | Presenter Name · University of Jyväskylä |
| Use Cases | Lab meetings, journal clubs, conference talks, thesis (pre-)defenses |
| Tone | Calm, academic, restrained |
| Sources | Theme colors and fonts of the author's JYU PowerPoint deck; bundled JYU and InterLearn logo files |

## II. Color Scheme
| Role | HEX | Provenance | Use |
|---|---|---|---|
| primary | #002957 | fact | Dark structural pages; titles on light pages |
| accent | #F1563F | fact | Section numbers, the contrasted condition, pointers |
| secondary | #C29A5B | fact | Thin rules and small labels on dark pages |
| neutral | #C7C9C8 | fact | Dividers; secondary text on dark pages |
| surface | #EFEFEF | fact | Card / panel fill when a card is used |
| muted | #8094AB | fact | Source lines and non-essential meta information |
| text | #1A1A1A | approx | Main text on light backgrounds |
| on_dark | #FFFFFF | approx | Main text on dark backgrounds |

- Main text uses `text` on light and `on_dark` on dark backgrounds; titles may use `primary` on light pages.
- `muted` is for sources and non-essential meta information only — never for claims, condition names or explanations. Judge every text colour by its contrast against the actual background.

## III. Typography
| Role | Family | Weight |
|---|---|---|
| title | Aleo, Georgia, serif | 700 |
| body | Lato, Microsoft YaHei, Arial, sans-serif | 400 / 700 |

Aleo and Lato are installed on the author's machine. When unavailable, use the listed fallbacks and check line breaks, overflow and glyph coverage after export.

## IV. Logo
| File | Background |
|---|---|
| ../images/jyu_logo_vertical_white.svg | Dark |
| ../images/jyu_logo_horizontal_white.svg | Dark |
| ../images/jyu_torch_navy.svg | Light (compact mark) |
| ../images/jyu_torch_slate.svg | Dark (large, low-contrast mark) |
| ../images/interlearn_logo.png | Either (partner logo) |

- White marks on dark backgrounds, the navy mark on light backgrounds; keep original proportions and clear space.
- Whether and where a mark appears follows the page's content and hierarchy; no fixed corner, per-page stamp or mandatory watermark.
- Use the InterLearn logo only when the talk relates to InterLearn or the user asks for it.
- Available brand line: "JYU SINCE 1863." — optional, not a mandatory footer.

## V. Voice & Tone
- Formality: formal (academic)
- Person: none by default — use "we" only for the presenter's own work; for other authors' studies write "the authors" / "the study" and keep the original attribution
- Emoji: forbidden
- Abbreviations: spell-out-first

## VI. Icon Style
- Preference: linear

## VII. Visual Assets
The five logo files listed in §IV, stored in `../images/`.
