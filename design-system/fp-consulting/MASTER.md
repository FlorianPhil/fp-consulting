# Design System Master File

> **LOGIC:** When building a specific page, first check `design-system/pages/[page-name].md`.
> If that file exists, its rules **override** this Master file.
> If not, strictly follow the rules below.

---

**Project:** FP. Consulting
**Generated:** 2026-03-26
**Category:** Premium Brand Strategy / Editorial
**Visual Metaphor:** Light passing through a prism... clarity, transformation, controlled revelation.
**Sensory Register:** Matte, not glossy. Grain, not polish. A private doctor's office, not a nightclub.

---

## Color System

| Role | Hex | CSS Variable | Usage |
|------|-----|--------------|-------|
| Brand Accent | `#5A5CF9` | `--accent` | Logo dot, CTAs, accent elements, highlights |
| Accent Glow | `rgba(90, 92, 249, 0.35)` | `--accent-glow` | Hover states, focus rings |
| Accent Soft | `rgba(90, 92, 249, 0.08)` | `--accent-soft` | Subtle backgrounds, hover fills |
| Dark Base | `#1D1D1D` | `--dark` | Dark sections, social thumbnails |
| Light Base | `#F6F6F6` | `--light` | Primary website background |
| Pure White | `#FFFFFF` | `--white` | Cards, breathing sections |
| Pure Black | `#000000` | `--black` | Headlines on light backgrounds |
| Mid Gray | `#949494` | `--gray` | Subtitles, secondary text, metadata |
| Light Gray | `#E0E0E0` | `--gray-light` | Borders, dividers |

### Color Rules (Non-Negotiable)
- Purple `#5A5CF9` is ALWAYS the accent, never the background (except carousels)
- No warm colors (orange, red, yellow) as design elements. EVER.
- Palette is intentionally narrow... restriction creates recognition.
- Glass elements on dark: `rgba(255, 255, 255, 0.06)` bg + `rgba(255, 255, 255, 0.1)` border + `backdrop-filter: blur(16px)`

---

## Typography

### Primary: Bricolage Grotesque (LOCKED)
- Headlines: Bold/Heavy (700-800), large, often uppercase
- Subtitles: Regular/Medium (400-500), smaller, often in `--gray`
- CTAs: Bold (700), inside sharp-cornered buttons

### Secondary: Inter (LOCKED)
- Body copy, captions, metadata, UI labels
- Weights: 300 (light), 400 (regular), 500 (medium), 600 (semibold)

**CRITICAL: Never change these typefaces. Never introduce new fonts.**

```css
@import url('https://fonts.googleapis.com/css2?family=Bricolage+Grotesque:opsz,wght@12..96,200..800&family=Inter:wght@300;400;500;600&display=swap');
```

### Type Scale

| Token | Size | Usage |
|-------|------|-------|
| `--text-hero` | `clamp(56px, 8vw, 120px)` | Hero headline |
| `--text-h1` | `clamp(40px, 5vw, 72px)` | Section headlines |
| `--text-h2` | `clamp(28px, 3.5vw, 48px)` | Sub-section headlines |
| `--text-h3` | `clamp(20px, 2vw, 28px)` | Card titles, feature heads |
| `--text-body` | `clamp(16px, 1.2vw, 18px)` | Body copy |
| `--text-small` | `clamp(13px, 1vw, 15px)` | Captions, metadata |
| `--text-eyebrow` | `clamp(11px, 1.2vw, 13px)` | Labels, overlines |

### Typography Rules
- One headline per visual, immediately readable
- Keyword emphasis: bold the single most important word (sometimes in `#5A5CF9`)
- Generous line height... text always breathes (1.5-1.7 for body, 1.1-1.2 for headlines)
- All-caps reserved for eyebrow labels and short headlines only
- Minimum ~8% canvas width as margin

---

## Spacing System

