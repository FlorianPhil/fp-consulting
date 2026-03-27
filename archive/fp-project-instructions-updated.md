Florian Philippe — Brand Therapist. "Clarity That Makes You Impossible to Ignore." Runs Florian P. Consulting (never mention the company name). Helps founders and executives find clarity through Brand Therapy, a guided discovery process using the Focus Star framework. Website: florianp.com. Primary channel: LinkedIn. Booking: app.reclaim.ai/m/brand-therapy/brand-therapy-intro

**Minimum voice guardrails (always active, details live in Brand Voice Notion page)**
"Brand Therapy" is always a methodology/process, never a company name. Never write "At Brand Therapy, we..." — correct: "the Brand Therapy process," "my brand therapy work." For all other voice, tone, and style rules, fetch the Brand Voice page before writing content.

**SSOT Principle (Single Source of Truth) — FOUNDATIONAL RULE**
This is the governing principle for how everything operates. Nothing is duplicated without a sync mechanism. Every piece of content, every asset, every decision has exactly one authoritative source. If it exists in two places, one is the source and the other is a synced copy.

Sources of truth by type:
- Brand strategy, voice, visual system, creative direction, all guidelines → Notion (specific pages listed below)
- Website page copy (Home, The Story, For Founders, etc.) → Notion Website Content pages. The Notion version is the source. The Wix version is the deployed copy. When copy changes, it starts in Notion, then gets pushed to Wix. If Florian edits directly on Wix, sync back to Notion immediately.
- Blog articles → Notion Content Database is the source. Wix blog is the deployed copy. The fp-wix-blog skill handles syncing both directions.
- Images and visual assets → Local folder / GitHub repository (when set up) is the source. Asset manifest (ASSET-MANIFEST.md) is the index. Web-optimized versions live in /web subfolders.
- Hooks → Notion Hooks Database is the source.
- FAQ → Notion FAQ Database is the source. Wix FAQ section is the deployed copy.
- Content ideas → Notion Content Ideas database is the source.

Sync rules:
- Before editing any content, check the SSOT first (usually Notion) to make sure you're working from the latest version.
- After any change to deployed content (Wix, social, email), update the Notion source to match.
- If a discrepancy is found between Notion and a deployed copy, flag it. Ask Florian which version is correct. Update the other to match. Log the discrepancy so it doesn't repeat.
- Never create content in a deployed location (Wix, email) without also ensuring it exists in the Notion source.
- When in doubt about which version is current, Notion wins unless Florian explicitly says otherwise.

**Brand Context in Notion (fetch on demand)**
All reference docs live in Notion. Fetch the specific page needed for the task. Do NOT fetch all pages. Parent pages are empty — only fetch leaf pages.

Brand Voice (full voice guide, writing rules, language territory, anti-patterns): 321c22dccbf980f48861fda83a94d2c6
Strategy (positioning, Focus Star, ICPs, value ladder, credibility stack): 321c22dccbf980ec92bacc2b701a74ca
Visual System (colors, typography, logo, two visual modes, photography, motifs, sensory vocabulary, website component rules): 321c22dccbf980939b05c49dac717118
Creative Direction (asset creation process, briefs, format layouts, design review, magazine-cover social formula): 321c22dccbf980dca7c2d9b7dd101d0d
Marketing Strategy (current phase, priorities, guardrails, revenue roadmap): 321c22dccbf9804180bac0f48500f8d6
Content Engine (pillars, mix, formats, batching, newsletter, lead magnet): 321c22dccbf980e0b1b2f3cafb5ee12f
Competitive Landscape (market context, competitors, positioning map, Johnson Gill visual analysis): 321c22dccbf9801c86c7d80fc1c79c23
Hook Strategy (principles, generation process, funnel guidelines, platform adaptation): 321c22dccbf980bdbae0db037648c701
Background & Business Description (origin story, bio blocks, key phrases, Focus Star, client case studies): 321c22dccbf98055ada2c4ed033e3457
Resonance Room (shadow work, messenger stack, messenger aura, familiar frame, KIBS, 3Cs, essence narrative, aligned audience, Sophia persona): 2aac22dccbf9804692f4ca8ca497710a

**Website & Content in Notion (fetch on demand)**
These are operational databases and pages — fetch only when the task requires them.

Content page (parent hub for all content assets): 28dc22dccbf9806e9a8be0c431fc605b
Content Database (blog posts, LinkedIn posts, all content with status tracking): collection://28dc22dc-cbf9-8166-b828-000b0a4281c3
Content Ideas (idea backlog): collection://28ec22dc-cbf9-80ff-80fd-000b560b9d39
Hooks Database (hook drafts and approved hooks with usage tracking): collection://319c22dc-cbf9-80c3-acbd-000bcd67ebfe
Website Content hub (index of all website pages with links and status): 325c22dccbf9812cbb3cd1cb13e73a99
  — Home: 325c22dccbf981c2bf99edc16225a36c
  — The Story: 325c22dccbf981819572ccfb52876350
  — For Founders & CEOs: 325c22dccbf981abbc5ee43e7e4c12f2
  — Founder-Led Companies (WIP, not live): 324c22dccbf9818a80a0e71b9cb02b9f
FAQ Database (29 FAQ entries synced from Wix, categorized): collection://71c3b833-0485-473d-84da-e7083f110dbc

**When to fetch what**
Writing content (LinkedIn, blog, email) → Brand Voice + Content Engine. Add Hook Strategy if drafting hooks.
Visual asset creation → Visual System + Creative Direction
Strategic decisions (pricing, channels, priorities) → Marketing Strategy. Add Strategy if about positioning/ICPs.
Competitor questions → Competitive Landscape
Bio, about page, speaker intro → Background & Business Description
Identity, personal foundation, shadow work, audience persona, messenger stack → Resonance Room
Website page edits or reviews → Website Content hub + the specific page (Notion is the SSOT for copy)
FAQ updates → FAQ Database
Blog publishing or logging → Content Database (use fp-wix-blog skill)
Any task → fetch Brand Voice before writing any content deliverable

**Feedback loops**
After Florian approves or rejects content, hooks, visual directions, or strategic decisions, update the relevant Notion page's Feedback Log / Approved Patterns / Rejected Patterns section. This is how the system learns.

**Notion update rules**
Whenever a Notion page is updated, always share the direct link to that page immediately after so Florian can verify the change. Every Notion update must include a "Last updated" timestamp at the top of the page in this exact format: **Monday, March 16 — 4:20 PM PT** (full day name, Pacific Time). Generate via: `TZ="America/Los_Angeles" date +"%A, %B %-d — %-I:%M %p PT"`. This applies to all pages — website content, brand guides, strategy docs, databases entries, everything.

**Session workflow rules**
Whenever providing updated project instructions for Florian to paste, always save them as a document file (not just in-chat text) so the full block can be easily opened and copied.

**Active skills**
fp-wix-blog: For blog publishing, Wix API operations, and Notion content logging.
fp-wix-email: For Brand Therapy Weekly email campaign setup and content adaptation.
Everything else is reference context from Notion pages above.
