# ASTRO.org — Style Tile B Design Specification
**For use by:** Claude Code — HTML prototype build  
**Project:** astro.org Redesign  
**Prepared by:** Alley Interactive  
**Date:** April 2026  
**Direction selected:** Style Tile B — "Modern, Energetic, Distinctive"

---

## What Style Tile B is

Style Tile B is the bolder of the two directions presented to the ASTRO team. Where Tile A leans academic and institutional (serif headings, squared shapes, restrained color), Tile B signals a clear visual leap — geometric sans-serif headings at heavy weight, pill-shaped buttons, the brand gradient used actively in heroes and CTAs, and cyan elevated to co-primary alongside ASTRO Blue.

The tagline for this direction: **"We made a significant leap."**

---

## 1. COLOR SYSTEM

### CSS Custom Properties — copy exactly into `:root`

```css
:root {
  /* ── Primary brand ── */
  --color-blue:         #0E4C8C;   /* ASTRO Blue — logo, headings, nav bg, primary CTAs */
  --color-blue-dark:    #0A3A6B;   /* Darker blue — hover states, footer */
  --color-green:        #4E7E3A;   /* ASTRO Green — logo accent, secondary CTAs, success */

  /* ── Accent ── */
  --color-cyan:         #3ABEB6;   /* Strong Cyan — co-primary in Tile B, links, interactive */
  --color-cyan-dark:    #2A9E97;   /* Cyan hover/active state */
  --color-plum:         #C74090;   /* Fuchsia Plum — Speed of Light accent, highlights */

  /* ── Light tint backgrounds ── */
  --color-blue-50:      #E6F0FA;   /* Light blue bg — info cards, selected states */
  --color-cyan-50:      #E3F3EF;   /* Azure Mist — cyan tint bg, callout boxes */
  --color-cyan-25:      #EAF6F5;   /* Mint Cream — lightest cyan bg */
  --color-plum-50:      #F2DDE9;   /* Lavender Veil — pink tint bg */
  --color-green-50:     #E5E8DE;   /* Eggshell Green — subtle green bg */
  --color-ivory:        #FBF5E5;   /* Ivory Mist — warm neutral bg */
  --color-porcelain:    #FFFAF0;   /* Porcelain — near-white warm */

  /* ── Neutrals ── */
  --color-charcoal:     #58595B;   /* Primary body text */
  --color-granite:      #979291;   /* Secondary text, captions, metadata */
  --color-alabaster:    #E5E6E5;   /* Borders, dividers, disabled states */
  --color-white:        #FFFFFF;
  --color-light-bg:     #F4F6F8;   /* Page background alternative */

  /* ── Brand gradient (Tile B signature) ── */
  --gradient-brand: linear-gradient(135deg, #0E4C8C 0%, #00CCBE 55%, #1C9E4B 100%);
  /* Usage: hero sections, CTA banners, feature section backgrounds */
  /* Note: gradient green #1C9E4B differs from logo green #4E7E3A — intentional for vibrancy */

  /* ── Semantic tokens ── */
  --color-text-primary:     var(--color-charcoal);
  --color-text-heading:     var(--color-blue);
  --color-text-link:        var(--color-blue);
  --color-text-link-hover:  var(--color-cyan);
  --color-text-muted:       var(--color-granite);

  --color-bg-page:          var(--color-light-bg);
  --color-bg-surface:       var(--color-white);
  --color-bg-subtle:        var(--color-green-50);

  --color-border-default:   var(--color-alabaster);
  --color-border-focus:     var(--color-cyan);    /* Tile B: cyan focus rings */

  --color-cta-primary-bg:   var(--color-blue);
  --color-cta-primary-text: var(--color-white);
  --color-cta-secondary-bg: var(--color-cyan);
  --color-cta-secondary-text: var(--color-white);
  --color-cta-ghost-border: var(--color-blue);
  --color-cta-ghost-text:   var(--color-blue);

  --color-nav-bg:           var(--color-blue);
  --color-nav-text:         var(--color-white);
  --color-nav-hover:        var(--color-cyan);
  --color-dropdown-bg:      var(--color-white);
  --color-dropdown-border:  var(--color-alabaster);
  --color-dropdown-heading: var(--color-blue);
  --color-dropdown-item:    var(--color-charcoal);
  --color-dropdown-item-hover: var(--color-cyan-50);

  --color-accent:    var(--color-cyan);
  --color-highlight: var(--color-plum);
}
```

