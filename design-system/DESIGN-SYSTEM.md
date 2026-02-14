# KodNest Premium Build System

A calm, intentional design system for serious B2C product experiences.

---

## Design Philosophy

- **Calm** — No animation noise, no gradients, no glassmorphism
- **Intentional** — Every decision has purpose
- **Coherent** — One visual language throughout
- **Confident** — Large typography, generous spacing, clear hierarchy

---

## Color System

| Token | Hex | Usage |
|-------|-----|-------|
| Background | `#F7F6F3` | Page background |
| Primary text | `#111111` | Body copy, headings |
| Accent | `#8B0000` | Primary buttons, links, focus |
| Success | `#4A7C59` | Status shipped, checkmarks |
| Warning | `#B8860B` | Caution states |

Maximum 4 colors. Muted variants for borders and secondary text only.

---

## Typography

- **Headings:** Libre Baskerville (serif), large, generous spacing
- **Body:** Source Sans 3 (sans-serif), 16–18px, line-height 1.6–1.8
- **Text blocks:** Max-width 720px
- **No decorative fonts, no random sizes**

---

## Spacing Scale

Only these values: `8px`, `16px`, `24px`, `40px`, `64px`

| Token | Value |
|-------|-------|
| `--space-1` | 8px |
| `--space-2` | 16px |
| `--space-3` | 24px |
| `--space-4` | 40px |
| `--space-5` | 64px |

---

## Global Layout Structure

Every page follows this structure:

1. **Top Bar** — Project name (left) | Progress Step X/Y (center) | Status badge (right)
2. **Context Header** — Large serif headline, 1-line subtext
3. **Main** — Primary Workspace (70%) + Secondary Panel (30%)
4. **Proof Footer** — Checklist: □ UI Built □ Logic Working □ Test Passed □ Deployed

---

## Components

### Buttons
- **Primary:** Solid deep red (`#8B0000`)
- **Secondary:** Outlined, transparent fill
- **Transitions:** 150–200ms ease-in-out
- **Border radius:** 4px everywhere

### Inputs
- Clean 1px border
- Focus: accent color border
- No heavy shadows

### Cards
- Subtle 1px border
- No drop shadows
- Padding: 24px

### Secondary Panel
- Step explanation (short)
- Copyable prompt box
- Actions: Copy, Build in Lovable, It Worked, Error, Add Screenshot

---

## Interaction Rules

- **Transitions:** 150–200ms, ease-in-out
- **No bounce, no parallax**
- **Hover:** Same treatment across all interactive elements

---

## Error States

- Explain what went wrong
- Explain how to fix it
- Never blame the user

## Empty States

- Provide next action
- Never feel dead

---

## Usage

```html
<link rel="stylesheet" href="design-system/kodnest.css" />
```

```html
<div class="kodnest-app">
  <header class="kodnest-topbar">
    <span class="kodnest-topbar__project">Project Name</span>
    <span class="kodnest-topbar__progress">Step 2 / 5</span>
    <span class="kodnest-topbar__status kodnest-topbar__status--in-progress">In Progress</span>
  </header>
  <section class="kodnest-context">
    <h1 class="kodnest-context__headline">Headline</h1>
    <p class="kodnest-context__subtext">One-line subtext.</p>
  </section>
  <main class="kodnest-main">
    <div class="kodnest-workspace">...</div>
    <aside class="kodnest-panel">...</aside>
  </main>
  <footer class="kodnest-footer">
    <div class="kodnest-footer__checklist">...</div>
  </footer>
</div>
```

---

## File Structure

```
design-system/
├── tokens.css      — Design tokens (colors, typography, spacing)
├── base.css        — Reset, typography base
├── layout.css      — App shell, TopBar, Context, Workspace, Panel, Footer
├── components.css  — Buttons, inputs, cards, panel elements, error/empty states
├── kodnest.css     — Single entry point (import all)
└── DESIGN-SYSTEM.md — This document
```
