# HỒ NGỌC QUÂN — PERSONAL PORTFOLIO
## Figma Design Specification

---

## 1. FRAME & CANVAS

### Desktop (Primary)
- Frame: 1440 x 900px (aspect ratio)
- Canvas color: #080B10
- Safe margins: 80px left/right
- Content width: 1280px max

### Tablet
- Frame: 768 x 1024px
- Safe margins: 40px left/right
- Content adapts to narrower layout

### Mobile
- Frame: 375 x 812px (iPhone 14 Pro)
- Safe margins: 20px left/right
- Single column layout

---

## 2. GRID SYSTEM

### Desktop Grid
- 12 columns
- Column gap: 24px
- Row height: 8px base unit
- Major grid lines every 8 rows (64px)

### Section Spacing
- Section padding: 120px vertical (desktop)
- Section padding: 80px vertical (tablet)
- Section padding: 60px vertical (mobile)

### Component Grid
- Card padding: 28px
- Button padding: 16px 28px
- Input padding: 14px 18px

---

## 3. TYPOGRAPHY

### Font Families
- Headings: "Space Grotesk", Inter, Arial, sans-serif
- Body: "Inter", Arial, sans-serif
- Code/Labels: "IBM Plex Mono", Courier New, monospace

### Type Scale
| Element | Size | Weight | Line Height |
|---------|------|--------|------------|
| Hero H1 | clamp(3.5rem, 8vw, 8rem) | 700 | 0.95 |
| Section H2 | clamp(2rem, 4vw, 4.5rem) | 600 | 1.1 |
| H3 | clamp(1.5rem, 2.5vw, 2.5rem) | 600 | 1.2 |
| H4 | 1.25rem | 500 | 1.3 |
| Body Large | 18px | 400 | 1.7 |
| Body | 16px | 400 | 1.7 |
| Small | 14px | 400 | 1.5 |
| Label | 12px | 500 | 1.4 |
| Mono Label | 11px | 500 | 1.3 |

### Special Typography
- Eyebrow text: 11px, uppercase, letter-spacing: 0.2em
- Section numbers: 11px, mono, accent color
- Technical labels: 10-13px, mono, muted color

---

## 4. COLOR SYSTEM

### Color Palette
```
Background Colors:
- bg:           #080B10  (primary dark)
- bg-soft:      #0D1118  (elevated surface)
- surface:      #111722  (cards, panels)
- surface-2:    #151D29  (nested surfaces)

Text Colors:
- text:         #F4F7FB  (primary text)
- text-secondary: #A7B0BF  (secondary text)
- text-muted:   #737E8F  (muted, labels)

Accent Colors:
- accent:       #69E6D7  (primary cyan/mint)
- accent-blue:  #69A7FF  (secondary blue)
- accent-soft:  rgba(105, 230, 215, 0.12)

Border Colors:
- border:       rgba(255, 255, 255, 0.09)
- border-hover: rgba(105, 230, 215, 0.36)

Functional:
- error:        #FF6B6B
- success:      #69E6D7
```

### Usage Rules
- Accent color used sparingly for emphasis
- Primary background: #080B10
- Cards/elevated surfaces: #111722 to #151D29
- Text contrast ratio: minimum 4.5:1 (WCAG AA)
- Accent on dark: high contrast, accessible

---

## 5. SPACING SYSTEM

### Base Unit: 8px
```
4px   - xs
8px   - sm
16px  - md
24px  - lg
32px  - xl
48px  - 2xl
64px  - 3xl
96px  - 4xl
128px - 5xl
```

### Section Spacing
- Desktop: 120px-160px vertical
- Tablet: 90px-110px vertical
- Mobile: 70px-90px vertical

### Container
- Max width: 1240px
- Padding inline: 32px (desktop), 20px (mobile)

---

## 6. BORDERS & RADIUS

### Border Width
- Subtle: 1px
- Default: 1px solid var(--border)
- Hover: 1px solid var(--border-hover)
- Accent: 1px solid var(--accent)

### Border Radius
```
--radius-sm:  10px  (buttons, inputs)
--radius-md:  18px  (cards, panels)
--radius-lg:  28px  (large containers)
--radius-xl:  40px  (hero elements)
```

### Shadows
```
--shadow-sm:  0 2px 8px rgba(0, 0, 0, 0.3)
--shadow-md:  0 8px 24px rgba(0, 0, 0, 0.4)
--shadow-lg:  0 16px 48px rgba(0, 0, 0, 0.5)
--shadow-glow: 0 0 40px rgba(105, 230, 215, 0.15)
```

