# Bundus DNA Platform - Unified Design Guidelines

## Overview

The Bundus DNA Platform employs a **Dark Mode Bio-Tech Swiss Design System** with two complementary visual themes. This document consolidates design standards across all applications for consistency and clarity.

---

## Design Philosophy

### Core Principles

1. **Scientific Precision**: Dense, data-centric layouts that prioritize information accessibility
2. **High Contrast**: Ensuring accessibility and visual clarity
3. **Minimal Chrome**: Maximum data visibility, minimal decorative UI elements
4. **Swiss Functionality**: Clean grid systems, precise typography, intentional spacing
5. **Dark Mode**: Reduces eye strain for extended data analysis sessions
6. **Terminal Aesthetic**: Monospace fonts for genomic data and coordinates

### Not Allowed
- Glassmorphism effects on dashboards (data must remain crisp and readable)
- Playful or rounded icon styles
- Soft gradients on visualization elements
- Purple or teal default colors (explicitly forbidden)
- Complex map SVGs for basic geographic representation

---

## Theme A: Lab Instrument (Primary)

**Used by**: dna-deep-dive, core applications

### Color Palette

```json
{
  "background": {
    "main": "#050505",           // Ultra-dark primary background
    "card": "#0A0A0A",           // Slightly lighter card background
    "surface_hover": "#141414",  // Interactive hover state
    "overlay": "rgba(0, 0, 0, 0.8)"
  },
  "text": {
    "primary": "#FAFAFA",        // Off-white primary text
    "secondary": "#A3A3A3",      // Gray secondary text
    "muted": "#525252"           // Very muted tertiary text
  },
  "accents": {
    "primary": "#F59E0B",        // Amber (Tailwind: amber-500)
    "secondary": "#E11D48",      // Crimson (Tailwind: rose-600)
    "tertiary": "#FCD34D",       // Tertiary yellow (Tailwind: amber-300)
    "border": "#262626"          // Dark borders (Tailwind: zinc-800)
  }
}
```

### Typography

```json
{
  "fonts": {
    "heading": "Chivo",
    "body": "IBM Plex Sans",
    "mono": "IBM Plex Mono"
  },
  "hierarchy": {
    "h1": "text-4xl sm:text-5xl font-black tracking-tighter leading-none text-zinc-50",
    "h2": "text-2xl sm:text-3xl font-bold tracking-tight text-zinc-100",
    "h3": "text-xl font-semibold tracking-tight text-zinc-200",
    "overline": "text-xs font-mono uppercase tracking-[0.2em] text-amber-500",
    "body": "text-sm leading-relaxed text-zinc-400",
    "data_point": "text-base font-mono text-zinc-100"
  }
}
```

### Layout & Spacing

```json
{
  "grid_strategy": "Control Room Grid (Dense, Functional)",
  "container_padding": "p-4 md:p-6",
  "gap_size": "gap-4 md:gap-6",
  "radius": "rounded-none md:rounded-sm max-w-[4px]",
  "card_style": "bg-[#0A0A0A] border border-zinc-800 p-4 md:p-6 shadow-none flex flex-col hover:border-zinc-700 transition-colors"
}
```

### Components

#### Buttons
- **Primary**: `bg-amber-500 text-black hover:bg-amber-400 font-bold`
- **Secondary**: `border border-zinc-700 bg-transparent text-zinc-300 hover:text-white hover:border-zinc-600`
- Style: Flat, sharp edges (no radius)

#### Tables
- Extremely dense: `py-2 text-sm font-mono` for data cells
- Row borders: `border-b border-zinc-800/50`
- Hover states: `bg-zinc-900/50` on rows
- Header text: monospace, uppercase

#### Inputs
- Style: `bg-transparent border-zinc-800 text-zinc-100 focus:border-amber-500 focus:ring-1 focus:ring-amber-500 rounded-sm font-mono text-sm`

### Visual Enhancements

- **Borders**: 1px solid #262626 - Use 'Grid Borders' micro-theme to expose layout skeleton
- **Glassmorphism**: Avoid entirely for dashboards
- **Textures**: Add subtle 2% noise overlay to main background to reduce digital flatness
- **Charts**: No soft gradients; use sharp, distinct color blocks (Amber, Crimson, Off-White)

### Advanced Visualizations

#### Chromosome Ideogram
- **Library**: D3.js
- **Styling**: Dark mode SVG. Backbone in #262626, active segments in Amber/Crimson, centromeres marked with white
- **Interaction**: Hover tooltips snap precisely to bp locations

#### Haplogroup Globe
- **Library**: react-globe.gl
- **Styling**: Arc colors in Amber/Crimson, transparent background, no atmosphere glow for flat technical look