### Color usage rules for Tile B

- **ASTRO Blue (#0E4C8C):** Nav bar background, page headings, primary CTA buttons, footer background, card heading text
- **Strong Cyan (#3ABEB6):** Co-primary — links, interactive element accents, icon colors, focus rings, quote card left borders, step number circles, hover states. This is MORE prominent in Tile B than Tile A.
- **Brand gradient:** Hero section backgrounds, large CTA banners, section transition dividers. NOT used on small components.
- **ASTRO Green (#4E7E3A):** Secondary CTAs, success states, category labels for Practice/clinical content
- **Fuchsia Plum (#C74090):** Use sparingly — highlights, badges, Speed of Light related content only
- **Charcoal (#58595B):** All body text
- **Granite (#979291):** Secondary text, timestamps, attributions, helper text
- **Alabaster (#E5E6E5):** All borders and dividers

### WCAG accessibility pairings
- White text ON: Blue ✓, Green ✓, Cyan ✓, Plum ✓, Charcoal ✓
- Dark text ON: Azure Mist ✓, Lavender Veil ✓, Ivory Mist ✓, Alabaster ✓, Porcelain ✓
- ⚠ ASTRO Green on white (#4E7E3A on #FFF) = ~4.7:1 — passes AA for large text (18px+) only. Do NOT use for body-sized text links.

---

## 2. TYPOGRAPHY

### Font stack

```css
/* Load from Google Fonts */
@import url('https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700;800&display=swap');

:root {
  --font-primary: 'DM Sans', system-ui, -apple-system, sans-serif;
  /* DM Sans is the ONLY typeface in Tile B — used for ALL text at all weights */
  /* No serif typeface in Tile B (that is Tile A's distinction) */
}
```

### Type scale

```css
/* Tile B — DM Sans at all levels, heavy weights for headings */

--text-display:     52px / font-weight: 800 / letter-spacing: -0.03em / line-height: 1.1
/* Usage: hero headline only */

--text-h1:          40px / font-weight: 800 / letter-spacing: -0.02em / line-height: 1.15
/* Usage: page titles */

--text-h2:          32px / font-weight: 800 / letter-spacing: -0.02em / line-height: 1.2
/* Usage: section headings */

--text-h3:          24px / font-weight: 700 / letter-spacing: -0.01em / line-height: 1.3
/* Usage: card headings, subsection titles */

--text-h4:          18px / font-weight: 700 / line-height: 1.4
/* Usage: dropdown column headers, sidebar headings */

--text-body-lg:     17px / font-weight: 400 / line-height: 1.7 / max-width: 65ch
/* Usage: lead paragraphs, intro text */

--text-body:        15px / font-weight: 400 / line-height: 1.7 / max-width: 65ch
/* Usage: standard body copy */

--text-body-sm:     14px / font-weight: 400 / line-height: 1.6
/* Usage: card body, secondary descriptions */

--text-ui:          14px / font-weight: 500 / line-height: 1.4
/* Usage: nav items, button labels, form labels */

--text-caption:     13px / font-weight: 400 / line-height: 1.5
/* Usage: captions, attributions, metadata */

--text-label:       11px / font-weight: 700 / letter-spacing: 0.08em / text-transform: uppercase
/* Usage: section labels, category tags, table headers */

--text-nav-primary: 15px / font-weight: 600
/* Primary nav item labels */

--text-nav-dropdown-heading: 11px / font-weight: 700 / letter-spacing: 0.08em / uppercase
/* Dropdown column header labels */

--text-nav-dropdown-item: 14px / font-weight: 400
/* Individual dropdown link items */
```

### Tile B type personality notes
- Headings use DM Sans 800 — heavy, geometric, confident. This signals the "significant visual leap."
- No italics except for quote attributions and editorial callout text
- Large stat numbers (hero stats, data callouts): DM Sans 800, 40–52px, color: var(--color-cyan)
- Letter-spacing negative on large headings only — tightens at display sizes

---

## 3. SPACING & LAYOUT

```css
:root {
  /* ── Border radius — Tile B signature ── */
  --radius-sm:     4px;    /* Tags, badges, table cells */
  --radius-md:     8px;    /* Cards, form inputs, dropdowns */
  --radius-lg:     12px;   /* Feature cards, nav dropdown panel */
  --radius-pill:   999px;  /* BUTTONS — Tile B uses full pill radius on all buttons */
  /* Note: Tile A uses 4px on buttons. Tile B uses pill. This is a key differentiator. */

  /* ── Spacing scale ── */
  --space-1:   4px;
  --space-2:   8px;
  --space-3:   12px;
  --space-4:   16px;
  --space-5:   24px;
  --space-6:   32px;
  --space-7:   48px;
  --space-8:   64px;
  --space-9:   80px;
  --space-10:  96px;

  /* ── Layout ── */
  --container-max:    1280px;
  --container-wide:   1440px;
  --container-narrow: 800px;
  --nav-height:       64px;     /* Primary nav bar height */
  --util-nav-height:  40px;     /* Utility nav bar height */
  --section-padding:  80px 0;   /* Default section vertical padding */
  --card-padding:     28px 24px;
  --nav-dropdown-padding: 32px;
}
```

---

## 4. COMPONENT SPECS

### Navigation bar

```
Structure (top to bottom):
1. Utility nav bar — 40px tall, dark charcoal bg (#58595B), white text 12px/500
2. Primary nav bar — 64px tall, ASTRO Blue bg (#0E4C8C), white text 15px/600
3. Mega menu dropdown — white bg, full-width, appears on hover

Utility nav bar:
- Background: #58595B (charcoal)
- Text: white, 12px, font-weight 500
- Items: Search | For Patients | Speed of Light Foundation | [Become a Member CTA] | [Welcome Back ▾]
- "Become a Member" button: pill shape, background #3ABEB6 (cyan), white text, 12px/700
- Right-aligned group: Become a Member + Welcome Back

Primary nav bar:
- Background: #0E4C8C (ASTRO Blue)
- Logo: horizontal variant (ASTRO wordmark + full name), white reversed, left-aligned
- Nav items: white text, 15px, font-weight 600, spaced with 32px gap
- Active/current item: cyan underline (2px, #3ABEB6), or cyan text color
- Hover: text color transitions to #3ABEB6 (cyan)
- No visible border between nav and page — mega menu adds shadow when open

Mega menu dropdown:
- Background: white (#FFFFFF)
- Full viewport width, positioned below nav bar
- Box shadow: 0 8px 32px rgba(0,0,0,0.10)
- Padding: 40px 80px
- Inner layout: CSS grid with column headers
- Column header: 11px, 700 weight, uppercase, letter-spacing 0.08em, color: #0E4C8C (blue)
- Column items: 14px, 400 weight, color: #58595B (charcoal), 10px vertical padding each
- Item hover: background #E3F3EF (azure mist), color #0E4C8C (blue), border-radius 4px
- Divider between columns: 1px solid #E5E6E5 (alabaster)
- Close on: mouse leave nav area, ESC key, click outside
```

### Buttons (Tile B — ALL pill shaped)

```css
/* Primary button */
.btn-primary {
  background: var(--color-blue);       /* #0E4C8C */
  color: white;
  font: 700 15px 'DM Sans';
  padding: 12px 28px;
  border-radius: 999px;                /* PILL — Tile B signature */
  border: none;
  cursor: pointer;
  transition: background 0.15s;
}
.btn-primary:hover { background: var(--color-blue-dark); /* #0A3A6B */ }

/* Secondary / CTA button */
.btn-secondary {
  background: var(--color-cyan);       /* #3ABEB6 */
  color: white;
  font: 700 15px 'DM Sans';
  padding: 12px 28px;
  border-radius: 999px;
  border: none;
}
.btn-secondary:hover { background: var(--color-cyan-dark); /* #2A9E97 */ }

/* Ghost button */
.btn-ghost {
  background: transparent;
  color: var(--color-blue);
  font: 600 15px 'DM Sans';
  padding: 11px 27px;
  border-radius: 999px;
  border: 1.5px solid var(--color-blue);
}
.btn-ghost:hover { background: var(--color-blue-50); }

/* Small utility button (e.g. Become a Member in util nav) */
.btn-sm {
  padding: 6px 16px;
  font-size: 12px;
  font-weight: 700;
  border-radius: 999px;
}
```

### Cards

```css
/* Standard content card */
.card {
  background: white;
  border-radius: 12px;
  border: 1px solid var(--color-alabaster);  /* #E5E6E5 */
  padding: 28px 24px;
  /* NO drop shadow in default state — Tile B uses border only */
}
.card:hover {
  border-color: var(--color-cyan);           /* Cyan border on hover */
  box-shadow: 0 4px 16px rgba(58,190,182,0.12);
}
.card-heading {
  font: 700 18px 'DM Sans';
  color: var(--color-blue);
  margin-bottom: 8px;
}
.card-body {
  font: 400 14px/1.6 'DM Sans';
  color: var(--color-charcoal);
}

/* Feature card (colored bg) */
.card-feature {
  background: var(--color-blue-50);   /* #E6F0FA */
  border-radius: 12px;
  padding: 28px 24px;
  border: none;
}

/* Stat / metric card */
.card-stat {
  background: rgba(255,255,255,0.08); /* On colored bg */
  border-radius: 8px;
  padding: 28px 24px;
}
.card-stat-num {
  font: 800 32px 'DM Sans';
  color: var(--color-cyan);            /* Cyan numbers — Tile B */
  line-height: 1;
  margin-bottom: 6px;
}
.card-stat-label {
  font: 400 13px 'DM Sans';
  color: white;
  opacity: 0.8;
}
```

### Quote / callout treatment (Tile B)

```css
/* Tile B quote card — cyan left border replaces green quote mark */
.quote-card {
  background: white;
  border-radius: 8px;
  padding: 24px 28px;
  position: relative;
  box-shadow: 0 1px 4px rgba(0,0,0,0.06);
}
.quote-card::before {
  content: '';
  position: absolute;
  left: 0; top: 0; bottom: 0;
  width: 4px;
  background: var(--color-cyan);       /* #3ABEB6 — Tile B signature */
  border-radius: 4px 0 0 4px;
}
/* Tile A uses a green quote mark (Georgia Bold). Tile B uses this cyan border instead. */
```

### Section labels / eyebrow text

```css
.section-label {
  font: 700 11px 'DM Sans';
  letter-spacing: 0.08em;
  text-transform: uppercase;
  color: var(--color-cyan);            /* Cyan labels in Tile B */
  margin-bottom: 12px;
  display: block;
}
```

### Focus ring (accessibility)

```css
:focus-visible {
  outline: 2px solid var(--color-cyan);   /* Cyan focus ring — Tile B */
  outline-offset: 2px;
}
```

---

## 5. HERO / HEADER SECTION

```
Hero treatment (Tile B):
- Background: brand gradient  linear-gradient(135deg, #0E4C8C 0%, #00CCBE 55%, #1C9E4B 100%)
- Heading: DM Sans 800, 52px, white, letter-spacing -0.03em
- Subheading: DM Sans 400, 20-22px, white at 85% opacity
- CTA buttons: pill shape, primary = white text on cyan, secondary = ghost white border
- Min height: 480px desktop, centered or left-aligned content
- Max content width: 700px within container
- No carousel. Static, intentional content only.

Audience pathway cards (homepage above fold):
- 4 cards in a row, replacing the carousel
- Each card: white bg, 12px radius, cyan top border (4px), blue heading, charcoal body
- On hover: cyan border glow, slight lift
- Labels: Radiation Oncologist / Physicist & Dosimetrist / Resident & Student / Practice Administrator
```

---

## 6. NAV-SPECIFIC PROTOTYPE DETAILS

### Desktop mega menu behavior
```
Trigger: hover on L1 nav item (200ms delay before opening)
Close: mouse leaves the combined [nav bar + dropdown] area
Animation: dropdown fades in + slides down 8px (100ms ease-out)
Width: 100vw, aligned to left edge of viewport
Max inner content width: 1280px centered

Column structure inside dropdown:
- Each L2 group = one column
- Column header: uppercase label in ASTRO Blue
- Items listed vertically below header
- Inter-column divider: 1px solid alabaster
- Suggested column count per section:
  - Meetings & Events: 2 columns (Annual Meeting | Events)
  - Practice: 4 columns (Treat Patients | Manage Practice | Improve Quality | Learn & Certify)
  - Publications & News: 3 columns (Journals | Society News | News & Media + Research)
  - Advocacy: 3 columns (Key Issues | Become an Advocate | ASTRO PAC)
  - About & Join: 3 columns (About ASTRO | Membership | Career Pathways + Community)
```

### Mobile navigation
```
Breakpoint: < 768px
Trigger: hamburger icon (top right), 24px, white on blue
Menu style: full-screen overlay, blue background (#0E4C8C)
L1 items: stacked, 18px/700, white, 20px vertical padding, chevron right
Expanded L1: accordion reveals L2 items below
L2 items: 15px/600, cyan color (#3ABEB6), 14px vertical padding
L3 items: 14px/400, white 80% opacity, 10px vertical padding, indented 20px
Close: X button top right, or swipe left
```

---

## 7. HOMEPAGE COMPONENT ORDER

```
1. Utility nav (charcoal bar, 40px)
2. Primary nav (blue bar, 64px)
3. Hero section (gradient bg, audience pathway cards)
4. Quick-access bar (white bg, most common tasks as pill links)
5. Featured content grid (2-3 columns, content cards)
6. Upcoming meetings / events strip (blue bg)
7. Latest from journals + news (2-column editorial layout)
8. Membership CTA banner (gradient bg)
9. Footer (dark charcoal bg, white text)
```

---

## 8. FOOTER

```css
footer {
  background: #0A3A6B;          /* Blue dark */
  color: white;
  padding: 64px 0 32px;
}
footer a {
  color: rgba(255,255,255,0.75);
  font-size: 14px;
  text-decoration: none;
}
footer a:hover { color: var(--color-cyan); }
footer .footer-heading {
  font: 700 13px 'DM Sans';
  letter-spacing: 0.06em;
  text-transform: uppercase;
  color: rgba(255,255,255,0.5);
  margin-bottom: 16px;
}
footer .footer-bottom {
  border-top: 1px solid rgba(255,255,255,0.12);
  padding-top: 24px;
  margin-top: 48px;
  font-size: 12px;
  color: rgba(255,255,255,0.45);
}
```

---

## 9. WHAT TO BUILD FIRST (prototype priority order)

1. **Nav shell** — utility nav + primary nav with mega menu dropdowns. This is the #1 priority. All 5 sections should open with correct L2 column headers and L3 items. Test hover and keyboard nav.

2. **Homepage hero** — gradient background, headline, subheading, 4 audience pathway cards below.

3. **Reimbursement landing page** — demonstrates progressive disclosure pattern. Shows Coding, Medicare, Model Policies, Practice Management, Private Payers as cards.

4. **Publications & News section landing** — shows Journals featured prominently at top, Society News and News & Media below.

5. **Mobile nav** — hamburger → full-screen overlay → accordion pattern.

---

## 10. GOOGLE FONTS IMPORT

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=DM+Sans:ital,opsz,wght@0,9..40,400;0,9..40,500;0,9..40,600;0,9..40,700;0,9..40,800&display=swap" rel="stylesheet">
```

---

## 11. QUICK REFERENCE — TILE B vs TILE A

| Property | Tile A | **Tile B (use this)** |
|----------|--------|----------------------|
| Heading typeface | Source Serif 4 (serif) | **DM Sans 800 (geometric sans)** |
| Body typeface | Source Sans 3 | **DM Sans 400** |
| Button shape | Squared (4px radius) | **Pill (full radius 999px)** |
| Hero background | Solid ASTRO Blue | **Brand gradient** |
| Cyan usage | Subtle accent only | **Co-primary with blue** |
| Focus ring | Blue | **Cyan** |
| Quote treatment | Green quote mark | **Cyan left border** |
| Section labels | Blue | **Cyan** |
| Stat numbers | Blue | **Cyan** |
| Overall feel | Academic, institutional | **Modern, energetic, distinctive** |

---

*Use this file alongside ASTRO_Proposed_Sitemap_v3.md for the full prototype brief.*  
*Sitemap file = what to build. This file = how it should look.*  
*Both files should be uploaded together at the start of a Claude Code session.*