| Token | Value | Usage |
|-------|-------|-------|
| `--space-xs` | `4px` | Tight gaps |
| `--space-sm` | `8px` | Icon gaps, inline spacing |
| `--space-md` | `16px` | Standard padding |
| `--space-lg` | `24px` | Component internal padding |
| `--space-xl` | `32px` | Card padding, medium gaps |
| `--space-2xl` | `48px` | Section internal spacing |
| `--space-3xl` | `64px` | Section separators |
| `--section-pad` | `clamp(100px, 12vw, 180px)` | Section vertical padding |
| `--container` | `1240px` | Max content width |
| `--gutter` | `clamp(24px, 5vw, 64px)` | Container horizontal padding |

---

## Two Visual Modes

### Mode B: Light / Editorial (DEFAULT for website)
- Background: `#FFFFFF` or `#F6F6F6`
- Photography featured LARGE (half-page or full-section)
- Bold black typography on light backgrounds
- Purple as accent only: CTAs, underlines, keyword highlights
- White space is an active design tool

### Mode A: Dark / Conceptual (accent sections only)
- Background: `#1D1D1D`
- ALWAYS includes grain texture overlay (~3-4% opacity)
- ALWAYS includes 3px purple edge at bottom
- Glass-morphism cards for content within dark sections
- Max 1-2 dark sections per page

---

## Component Specs

### Buttons (Sharp corners. No pills. No border-radius.)

```css
/* Primary: Solid Black */
.btn-primary {
  background: var(--black);
  color: var(--white);
  padding: 14px 28px;
  border-radius: 0;
  font-family: var(--ff-primary);
  font-weight: 700;
  font-size: 14px;
  letter-spacing: 0.02em;
  transition: all 200ms ease;
  cursor: pointer;
}
.btn-primary:hover {
  background: var(--dark);
  transform: translateY(-1px);
}

/* Ghost: Text + Arrow */
.btn-ghost {
  background: transparent;
  color: var(--dark);
  padding: 14px 0;
  border: none;
  border-radius: 0;
  font-family: var(--ff-body);
  font-weight: 500;
  font-size: 14px;
  cursor: pointer;
  display: inline-flex;
  align-items: center;
  gap: 8px;
  transition: gap 200ms ease;
}
.btn-ghost:hover { gap: 12px; }
.btn-ghost::after { content: '\2192'; }

/* Outline */
.btn-outline {
  background: transparent;
  color: var(--dark);
  padding: 14px 28px;
  border: 1.5px solid var(--dark);
  border-radius: 0;
  font-family: var(--ff-primary);
  font-weight: 600;
  font-size: 14px;
  transition: all 200ms ease;
  cursor: pointer;
}
.btn-outline:hover {
  background: var(--dark);
  color: var(--white);
}

/* Purple CTA: ONE per page maximum */
.btn-accent {
  background: var(--accent);
  color: var(--white);
  padding: 16px 32px;
  border-radius: 0;
  font-family: var(--ff-primary);
  font-weight: 700;
  font-size: 14px;
  letter-spacing: 0.02em;
  transition: all 200ms ease;
  cursor: pointer;
}
.btn-accent:hover {
  background: #4849e0;
  transform: translateY(-1px);
}
```

### Glass Cards (dark sections only)

```css
.glass-card {
  background: rgba(255, 255, 255, 0.06);
  border: 1px solid rgba(255, 255, 255, 0.1);
  backdrop-filter: blur(16px);
  -webkit-backdrop-filter: blur(16px);
  padding: 32px;
  border-radius: 0; /* Sharp corners */
}
```

### Grain Texture (dark surfaces only)

```css
.grain::after {
  content: '';
  position: absolute;
  inset: 0;
  background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noise'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noise)' opacity='1'/%3E%3C/svg%3E");
  background-size: 128px 128px;
  opacity: 0.035;
  pointer-events: none;
  z-index: 1;
}
```

### Purple Edge (dark sections)

```css
.purple-edge::after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  height: 3px;
  background: var(--accent);
  z-index: 2;
}
```

---

## Navigation