#### Ancestry Sunburst
- **Library**: D3.js
- **Styling**: Flat SVG paths with high contrast boundaries (1px black stroke between segments)

---

## Theme B: Bio-Tech (Alternative)

**Used by**: bundus-genetic-insights, bundus-with-your-hidden-insights

### Color Palette

```json
{
  "background_base": "#0A0A0C",                    // Deep navy-black
  "surface": "#121216",                            // Slightly lighter surface
  "surface_hover": "#1C1C22",                      // Hover state
  "surface_glass": "rgba(18, 18, 22, 0.7)",       // Glassmorphism (if used)
  "primary_action": "#3366FF",                     // Blue
  "gene_positive": "#00E676",                      // Green (positive traits)
  "gene_warning": "#FFC400",                       // Yellow (warning)
  "gene_alert": "#FF2A55",                         // Red (alert)
  "border": "rgba(255, 255, 255, 0.08)",          // Subtle light borders
  "text_primary": "#FAFAFA",                       // Off-white
  "text_secondary": "#A0A0AB",                     // Gray
  "text_muted": "#666670"                          // Muted gray
}
```

### Typography

```json
{
  "fonts_to_install": [
    "Cabinet Grotesk",
    "IBM Plex Sans",
    "IBM Plex Mono"
  ],
  "headings": {
    "family": "font-sans",
    "classes": "font-['Cabinet_Grotesk'] font-bold tracking-tight text-white",
    "hierarchy": {
      "h1": "text-4xl sm:text-5xl",
      "h2": "text-2xl sm:text-3xl",
      "h3": "text-xl sm:text-2xl",
      "h4": "text-lg"
    }
  },
  "body": {
    "family": "font-sans",
    "classes": "font-['IBM_Plex_Sans'] font-normal leading-relaxed text-[#A0A0AB]"
  },
  "mono": {
    "family": "font-mono",
    "classes": "font-['IBM_Plex_Mono'] text-xs tracking-widest uppercase"
  }
}
```

### Layout & Spacing

```json
{
  "dashboard_grid": "grid grid-cols-1 md:grid-cols-4 lg:grid-cols-12 gap-6",
  "spacing": "Generous paddings (p-6, p-8) for deep-dive sections. Dense padding (p-4) for data tables and widgets.",
  "alignment": "Strict left-alignment for data and copy. Grid items use align-items: start with align-self: stretch for consistent heights."
}
```

### Components

#### Buttons
- **Primary**: `bg-[#3366FF] hover:bg-[#2952CC] text-white border-none rounded-md px-6 py-2.5 text-sm font-medium transition-colors`
- **Outline**: `bg-transparent border border-[#3366FF]/50 text-[#3366FF] hover:bg-[#3366FF]/10 rounded-md px-4 py-2 text-sm uppercase tracking-widest`

#### Cards
- `bg-[#121216] border border-white/5 rounded-xl shadow-[inset_0_1px_0_rgba(255,255,255,0.05)] overflow-hidden`
- **Premium Cards** (Longevity, Mind): Add 1px glowing primary_action border

#### Tables
- Header: `text-xs font-['IBM_Plex_Mono'] text-[#A0A0AB] uppercase pb-3 border-b border-white/10`
- Data: `py-3 border-b border-white/5 font-['IBM_Plex_Sans']`

#### Inputs
- `bg-[#0A0A0C] border border-white/10 rounded-md focus:border-[#3366FF] focus:ring-1 focus:ring-[#3366FF] text-white`

### Data Visualization

- **Charts**: Use Recharts, no filled areas, stroke width 2, glow effect with drop-shadow
- **Colors**: #3366FF (blue), #00E676 (green), #FFC400 (yellow)
- **Ancestry Map**: Abstract visual representation using dark dotted background or ScatterChart

### Pages & Features

#### Dashboard Home
- Bento grid layout
- 'Bundus Assistant' summary panel at top
- Interactive Ancestry Map (col-span-8) + Precision Health Panel (col-span-4)

#### Trait Deep Dives
- Scrollable analytical sections
- Longevity (FOXO3), Mind & Temperament (COMT)
- Distinct iconography and progress/meter bars for trait expression

#### DNA Explorer
- Data-heavy terminal-style table
- Columns: RSID, Chromosome, Position, Genotype, Impact
- Monospace font for RSIDs and Genotypes

#### Auth & Upload
- Center-aligned glassmorphism card over hero background
- Dropzone with dashed border and subtle hover state

---

## Universal Standards (Both Themes)

### Iconography

- **Library**: @phosphor-icons/react (duotone or regular)
- **Style**: Precise, geometric; avoid playful/rounded icons
- **Size**: 24px default, 32px for primary actions, 16px for secondary

