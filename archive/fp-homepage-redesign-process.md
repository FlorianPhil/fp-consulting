# FP. Homepage Redesign: Process & Research Brief

**Created:** March 19, 2026
**Purpose:** Hand this to the design session (with all skills loaded) so it can execute the homepage redesign without repeating any of this research.
**This document is RESEARCH ONLY. No design decisions have been finalized.**

---

## What This Session Figured Out

### The Original Question
Florian saw a video about using Google Stitch MCP + Nano Banana 2 + UI UX Pro Max skill + 21st.dev to create premium, animated websites via Claude Code. He wants that level of visual execution for florianp.com, but his site runs on Wix Studio, not React/Next.js.

### The Core Problem (Not Strategy, Not Brand)
The brand guidelines, voice, creative direction, and copy are all solid and well-documented. The gap is purely execution quality: the site looks like a 2024 Wix template. It needs scroll animations, 3D elements, micro-interactions, and that "alive" feeling that separates a $50K website from a template.

---

## Platform Decision: Stay on Wix Studio

Florian's Wix Studio setup includes payments, CRM, forms, SEO, tracking, and blog integrations. Rebuilding on Wix Headless would mean losing all of that. The decision is to stay on Wix Studio and push its capabilities to the limit.

### What's Proven Possible on Wix Studio

**Native (no code):**
- Scroll animations tied to scroll position (scrub-style)
- Entrance animations (fade, slide, spin, drop)
- Mouse parallax (elements move with cursor)
- WebGL effects on media backgrounds
- Horizontal scroll sections
- Multi-speed parallax layers

**Via Embeds / Custom Elements (proven, community-validated):**
- GSAP + ScrollTrigger via CDN inside Embed Code blocks or Custom Elements
- Spline 3D scenes via iframe embed (official Spline integration exists)
- Lottie animations (native support, paste JSON URL)
- Scroll-Based Lottie Animation app on Wix App Market
- Any JS ES6 library via Custom Elements

**What does NOT work:**
- NPM install of any library (Wix blocks DOM access for npm packages)
- GSAP animating native Wix page elements (only works inside its own embed container)
- More than 1 scroll-based Lottie per page with the third-party app
- Parallax on mobile (disabled automatically by Wix)

### Proof That Premium Wix Studio Sites Exist
- Eliran Vahdi's cosmic scroll site won an Awwwards Honorable Mention, built entirely in Wix Studio with no custom code
- Wix Studio Inspiration Gallery: https://www.wix.com/studio/inspiration
- Alice in Wonderland mouse parallax showcase by the Wix WOW team

---

## The Tools from the Video: What Applies and What Doesn't

| Tool | Verdict for Wix Studio | Notes |
|------|----------------------|-------|
| Google Stitch MCP | USEFUL (mockup generation is platform-agnostic) | Generates visual mockup targets, not final code. Could be installed in Claude Code for the design session. |
| Nano Banana 2 | USEFUL (image generation is platform-agnostic) | For custom hero images, backgrounds, textures. Not for wireframing as originally thought from the video. Actually it IS for generating mockup images of what the site should look like. The design session should clarify which. |
| UI UX Pro Max skill | SKIP | React/Next.js focused. Conflicts with Florian's existing brand/UX skills. |
| 21st.dev components | SKIP | React-only component library. Can't deploy into Wix Studio. |

### What to Use Instead
- **Spline** (free, official Wix Studio integration) replaces 21st.dev for 3D elements
- **GSAP via CDN in Embed blocks** replaces React animation libraries
- **Lottie** for micro-animations (icons, transitions, loading states)
- **Wix native scroll animations** for section transitions, parallax, entrance effects
- **Florian's existing brand/UX/design skills** replace UI UX Pro Max

---

## The Proposed Pipeline for the Design Session

### Step 1: Pull All Real Content First
Before any design work, the design session MUST pull:
- Actual approved copy from Notion (headlines, descriptions, CTAs)
- Real testimonials (with correct attribution)
- Real stats (verified numbers only)
- Real photos from /images/florian/ folder
- Brand voice, visual system, and creative direction from Notion SSOT pages

**CRITICAL RULE: Never fabricate testimonials, stats, or attributions. If real content isn't available, use [PLACEHOLDER - need real content] markers. Never invent fake names or quotes.**

### Step 2: Build Interactive HTML Prototype
Using GSAP + ScrollTrigger, build a full-page interactive prototype with:
- Real content (from Step 1)
- Real images (from the /images/florian/ folder)
- The animation techniques listed below
- Clear markers for what will be native Wix vs. embed code vs. Spline

### Step 3: Break Into Implementation Blocks
Decompose the prototype into:
- Sections using Wix native scroll animations (settings specified)
- Sections that are Embed Code blocks (HTML/CSS/JS provided)
- Sections that need Spline 3D embeds (scene URL specified)
- Sections using Lottie (animation file URL specified)

### Step 4: Generate Wix Studio Build Guide
Section-by-section recipe with exact settings, embed code, and animation parameters.