- Fixed, transparent on load, glass-blur on scroll
- FP. logo left (Bricolage Grotesque 700, dot in `#5A5CF9`)
- Links right: Process, About, Blog, Book a Call (purple CTA)
- Hides on scroll down, reveals on scroll up
- Mobile: hamburger menu with full-screen overlay

---

## Animation System

### Scroll-Triggered Reveals
- Elements fade up 20px with 0.6s ease on intersection
- Stagger children by 0.1s delay each
- Use IntersectionObserver at threshold 0.1

### Signature Animations
- **Page loader:** FP. logo + purple loading line, white bg, fades out
- **Custom cursor:** 6px purple dot + 36px ring, expands on hover
- **Marquee tagline:** Horizontal scrolling large text, continuous loop
- **Progress bar:** 3px purple, fixed top, scales with scroll
- **Word-by-word reveal:** Headlines reveal one word at a time on scroll
- **Counter animation:** Numbers count up when visible

### Motion Principles
- Slow, deliberate. Things drift, not jump.
- Reveals, not pops.
- 400-600ms for major transitions
- 150-200ms for micro-interactions (hovers, focuses)
- `prefers-reduced-motion` must be respected

---

## Section Contrast Rhythm

Never flat-alternate the same tones. Bold contrast jumps.

Recommended homepage flow:
1. **Hero** (white bg, photography + headline)
2. **Statement** (dark bg, grain + purple edge, quote)
3. **What is Brand Therapy** (light bg, photography left, text right)
4. **Process** (dark bg, grain + purple edge, glass cards, numbered steps)
5. **Benefits** (white bg, clean editorial)
6. **Two Ways to Work** (light bg, side-by-side cards)
7. **Testimonials** (white bg, large quotes)
8. **CTA** (dark bg, grain + purple edge, final conversion)
9. **FAQ** (light bg, accordion)
10. **Footer** (dark, minimal)

---

## Photography Direction

- Photography is a PRIMARY design element, not supporting
- Scale: LARGE. Half-page or full-section. Never a small avatar.
- Hero image: `florian-editorial-lens-bw` in FULL COLOR (selective color through glass)
- Treatments: B&W with selective color reveal, straight B&W at high contrast, natural
- Smart casual style: vest, gingham shirt, tie. Intellectual but approachable.

---

## Anti-Patterns (Never Do These)

- Dark backgrounds for entire website pages
- Reducing photography to small avatars
- Warm color palettes (orange, red, yellow)
- Generic stock photography
- Busy compositions... if it feels cluttered, remove elements
- Gradient backgrounds
- Rounded, friendly, "startup" aesthetics (pill buttons, etc.)
- Multiple accent colors (purple is the ONLY accent)
- Decorative elements for decoration's sake
- CSS-faked 3D prism effects (conic-gradient, etc.)
- Flat same-tone section alternation
- Inflated vanity stats (no fake numbers)
- Template-looking layouts... every section must feel intentional
- Em dashes in any copy

---

## Pre-Delivery Checklist

- [ ] Mode B (light) as default, max 1-2 dark accent sections
- [ ] Bricolage Grotesque + Inter only (no other fonts)
- [ ] `#5A5CF9` as only accent color
- [ ] Sharp-cornered buttons (border-radius: 0)
- [ ] Hero lens image in COLOR, never B&W
- [ ] Photography featured at appropriate scale (large)
- [ ] Grain texture on dark surfaces only
- [ ] Purple edge (3px) at bottom of dark sections
- [ ] No fake stats or inflated numbers
- [ ] No em dashes in any copy
- [ ] `cursor: pointer` on all clickable elements
- [ ] Hover states with smooth transitions (150-300ms)
- [ ] Text contrast 4.5:1 minimum
- [ ] Focus states visible for keyboard nav
- [ ] `prefers-reduced-motion` respected
- [ ] Responsive: 375px, 768px, 1024px, 1440px
- [ ] No horizontal scroll on mobile
