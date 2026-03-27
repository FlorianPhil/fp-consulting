# FP. Website Design Improvement Plan

**Prepared: March 16, 2026**
**Scope: florianp.com homepage redesign - improvement, not rebuild**

---

## The Diagnosis

Your hero section is the strongest thing on the page. Bold headline, signature B&W lens photo, clear value prop. It feels like a brand therapist's website. The problem is that everything below the hero drops in quality dramatically. The rest of the page feels like a first draft that never got designed.

Here's the section-by-section breakdown.

---

## Section-by-Section Audit

### 1. Hero (KEEP - minor polish)
**What works:** Massive headline, editorial lens photo, "Clarity That Makes You Impossible to Ignore" is a killer line, clean light background.
**What to improve:** The CTA button ("Book Your Free Intro Call") gets lost below the fold. On mobile, the image will push the CTA even further down. Consider making the CTA visible within the first viewport, either as a pill button below the subtitle or as a sticky element.

### 2. Brand Therapy Intro Section (NEEDS REDESIGN)
**Current state:** Text shoved to the right half of the page. Entire left side is empty gray space. Feels unfinished.
**Problem:** This is your "what I do" section and it looks like a placeholder. No imagery, no visual anchor, no reason for the eye to stop.
**Recommendation:** Use a two-column layout with a large editorial photo of you on the left (the consulting session photo or the sofa lobby shot would work perfectly) and the text on the right. Or go full-width with the text overlaying a subtle background treatment. This section needs to feel as intentional as the hero.

### 3. Testimonials (NEEDS MAJOR REDESIGN)
**Current state:** A LinkedIn embed widget next to a text testimonial. The LinkedIn widget screams "I embedded my LinkedIn profile" rather than "I'm a credible professional."
**Problems:**
- LinkedIn widget looks like a technical artifact, not a design choice
- Testimonial text is long and unformatted with no visual hierarchy
- Small headshot photo, no names styled prominently
- No visual rhythm between testimonials
**Recommendation:** Replace the LinkedIn embed entirely. Build a clean testimonial section: large pull-quote style with the most powerful line in huge type ("He's a fucking unicorn" deserves to be 60px bold), then the attribution with name, title, and company below. Use a horizontal scroll or numbered tabs. Think about how Lark Creatives showcases client work as bold visual blocks - apply that same energy to your social proof.

### 4. Featured On (NEEDS STRENGTHENING)
**Current state:** Two publication logos floating in space. Looks sparse and undermines credibility.
**Recommendation:** Either add more logos (even podcast appearances, speaking events, or collaborations count) or redesign this as a horizontal marquee strip. A single row of 5-8 logos on a subtle background carries more weight than 2 logos in a sea of white space. If you only have 2, combine this section into the hero or testimonials area as a subtle trust bar.

### 5. The Process - Dark Section (NEEDS COMPLETE REDESIGN)
**Current state:** Dark background with tiny purple icons and no visible text. The icons are so small they're unreadable. Massive amounts of dead space.
**Problems:** This is the worst section on the page. The dark mode switch is jarring after the light sections, the icons communicate nothing, and the content (Discovery Call, Blueprint, Authority Takeover, Show Up) is completely invisible without scrolling into each subsection.
**Recommendation:** Keep it dark if you want (it provides contrast), but make it work:
- Show all 4 steps visually in a horizontal timeline or stacked vertical blocks
- Each step gets a bold number (01, 02, 03, 04), a short headline, and a one-line description - all visible without interaction
- Use larger icons or replace icons with bold typography
- Consider a vertical layout that works naturally on mobile (stacked cards)
- Reference: the Lark Creatives approach with bold type on dark backgrounds

### 6. AI/Identity Quote Section (GOOD CONTENT, WEAK EXECUTION)
**Current state:** Powerful text on a gray background. "Your identity becomes your biggest competitive asset" is a strong statement.
**Problem:** It reads as a text block, not a design moment. No visual emphasis beyond the purple highlight on "your identity."
**Recommendation:** Make this a full-bleed statement section. Massive type, tighter. Black text on off-white, or white text on dark. Let the statement breathe with generous padding. This should feel like a magazine spread, not a paragraph. Add a subtle editorial photo or prism motif in the background.

### 7. What Strategic Clarity Does (NEEDS VISUAL UPGRADE)
**Current state:** Three columns of text with "Show More" toggles. Reads like documentation, not like a premium service offering.
**Recommendation:** Turn each column into a card with a bold header, short description, and visual element (icon, number, or accent line). Make the cards feel like distinct value propositions with clear visual hierarchy. The "Show More" pattern hides your best selling points - consider showing the full content by default on desktop.