### Step 5: Assemble in Wix Studio
Manual assembly following the guide. This step is done by Florian in the Wix Studio editor.

---

## Animation Techniques to Use (Ranked by Reliability)

### Tier 1: Use Confidently (native Wix Studio)
- Scroll-triggered entrance animations (fade, slide, scale)
- Mouse parallax on layered elements
- WebGL background effects
- Section background zoom on scroll
- Horizontal scroll sections

### Tier 2: Use via Embed (proven but requires code)
- GSAP text split animations (words/letters reveal on scroll)
- GSAP counter animations (numbers count up on scroll)
- GSAP pinned sections with scrub
- Custom cursor effects (inside embed only)
- Glassmorphism cards (pure CSS, works in Wix custom CSS or embed)

### Tier 3: Use via External Embed (proven, iframe-based)
- Spline 3D interactive scenes
- Scroll-based Lottie animations (via Wix App Market app)
- Custom Three.js scenes (if needed)

### Tier 4: Experimental (may hit roadblocks)
- GSAP horizontal scroll within Wix (scrollbar sync issues reported)
- Full-page GSAP takeover via single embed (performance concerns)
- Multiple Spline scenes on one page (performance)

---

## Key Tutorials & References

**Wix Studio Native Animations:**
- Scrollytelling Part 1: https://www.wix.com/studio/academy/tutorials/scrollytelling-part-1
- Spinning & Morphing Scroll: https://www.wix.com/studio/academy/tutorials/build-along-to-create-a-scroll-effect-with-spinning-and-changing-elements
- Horizontal Scroll: https://www.wix.com/studio/academy/tutorials/build-along-to-create-a-horizontal-scroll-effect
- Multi-Paced Scroll: https://www.wix.com/studio/academy/tutorials/create-a-multi-paced-scroll-effect
- Adding Scroll Animations: https://www.wix.com/studio/academy/tutorials/adding-scroll-animations

**Spline 3D + Wix Studio:**
- Official integration guide: https://docs.spline.design/integrations/integrating-with-wix-studio

**GSAP in Wix Studio:**
- Forum discussion with working examples: https://forum.wixstudio.com/t/gsap-animation-in-studio/55998
- Must load via CDN, not npm. Works inside Embed Code blocks only.

**Lottie in Wix Studio:**
- Scroll-Based Lottie App: https://www.wix.com/app-market/scroll-based-lottie-animation
- Custom Lottie on Scroll tutorial: https://lottiefiles.com/tutorials/web/custom-lottie-animation-on-scroll-or-wix-fix-CeseL64MuqM

---

## HTML Prototype (Technical Reference Only)

File: `fp-homepage-prototype-v1.html` in this same folder.

**WARNING: This prototype has FAKE CONTENT.** It was built as a technical proof-of-concept for the animation techniques only. The design session must:
1. Replace ALL copy with real approved content from Notion
2. Replace ALL testimonials with real ones (correct quotes, correct names)
3. Replace ALL stats with verified numbers
4. Replace placeholder images with real photos from /images/florian/
5. Remove "personal brands" language from the hero (violates brand guidelines)
6. Review all section copy against the brand voice skill before finalizing

**What IS useful in the prototype:**
- GSAP ScrollTrigger setup and configuration patterns
- Word-by-word text reveal on scroll (statement section)
- Horizontal scroll with pinned section (process section)
- Counter animation (stats section)
- Custom cursor implementation
- Glassmorphism card CSS
- Loading screen animation
- Progress bar tied to scroll
- Nav reveal on scroll with glassmorphic blur
- Parallax layer setup
- Grain texture overlay (matte black business card feel)

---

## Available Image Assets

Located in `/images/florian/`:

| File | Suggested Use |
|------|--------------|
| florian-editorial-lens-bw.png | Hero (current, keep) |
| florian-portrait-formal-dark.png | CTA section or About |
| florian-consulting-session-mountain.png | Brand Therapy intro |
| florian-lifestyle-sofa-lobby.png | Alternative intro |
| florian-editorial-atrium-blue.png | Statement section background |
| florian-lifestyle-coffee-contemplative.png | Blog or lifestyle |
| florian-about-seated-lounge.png | About or Story |
| florian-speaking-abaie-branding.jpg | Credibility section |
| florian-editorial-purple-gradient.png | Section accent |

---

## Existing Design Audit

File: `design-improvement-plan.md` in this same folder (created March 16, 2026).
Contains a full section-by-section audit of the current homepage with specific recommendations. The design session should reference this alongside the current document.

---

## Open Questions for the Design Session

1. Should we install Google Stitch MCP in Claude Code for mockup generation, or is the HTML prototype approach sufficient?
2. What is the exact scope: full homepage redesign, or start with hero + one section as proof of concept?
3. Which Spline 3D scene concept fits the brand (prism/lens/refraction theme)?
4. Should the design session build one mega-embed for GSAP effects, or multiple smaller embeds per section?
5. Does Florian want to test the prototype approach on a staging page in Wix Studio first before committing to the full homepage?
