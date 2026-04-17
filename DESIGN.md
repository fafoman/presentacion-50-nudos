# DESIGN.md — 50 Nudos: Velocidad de Crucero

## 1. Visual Theme & Atmosphere

"50 Nudos" is a sales contest for insurance professionals competing for a Caribbean cruise. The visual identity fuses three reference aesthetics into a **nautical-premium** language:

- **SpaceX's cinematic darkness** — full-viewport sections, text directly on dark canvas, industrial uppercase for key metrics, zero unnecessary decoration
- **Lamborghini's gold-on-black drama** — warm gold (#FFC000) as the sole accent of aspiration, theatrical reveals, monumental display type for prizes
- **Apple's controlled white space** — clean informational sections with generous breathing room, SF-inspired typography, product-page clarity for data

The result: a dark, commanding interface that alternates between **deep navy scenes** (data, market size, prizes) and **warm cream panels** (rules, zones, formulas). Every number is treated as a hero element. The cruise prize glows gold against darkness. Data slides feel like mission briefings. The overall mood is: **ambitious, urgent, achievable**.

**Key Characteristics:**
- Navy-dominant dark surfaces with cyan data accents and gold aspiration accents
- Alternating dark/light sections to prevent visual fatigue
- Numbers rendered at hero scale with monospace precision (JetBrains Mono)
- Zero generic patterns — no purple gradients, no Inter font, no centered-everything layouts
- Nautical motifs used sparingly: compass rose, wave lines, horizon metaphors
- Grid overlays at low opacity for technical/navigational feel
- Full-viewport sections — each section is a "scene" in the journey

## 2. Color Palette & Roles

### Dark Surfaces
- **Navy Deep** (`#0a1628`): Primary background — the ocean at night
- **Navy Mid** (`#112240`): Elevated surfaces, cards on dark backgrounds
- **Navy Light** (`#1a3355`): Tertiary dark surface, subtle hover states

### Light Surfaces
- **Cream Warm** (`#f5f0e8`): Primary light background — like aged nautical paper
- **Cream Light** (`#ece4d4`): Secondary light surface
- **Pure White** (`#ffffff`): Card backgrounds on light sections only

### Accent — Data (Cyan)
- **Cyan Primary** (`#00e5cc`): Metrics, progress bars, data highlights, active states
- **Cyan Glow** (`rgba(0, 229, 204, 0.15)`): Subtle backgrounds, glowing borders
- **Cyan Dim** (`rgba(0, 229, 204, 0.06)`): Chip/badge backgrounds

### Accent — Aspiration (Gold)
- **Gold Primary** (`#FFC000`): The cruise prize, CTA moments, achievement badges
- **Gold Light** (`#FFCE3E`): Hover state, shimmer highlights
- **Gold Dark** (`#917300`): Pressed state, deep gold borders
- **Gold Glow** (`rgba(255, 192, 0, 0.12)`): Prize card backgrounds

### Text
- **Spectral White** (`#f0f0fa`): Primary text on dark — slight blue tint, not pure white
- **White Dim** (`#8899aa`): Secondary text, labels, descriptions on dark
- **Dark Text** (`#1a1a1a`): Primary text on light surfaces
- **Mid Text** (`#666666`): Secondary text on light surfaces

### Semantic
- **Green Bolívar** (`#1a6b3c`): Seguros Bolívar brand reference, used on light sections as accent
- **Progress Red** (`#e74c3c`): Far from goal
- **Progress Yellow** (`#f1c40f`): In progress
- **Progress Green** (`#2ecc71`): On track / qualified

## 3. Typography Rules

### Font Families
- **Display**: `'Playfair Display', serif` — dramatic serif for headlines, loaded from Google Fonts with weights 400, 700, 900, and italic 400
- **Body / UI**: `'DM Sans', sans-serif` — clean geometric sans for body text, loaded with weights 300, 400, 500, 600, 700
- **Data / Numbers**: `'JetBrains Mono', monospace` — precision monospace for all numerical data, loaded with weights 400, 600

### Hierarchy

| Role | Font | Size | Weight | Notes |
|------|------|------|--------|-------|
| Hero Title | Playfair Display | 4.5rem (72px) | 900 | For slide titles with maximum impact |
| Slide Title | Playfair Display | 3.2rem (51px) | 900 | Standard slide headings |
| Section Title | Playfair Display | 2rem (32px) | 700 | Card headers, sub-sections |
| Subtitle | DM Sans | 1.3rem (21px) | 300 | Italic, used below titles |
| Body | DM Sans | 1rem (16px) | 400 | Standard readable text |
| Body Strong | DM Sans | 1rem (16px) | 600 | Emphasized body text |
| Label | DM Sans | 0.75rem (12px) | 700 | Uppercase, letter-spacing: 3px, for card labels |
| Big Number | JetBrains Mono | 5rem (80px) | 600 | Hero metrics (383.800, 1.96%) |
| Stat Number | JetBrains Mono | 2.5rem (40px) | 600 | Secondary metrics in stat rows |
| Table Number | JetBrains Mono | 0.95rem (15px) | 400 | Data tables |
| Tag | DM Sans | 0.75rem (12px) | 700 | Uppercase, letter-spacing: 2px, pill badges |

### Principles
- Numbers are ALWAYS in JetBrains Mono — mixing numeric fonts kills precision
- Colombian number formatting: periods as thousand separators ($77.500.000)
- Currency prefix with dollar sign, no decimals unless relevant
- Playfair Display only for display/title use — never for body text
- DM Sans weight 300 (light) is reserved for subtitles and italic contexts
- On dark surfaces: Spectral White for primary, White Dim for secondary
- On light surfaces: Dark Text for primary, Mid Text for secondary

## 4. Component Patterns