### 8. CTA Section - "Your next real brand conversation is free" (NEEDS POLISH)
**Current state:** Dark background with a diagonal slash transition from the section above. The diagonal feels dated (2018 web design). "Book Your Intro Call" link is barely visible.
**Recommendation:** Clean straight-edge transition. Make the CTA button prominent - large, purple (#5A5CF9), impossible to miss. Consider splitting this into: bold headline on the left, your portrait photo on the right, CTA button centered below. This is the conversion moment - treat it like the most important section after the hero.

### 9. Stats Section (NEEDS VISUAL IMPACT)
**Current state:** "250%, 500%, 1M+, 1.2M+" as plain text. No visual weight.
**Recommendation:** Large bold numbers with the purple accent, tight descriptions below each. These should feel like bold data points, not a paragraph. A horizontal row on desktop, 2x2 grid on mobile. Consider adding a subtle animation (count-up) when scrolling into view.

### 10. FAQ Section (DECENT - minor improvements)
**What works:** Category tabs, numbered accordion items, purple accent on active state.
**What to improve:** The purple background behind the FAQ section feels heavy. Consider keeping the FAQ on a light background to maintain the editorial feel. The FAQ is a massive section - consider whether all categories need to live on the homepage or if some should move to a dedicated FAQ page.

---

## Overarching Design Problems

### Photography Disappears After the Hero
Your Visual System doc says "Photography is a PRIMARY design element" and "Alternating rhythm: photography sections alternate with text-dominant sections." This isn't happening. After the hero, there are zero photos of you on the entire homepage. You have an incredible library of editorial photography (the formal dark portrait, the consulting session, the sofa lobby shot, the atrium blue image) and none of it appears on your homepage.

**Fix:** Weave photography into at least 3 sections below the hero. The Brand Therapy intro, the CTA section, and ideally one more spot.

### No Visual Rhythm
The page goes: light hero, light text, light testimonials, light featured-on, dark process, light quote, light cards, dark CTA, light stats, purple FAQ, purple footer. There's no deliberate alternation. It feels accidental.

**Fix:** Create a clear pattern: light section (with photo), light section (text), dark or accent section, light section (with photo), dark CTA. Each transition should feel intentional.

### Mobile-First Is Not Happening
Many sections rely on side-by-side layouts that will stack awkwardly on mobile. The Process section's tiny icons will be even more lost. The testimonial with the LinkedIn embed will feel clunky.

**Fix:** Design every section mobile-first. If it looks good stacked vertically in a single column at 375px wide, it will look even better on desktop. Prioritize vertical photography (portrait orientation) since that fills a mobile viewport naturally.

### The "Let's Chat" Wix Widget
The Wix chat bubble in the bottom-right is generic and doesn't match the brand. It feels like a default template element.

**Fix:** Either customize it to match the brand (purple, rounded, branded copy) or remove it in favor of a stronger CTA strategy throughout the page.

---

## What to Steal from Lark Creatives

The Lark Creatives site works because of a few key patterns that translate directly to your brand:

1. **Bold, full-bleed visual blocks** - Each case study / client showcase fills the viewport. Nothing feels small or timid. Apply this to your testimonials and process sections.

2. **Photography as the dominant element** - Portraits are large, confident, and cropped boldly. Your editorial photography (especially the formal dark portrait and the atrium blue shot) deserves this same treatment.

3. **Clear dark/light section alternation** - They alternate between dark portfolio blocks and light content sections. The rhythm feels intentional. Your site needs this discipline.

4. **Sticky navigation with service categories** - Their bottom nav bar stays visible while scrolling. Consider whether a sticky CTA or a persistent "Book a Call" element would serve you better than the generic chat widget.

---

## 2026 Trend Alignment

Based on current web design direction, here's what to prioritize:

### Glassmorphism / Glass UI (Priority Direction)
Apple is relaunching glass effects across their ecosystem and it's becoming a dominant design language again in 2026. This is a perfect fit for your brand because you already have the conceptual foundation: the prism, the lens, light passing through glass. Glassmorphism takes that from a metaphor to an actual UI treatment.

**What glassmorphism looks like in practice:**
- Frosted glass cards with `backdrop-filter: blur()` and semi-transparent white backgrounds
- Subtle border highlights that catch light (1px white border at ~20% opacity)
- Soft shadows with depth layers
- Content cards that feel like they're floating on glass panels over your photography or gradient backgrounds

**Where to apply it on your site:**
- **Testimonial cards** - Frosted glass panels over a subtle purple gradient or your editorial photography. The testimonial text sits on a translucent card that lets the background come through.
- **Process steps** - Glass cards on the dark section. Each step becomes a frosted panel floating over the dark background with the purple icon glowing through.
- **Stats section** - Each stat number on its own glass card, arranged in a row.
- **Navigation** - A frosted glass nav bar that becomes translucent as you scroll (like Apple's current navigation).
- **CTA section** - The booking form or button area on a glass panel overlaying your portrait photo.

**How it connects to your brand metaphor:**
Your entire visual identity is built on the idea of clarity through a prism/lens. Glass UI makes that literal. Visitors experience the "looking through glass to see clearly" concept at the interface level. The frosted panels represent the process of gaining clarity: you can see something through them, but the Brand Therapy process brings it into sharp focus.

**Technical notes for Wix implementation:**
Glass effects are pure CSS (`backdrop-filter: blur(10px)`, `background: rgba(255, 255, 255, 0.15)`, `border: 1px solid rgba(255, 255, 255, 0.2)`). Wix supports custom CSS in Velo, or you can achieve similar effects with Wix's built-in transparency and shadow controls. For best results, glass cards need a rich background behind them (photography, gradients, or your dark mode).

**Anti-pattern:** Don't go full glassmorphism on everything. Glass works best as an accent on 2-3 key sections, not as the entire page treatment. Your light editorial sections should stay clean and solid. Glass shines most on dark sections or over photography.

### Oversized Typography
You're already doing this in the hero. Extend it to section headers throughout the page. "The Process" headline should feel as bold as "Clarity That Makes You Impossible to Ignore."

### Intentional Color Blocking
Your purple (#5A5CF9) is distinctive. Use it more strategically as full-bleed section backgrounds for 1-2 key moments (not the entire FAQ + footer). When purple appears, it should feel like an event.

### Mobile-First Vertical Imagery
Portrait-orientation photography fills a mobile viewport naturally. Your editorial portraits are already shot this way - use them.

### Micro-Interactions
Subtle hover states on cards, smooth scroll transitions between sections, and a count-up animation on the stats section add polish without complexity. Glass cards can have subtle hover effects where the blur intensity shifts slightly.

### Accessibility-First
Ensure all text/background combinations hit WCAG AA contrast ratios. Your purple on white is borderline - verify it meets standards. Glass effects need extra attention here: text on translucent backgrounds must remain readable across all viewport sizes. The European Accessibility Act is now in effect.

---

## Prioritized Action Plan

### Phase 1: High-Impact, Low-Effort (Do First)
1. Add 3-4 editorial photos throughout the page (Brand Therapy intro, CTA section, one more)
2. Replace the LinkedIn embed with a designed testimonial block
3. Fix the Process section - show all 4 steps with visible headlines
4. Make the CTA button in the conversion section larger and purple

### Phase 2: Section Redesigns
5. Redesign the Brand Therapy intro as a photo + text two-column layout
6. Redesign the testimonials as large pull-quote cards
7. Fix the stats section with bold numbers and visual weight
8. Remove the diagonal slash transition - use clean edges

### Phase 3: Polish and Optimization
9. Strengthen the Featured On section or merge it
10. Optimize all sections for mobile-first (test at 375px)
11. Establish a clear light/dark section rhythm
12. Customize or remove the Wix chat widget
13. Add subtle micro-interactions (hover states, scroll animations)

---

## Image Assets Available

Your renamed image library includes strong options for each section:

| Image | Best Use |
|-------|----------|
| florian-editorial-lens-bw.png | Hero (current, keep) |
| florian-portrait-formal-dark.png | CTA section or About section |
| florian-consulting-session-mountain.png | Brand Therapy intro section |
| florian-lifestyle-sofa-lobby.png | Alternative for Brand Therapy intro |
| florian-editorial-atrium-blue.png | Statement/quote section background |
| florian-lifestyle-coffee-contemplative.png | Blog or lifestyle section |
| florian-about-seated-lounge.png | About or Story section |
| florian-speaking-brand-touchpoints.jpg | Credibility/speaking section |
| florian-editorial-purple-gradient.png | Section accent or hero alternative |

---

## Next Steps

Once you've reviewed this plan, I can:
- Build HTML mockups of specific sections for you to review before implementing in Wix
- Update the Creative Direction and Visual System pages in Notion based on decisions made
- Create mobile-first wireframes for the priority sections
- Start implementing changes section by section

The goal is to make the rest of your homepage match the energy of your hero section. You've already proven you can be bold - now the whole page needs to follow through.