### Testing Requirements

**CRITICAL**: All interactive and key informational elements MUST include kebab-case `data-testid` attributes:

```jsx
// Examples:
<button data-testid="upload-dna-button">Upload</button>
<input data-testid="trait-search-input" />
<div data-testid="chromosome-ideogram" />
<a data-testid="nav-dashboard-link">Dashboard</a>
```

### Accessibility

- **Contrast**: Ensure WCAG AA compliance (4.5:1 for text)
- **Text Colors**: Use `text-[#FAFAFA]` for primary data (never #FFFFFF or #000000)
- **Focus States**: Visible focus rings on all interactive elements
- **Keyboard Navigation**: All features accessible via keyboard
- **Screen Readers**: Proper ARIA labels and semantic HTML

### Media Assets

#### Hero Image (DNA Helix)
- URL: https://static.prod-images.emergentagent.com/jobs/b5760be5-c0ae-4a2b-806d-97e6f63c157a/images/a730a281315e8765e5ecb0b3751018670ea5fc6f1ee2eb0c40286e30cb67f487.png
- Usage: Login/onboarding background or empty states
- Overlay: Max black/40% opacity

#### Chromosome Abstract
- URL: https://static.prod-images.emergentagent.com/jobs/b5760be5-c0ae-4a2b-806d-97e6f63c157a/images/f224fd891e96ac97bd551686f5123919512816ffe4f644c3c1be3967fed8c8c8.png
- Usage: Marketing landing page or header graphics

#### Bio-Tech Texture
- URL: https://static.prod-images.emergentagent.com/jobs/db256171-4328-4e7b-adb8-479473b43277/images/4335288b75364bf6d47651e1b36e1df73b19b5f6dc54382bbda30b57181f2a64.png
- Usage: Low opacity (5-10%) background in large Deep Dive cards

---

## Tone & Voice (Bundus Assistant)

**Persona**: Bundus (Executive Assistant)

**Style**: Calm, precise, competent, highly scientific but accessible

**Examples**:
- "Good morning. Your DNA data indicates a rapid caffeine metabolism (CYP1A2). Adjusting intake timing is recommended for optimal REM sleep."
- "Your longevity markers (FOXO3) show a favorable expression for cellular repair."

---

## Implementation Instructions

### For All Developers

1. **Install Icon Library**: `npm install @phosphor-icons/react`
2. **Font Installation**: Import from Google Fonts CSS
3. **Color Constants**: Define all colors in a shared config file
4. **Typography Scale**: Use consistent sizing hierarchy
5. **Spacing System**: 4px, 8px, 16px, 24px, 32px increments
6. **Component Library**: Use Shadcn + deep customization (not default Vercel look)

### Theme A (Lab Instrument) Specifics

1. Use raw HTML/Tailwind for landing page
2. Use Shadcn + customization for dashboard
3. **MUST use D3.js** for Chromosome Ideogram (requires precise bp coordinate mapping)
4. Use react-globe.gl for Haplogroup migration map
5. Implement 'Control Room' dense grid for dashboard
6. Use IBM Plex Mono for all genomic coordinates

### Theme B (Bio-Tech) Specifics

1. Strictly follow 'Control Room' dense grid strategy
2. Use Lucide-React or Phosphor Icons
3. Implement charts with Recharts (dark mode, stroke-based, no fills)
4. Build UI with Tailwind + standard accessible HTML
5. Include 'Bundus Assistant' sticky summary panel
6. Ensure DNA Explorer table handles large datasets cleanly

---

## Color Reference Quick Guide

### Lab Instrument Theme
```
🟠 Amber Primary: #F59E0B
🔴 Crimson Secondary: #E11D48
🟡 Yellow Tertiary: #FCD34D
⬛ Ultra Dark BG: #050505
⬜ Off-White Text: #FAFAFA
```

### Bio-Tech Theme
```
🔵 Blue Primary: #3366FF
🟢 Green Positive: #00E676
🟡 Yellow Warning: #FFC400
🔴 Red Alert: #FF2A55
⬛ Deep Navy BG: #0A0A0C
⬜ Off-White Text: #FAFAFA
```

---

## Deprecation Notice

❌ **DO NOT USE**:
- Purple or teal colors (explicitly forbidden)
- Glassmorphism on dashboards
- Soft gradients on charts
- Playful/rounded icons
- High-contrast pure black/white text
- Decorative UI chrome

✅ **DO USE**:
- Approved color palettes only
- Dense, functional layouts
- Monospace fonts for data
- Sharp, geometric icons
- Off-white text (#FAFAFA)
- Data-focused minimalism

---

**Last Updated**: June 5, 2026
**Version**: 1.0 (Consolidated)