---

## 7. COMPONENT SPECIFICATIONS

### Header
- Height: 72px
- Background: rgba(8, 11, 16, 0.85)
- Backdrop-filter: blur(20px)
- Border-bottom: 1px solid var(--border)
- Sticky position

### Logo
- Text: "HQ." or "HỒ QUÂN"
- Font: Space Grotesk, 20px, 600 weight
- Color: var(--text)

### Navigation Links
- Font: Inter, 14px, 500 weight
- Color: var(--text-secondary)
- Hover: var(--text)
- Active indicator: 2px accent underline
- Spacing: 32px between items

### CTA Button (Primary)
- Background: var(--accent)
- Color: var(--bg)
- Font: Inter, 14px, 600 weight
- Padding: 14px 28px
- Border-radius: var(--radius-sm)
- Hover: translateY(-2px), shadow-glow
- Arrow ↗ moves on hover

### CTA Button (Secondary/Ghost)
- Background: transparent
- Border: 1px solid var(--border)
- Color: var(--text)
- Hover: border-color var(--accent), text var(--accent)

### Project Card (Standard)
- Background: var(--surface)
- Border: 1px solid var(--border)
- Border-radius: var(--radius-md)
- Padding: 24px
- Hover: border-color var(--border-hover), translateY(-8px)

### Skill Pill/Tag
- Background: var(--surface-2)
- Border: 1px solid var(--border)
- Border-radius: 100px (pill)
- Padding: 8px 16px
- Font: Inter, 13px, 500 weight
- Hover: border-color var(--accent), translateY(-3px)

### Timeline Node
- Size: 12px circle
- Border: 2px solid var(--accent)
- Background: var(--bg)
- Active: pulse animation with accent glow

### Image Container
- Border-radius: var(--radius-md)
- Overflow: hidden
- Hover: scale(1.02) image inside

---

## 8. SECTION LAYOUTS

### Hero Section
- Min height: 92vh
- Asymmetric two-column on desktop
- Left: Content (60%)
- Right: Visual/Decoration (40%)
- Center alignment for mobile

### About Section (Editorial)
- Two columns
- Left: Large intro text (60%)
- Right: Info grid + Image (40%)
- Image: grayscale default, color on hover

### Skills Section (Structured Grid)
- Category labels
- Interactive pills in grid
- Technical index numbers

### Featured Project (Cinematic)
- Full-width card
- Large project number
- Image left, info right (desktop)
- Stacked on mobile
- Terminal/browser-style frame

### Projects Grid
- 3 cards in row (desktop)
- 2 cards (tablet)
- 1 card (mobile)
- Hover animations

### Journey (Timeline)
- Vertical timeline
- Left: Line + nodes
- Right: Content cards
- Alternating on desktop

### Notes + Aside
- Two columns: articles (70%) + aside (30%)
- Article cards in grid
- Aside sticky on scroll

### Contact Section
- Centered oversized typography
- Big CTA buttons
- Minimal design

### Footer
- Three columns: Logo, Nav, Social
- Quote
- Back to top button

---

## 9. MOTION & ANIMATION

### Timing
- Fast: 200ms
- Default: 400ms
- Slow: 600ms
- Entrance: 800ms-1200ms

### Easing
- Default: cubic-bezier(0.4, 0, 0.2, 1)
- Enter: cubic-bezier(0, 0, 0.2, 1)
- Exit: cubic-bezier(0.4, 0, 1, 1)
- Bounce: cubic-bezier(0.34, 1.56, 0.64, 1)

### Animations Used
1. Hero Reveal - fade up + blur clear
2. Greeting Cycle - text swap animation
3. Line Reveal - scaleX from center
4. Float - gentle translateY oscillation
5. Marquee - continuous horizontal scroll
6. Pulse - subtle scale + opacity
7. Hover Lift - translateY + shadow

### Reduced Motion
```css
@media (prefers-reduced-motion: reduce) {
  * {
    animation-duration: 0.01ms !important;
    transition-duration: 0.01ms !important;
  }
}
```

---

## 10. BREAKPOINTS

```
Mobile:    max-width: 430px
Mobile L:  max-width: 640px
Tablet:    max-width: 768px
Tablet L:  max-width: 1024px
Desktop:   min-width: 1025px
Desktop L: min-width: 1280px
Desktop XL: min-width: 1440px
```

### Responsive Strategy
- Mobile-first where practical
- Typography: clamp() for fluid sizing
- Spacing: reduce proportionally
- Grid: collapse columns gracefully
- Images: scale or hide decorative elements

---