### Cards (Dark Surface)
- Background: `rgba(255, 255, 255, 0.04)` — barely visible elevation
- Border: `1px solid rgba(0, 229, 204, 0.15)` — cyan ghost border
- Border-radius: `16px`
- Padding: `36px`
- No shadow — the border IS the definition

### Cards (Light Surface)
- Background: `rgba(0, 0, 0, 0.03)`
- Border: `1px solid rgba(0, 0, 0, 0.1)`
- Border-radius: `16px`
- Padding: `36px`

### Progress Bars
- Track: `rgba(255, 255, 255, 0.06)` on dark, `rgba(0, 0, 0, 0.06)` on light
- Fill: `linear-gradient(90deg, #00e5cc, #00b8a9)` — cyan gradient
- Height: `28px` with `14px` border-radius
- Animate width on enter with `transition: width 1.5s cubic-bezier(0.4, 0, 0.2, 1)`

### Tags/Badges
- Cyan tag: `background: rgba(0, 229, 204, 0.15); color: #00e5cc`
- Gold tag: `background: rgba(255, 192, 0, 0.15); color: #FFC000`
- Padding: `4px 14px`, border-radius: `20px`
- Uppercase, letter-spacing: `2px`

### Prize Card (Special)
- Background: `linear-gradient(135deg, rgba(212, 168, 83, 0.1), rgba(212, 168, 83, 0.03))`
- Border: `2px solid #FFC000`
- Border-radius: `20px`
- Shimmer animation: `background: linear-gradient(90deg, transparent, rgba(255, 192, 0, 0.08), transparent)` moving at `3s linear infinite`
- Pulsing box-shadow: alternating between `0 0 20px rgba(255, 192, 0, 0.2)` and `0 0 60px rgba(255, 192, 0, 0.1)`

### Highlight Box
- Left border: `4px solid #00e5cc`
- Background: `linear-gradient(135deg, rgba(0, 229, 204, 0.08), rgba(0, 229, 204, 0.02))`
- Border-radius: `0 12px 12px 0`
- Padding: `20px 28px`

### Glow Line (Decorative)
- Width: `80px`, height: `3px`
- Background: `linear-gradient(90deg, #00e5cc, transparent)`
- Centered below titles as a subtle accent rule

## 5. Layout Patterns

### Slide-based (Presentation)
- Each slide: `100vh × 100vw`, flexbox centered
- Padding: `60px 80px` (projector safe area)
- Max content width: `1100px`
- Background alternates: dark (navy gradient) → light (cream) → dark

### Two-Column Split
- `display: grid; grid-template-columns: 1fr 1fr; gap: 40px`
- Used for SENA vs UNAD, formula explanations, before/after

### Stat Row
- `display: flex; gap: 60px; justify-content: center`
- Each stat: big number on top (cyan or gold), small label below (dim text)

### Timeline
- Horizontal flex with absolute line connecting nodes
- Line: `linear-gradient(90deg, #00e5cc, #FFC000)`
- Nodes: circles (cyan) transitioning to star (gold) for final prize

## 6. Animation Guidelines

### Library: GSAP 3.12+ via CDN
```
https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.5/gsap.min.js
https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.5/ScrollTrigger.min.js
```

### Core Animations
- **Counter-up**: Numbers count from 0 to target on slide enter (duration: 2s, ease: power2.out)
- **Stagger reveal**: Elements fade up with 150ms delay between siblings
- **Progress fill**: Bars animate from 0% to target width (duration: 1.5s)
- **Shimmer**: Gold prize card has continuous shimmer sweep
- **Pulse**: Prize elements have subtle box-shadow pulse
- **Wave**: CSS-only SVG wave animation at bottom of cover/closing slides

### Transition Between Slides
- Exit: `opacity: 0, translateY: -40px` (0.7s, cubic-bezier)
- Enter: `opacity: 1, translateY: 0` from `opacity: 0, translateY: 40px`

### Performance Rules
- Use `transform` and `opacity` only — no layout-triggering properties
- `will-change: transform, opacity` on animated elements
- Maximum 3 simultaneous animations per slide
- Disable heavy animations if `prefers-reduced-motion` is set

## 7. Nautical Decorative Elements

Use SPARINGLY — decoration must never compete with data.

- **Grid overlay**: `background-image` with 60px grid lines at 3% cyan opacity — on dark slides only
- **Compass rose**: Positioned absolute, bottom-right, 200px, very low opacity (0.3-0.4). CSS-only with circle border and rotated line.
- **Wave line**: SVG path at bottom of cover/closing slides. Animated with CSS translateX. Opacity 0.15.
- **Glow line**: 80px gradient line below titles as punctuation.

NO: anchor icons, ship wheels, nautical rope borders, or any other clip-art-level decoration.

## 8. Branding Rules

### Torres Guarín × Seguros Bolívar
- **Equal prominence** — always. Neither brand larger than the other.
- Cover: `Torres Guarín | 50 | Seguros Bolívar` — horizontal, centered
- Closing: `Seguros Bolívar | Torres Guarín — Desde 1976` — Bolívar first by convention but same size
- Logo separator: 2px vertical line, 30px tall, 20% white opacity
- Font for brand names: Playfair Display, weight 700, 1.1rem
- The "50" between them: weight 900, 2.2rem, cyan color

### Contest Name
- **"50 Nudos"** — primary name, always in Playfair Display, weight 900
- **"Velocidad de Crucero"** — tagline, in DM Sans, weight 300, italic
- The connection: "Un nudo es la velocidad en el mar. 50 nudos es velocidad de crucero. Y este año, cumplimos 50."

## 9. Google Fonts CDN

```html
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;0,900;1,400&family=DM+Sans:wght@300;400;500;600;700&family=JetBrains+Mono:wght@400;600&display=swap" rel="stylesheet">
```