## 11. VISUAL ASSETS

### Background Layers (CSS)
1. Base: #080B10
2. Radial gradient: accent glow (subtle)
3. Grid pattern: SVG grid overlay
4. Noise texture: SVG noise filter

### Decorative Elements
- Section numbers: 01, 02, 03...
- Technical coordinates
- Orbit lines (decorative)
- Accent underlines
- Gradient text on hero name

### Icons (Unicode/SVG)
- Arrow: ↗
- Status dot: ●
- Section marker: /
- Chevron: ▼

---

## 12. ACCESSIBILITY

### Focus States
```css
a:focus-visible,
button:focus-visible {
  outline: 2px solid var(--accent);
  outline-offset: 4px;
}
```

### Selection
```css
::selection {
  background: var(--accent);
  color: var(--bg);
}
```

### Color Contrast
- All text meets WCAG AA (4.5:1)
- Large text meets WCAG AAA (7:1)
- Interactive elements have distinct states

### Screen Reader
- Semantic HTML structure
- Alt text for all images
- Skip to content link
- Proper heading hierarchy

---

## 13. COMPONENT STATES

### Button States
| State | Background | Border | Color |
|-------|-----------|--------|-------|
| Default | var(--accent) | none | var(--bg) |
| Hover | var(--accent) | none | var(--bg) |
| Active | var(--accent-dark) | none | var(--bg) |
| Focus | var(--accent) | 2px outline | var(--bg) |

### Card States
| State | Border | Transform | Shadow |
|-------|--------|-----------|--------|
| Default | var(--border) | none | none |
| Hover | var(--border-hover) | translateY(-8px) | shadow-md |
| Focus | var(--border-hover) | none | shadow-sm |

### Link States
| State | Color | Decoration |
|-------|-------|------------|
| Default | var(--text-secondary) | none |
| Hover | var(--text) | underline |
| Active | var(--accent) | underline |

---

## 14. PAGE STRUCTURE

```
[HEADER] - Sticky
  ├── Logo
  ├── Navigation
  └── GitHub CTA

[HERO] - 92vh
  ├── Eyebrow (location, role)
  ├── Greeting animation
  ├── Name (large typography)
  ├── Subtitle
  ├── Description
  ├── CTA buttons
  └── Visual/Portrait area

[ABOUT]
  ├── Eyebrow
  ├── Section title
  ├── Intro text
  └── Info grid + Photo

[MARQUEE] - Interest strip

[SKILLS]
  ├── Eyebrow
  ├── Section title
  └── Skill categories (Programming, Tools, Learning)

[FEATURED PROJECT]
  ├── Eyebrow
  ├── Project number
  ├── Large showcase
  ├── Project info
  └── Tags

[OTHER PROJECTS]
  ├── Section header
  └── Project cards (3)

[GITHUB STRIP] - CTA banner

[JOURNEY] - Timeline
  ├── Eyebrow
  ├── Section title
  └── Timeline items (4)

[CURRENT EXPLORATIONS] - Multiple columns
  ├── Eyebrow
  ├── Heading
  └── Two-column content

[NOTES + ASIDE]
  ├── Notes cards
  └── Aside (Currently exploring + Social)

[CONTACT]
  ├── Eyebrow
  ├── Large heading
  ├── CTA buttons
  └── Social links

[FOOTER]
  ├── Logo
  ├── Navigation
  ├── Social
  ├── Quote
  └── Copyright
```

---

## 15. EXPORT NOTES

### Images Required (from user)
- avatar.jpg - Portrait photo (500x500px min)
- profile-about.jpg - About section photo (800x1000px)
- project-nextgpu.jpg - NEXTGPU PRO screenshot (1200x750px)
- project-chess.jpg - Chess project screenshot (600x400px)
- project-code-c.jpg - Code_C project screenshot (600x400px)
- project-code-c2.jpg - Code_C_2 project screenshot (600x400px)

### Placeholders
All images have fallback backgrounds (gradients/patterns) if not provided.

---

## 16. TECHNICAL NOTES

### CSS Architecture
- BEM naming convention
- CSS custom properties (variables)
- Organized by section
- Comments for CSS3 groups

### CSS3 Groups (7 Required)
1. SELECTORS
2. BORDER & BACKGROUND
3. TEXT EFFECTS
4. 2D / 3D TRANSFORM
5. TRANSITIONS & ANIMATIONS
6. MULTIPLE COLUMNS
7. USER INTERFACE

### Performance
- CSS animations on transform/opacity only
- SVG for decorative graphics
- Lazy loading for images (native)
- No external JS libraries
