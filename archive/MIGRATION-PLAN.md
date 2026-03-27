# FP. Migration Plan: From Chaos to Clean Slate
## March 26, 2026

---

## What This Document Is

This is the complete migration plan for consolidating all FP. Consulting work into a single, organized Claude Code setup. A new Claude Code session should read this document, then execute every step.

**Start the new session from: `~/Projects/`** (create it if it doesn't exist)

---

## Phase 1: Create the Folder Structure

```bash
mkdir -p ~/Projects/fp-consulting/{website,brand-assets/{florian,imagery,social-examples,brand-therapy-weekly,client-assets},content,social,video,deliverables,archive/{homepage-versions,visual-explorations,one-off-experiments}}
mkdir -p ~/Projects/fp-consulting/.claude/{rules,skills/fp-image-gen}
mkdir -p ~/Projects/_templates/new-client-setup
```

## Phase 2: Move Files from Old Location

### Brand assets (from ~/Documents/Claude/Webdesign/images/)
```
~/Documents/Claude/Webdesign/images/florian/         → ~/Projects/fp-consulting/brand-assets/florian/
~/Documents/Claude/Webdesign/images/florian/web/      → ~/Projects/fp-consulting/brand-assets/florian/web/
~/Documents/Claude/Webdesign/images/imagery/          → ~/Projects/fp-consulting/brand-assets/imagery/
~/Documents/Claude/Webdesign/images/social-examples/  → ~/Projects/fp-consulting/brand-assets/social-examples/
~/Documents/Claude/Webdesign/images/brand-therapy-weekly/ → ~/Projects/fp-consulting/brand-assets/brand-therapy-weekly/
~/Documents/Claude/Webdesign/images/client-assets/    → ~/Projects/fp-consulting/brand-assets/client-assets/
```

### Current website work
```
~/Documents/Claude/Webdesign/home-v7.html             → ~/Projects/fp-consulting/website/home-v7.html
~/Documents/Claude/Webdesign/index.html               → ~/Projects/fp-consulting/website/index.html
~/Documents/Claude/Webdesign/website-copy.md           → ~/Projects/fp-consulting/website/website-copy.md
~/Documents/Claude/Webdesign/wix-integration-research.html → ~/Projects/fp-consulting/website/wix-integration-research.html
```

### Deliverables
```
~/Documents/Claude/Webdesign/fp-brand-moodboard.html  → ~/Projects/fp-consulting/deliverables/fp-brand-moodboard.html
```

### Archive (old versions, experiments)
```
~/Documents/Claude/Webdesign/home-v1.html through home-v6.html → ~/Projects/fp-consulting/archive/homepage-versions/
~/Documents/Claude/Webdesign/visual-direction.html     → ~/Projects/fp-consulting/archive/visual-explorations/
~/Documents/Claude/Webdesign/visual-direction-v3.html  → ~/Projects/fp-consulting/archive/visual-explorations/
~/Documents/Claude/Webdesign/fp-homepage-prototype-v1.html → ~/Projects/fp-consulting/archive/homepage-versions/
~/Documents/Claude/Webdesign/prism-crystal.html        → ~/Projects/fp-consulting/archive/one-off-experiments/
~/Documents/Claude/Webdesign/prism-crystal-v2.html     → ~/Projects/fp-consulting/archive/one-off-experiments/
~/Documents/Claude/Webdesign/founder-led-companies.html → ~/Projects/fp-consulting/archive/one-off-experiments/
~/Documents/Claude/Webdesign/founder-spectrum/          → ~/Projects/fp-consulting/archive/one-off-experiments/founder-spectrum/
~/Documents/Claude/Webdesign/spectrum-slider.html       → ~/Projects/fp-consulting/archive/one-off-experiments/
```

### Delete (confirmed duplicates)
```
DELETE: ~/Documents/Claude/Webdesign/moodboard-assets/     (exact copies of images/florian/)
DELETE: ~/Documents/Claude/Webdesign copy/                  (entire duplicate directory from March 18)
```

### Investigate then archive/delete
```
~/Documents/Claude/Claude Code/                        → check if anything unique, likely delete
~/Documents/Claude/Training/                           → has old BTW content, website copy, SEO audit — archive useful pieces
~/Documents/Claude/Projects/[FP.]/                     → has Coworker outputs — archive or delete after extracting useful content
~/Documents/Claude/Local Plugins/                      → has custom plugin source files — may need for skill migration
```

### Old reference files (archive)
```
~/Documents/Claude/Webdesign/design-improvement-plan.md       → archive (superseded by Notion)
~/Documents/Claude/Webdesign/fp-project-instructions-updated.md → archive (superseded by new CLAUDE.md)
~/Documents/Claude/Webdesign/Plugin-Reference-Map.md           → archive
~/Documents/Claude/Webdesign/fp-homepage-redesign-process.md   → archive
~/Documents/Claude/Webdesign/ssot-user-preference.md           → archive
~/Documents/Claude/Webdesign/github-push-instructions.md       → archive
~/Documents/Claude/Webdesign/claude-code-audit-2026-03-26.md   → archive (this session's output)
```

---

## Phase 3: Create Project CLAUDE.md

Create `~/Projects/fp-consulting/CLAUDE.md` (~100 lines):

```markdown
# FP. Consulting — Brand Therapy

## What This Is
Florian Philippe's brand strategy consulting practice. Premium personal brand in the brand strategy space.
Website: florianp.com | Service: Brand Therapy Blueprint

## Source of Truth
ALL brand strategy, voice, visual, and content specs live in Notion. Always fetch before writing.

### Notion Page IDs (fetch these before any brand/content work)
- **Brand Voice**: 321c22dccbf980f48861fda83a94d2c6
- **Visual System**: 321c22dccbf980939b05c49dac717118
- **Creative Direction**: 321c22dccbf980dca7c2d9b7dd101d0d
- **Strategy**: 321c22dccbf980ec92bacc2b701a74ca
- **Marketing Strategy**: 321c22dccbf9804180bac0f48500f8d6
- **Content Engine**: 321c22dccbf980e0b1b2f3cafb5ee12f
- **Hook Strategy**: 321c22dccbf980bdbae0db037648c701
- **Competitive Landscape**: 321c22dccbf9801c86c7d80fc1c79c23
- **Resonance Room**: 2aac22dccbf9804692f4ca8ca497710a
- **Background & Business**: 321c22dccbf98055ada2c4ed033e3457

### Notion Databases
- **Content Database**: collection://28dc22dc-cbf9-8166-b828-000b0a4281c3
- **Content Ideas**: collection://28ec22dc-cbf9-80ff-80fd-000b560b9d39
- **Hooks Database**: collection://319c22dc-cbf9-80c3-acbd-000bcd67ebfe

### Asset Library
- **Local**: ~/Projects/fp-consulting/brand-assets/
- **Manifest**: brand-assets/ASSET-MANIFEST.md
- **GitHub**: github.com/FlorianPhil/fp-brand-assets (verify setup)

## Hard Rules (Non-Negotiable)
1. Never change typefaces. Bricolage Grotesque + Inter is locked.
2. Never use em dashes (—). Use ellipsis (...), colon, comma, or new sentence.
3. Purple #5A5CF9 is the only accent color. No warm colors ever.
4. Brand Therapy is a service/methodology name, not a company name.
5. Don't lead with "personal brand" as positioning language.
6. Website = Mode B (light/editorial). Social thumbnails/blog images = Mode A (dark).
7. Photography featured LARGE. Never reduce to small avatar.
8. Sharp-cornered buttons only. No pill buttons on website.
9. Verify URLs before including in any content. Dead links are worse than no links.
10. Fetch Notion pages before doing any brand/content/visual work. Don't rely on cached knowledge.

## Social Media Visual Direction (Updated March 2026)
Target energy: Magazine covers, not LinkedIn templates.
Reference: Johnson Gill / Lark Creatives analysis in Competitive Landscape page.
Formula: Oversized type interacting with B&W photography + purple accent.
One idea per post, massively scaled. No bullet lists, no icons.
Photography-forward. Prism imagery reserved for blog thumbnails and conceptual contexts only.

## Working With Florian
- He thinks fast, changes direction, and expects you to keep up
- Give direct recommendations, don't just present options
- Push back when something is wrong — don't be a yes-machine
- Keep responses concise. He reads diffs, not summaries.
- He's building this for himself now but will replicate for clients later
```

---

## Phase 4: Create Global CLAUDE.md

Create `~/.claude/CLAUDE.md` (~60 lines):

```markdown
# Florian Philippe

## Who I Am
Brand strategist, CMO, and founder of FP. Consulting. French, lived in 6 countries,
based in LA. Building Brand Therapy — a strategic clarity process for founders and executives.

## How I Work
- Direct and fast. Skip the preamble.
- I learn by doing. I'm using Claude to build my own brand as training for client work.
- I care about organization and clean systems. Messy folders give me anxiety.
- Notion is my single source of truth for all strategy and brand docs.
- I use Wix for my website and email campaigns.

## Preferences
- No emojis in content unless platform requires them
- No em dashes (—) anywhere, ever
- Responses should be concise and action-oriented
- When I ask for recommendations, give me YOUR opinion, not a menu of options
- When something is wrong, tell me directly

## Active Projects
Check ~/Projects/ for current client work. Each has its own CLAUDE.md.

## Key MCPs
- Notion: All brand/strategy docs
- Wix: Website and email campaigns
- Gmail: Email management
- Google Calendar: Scheduling
- Figma: Design system
- Chrome: Browser automation for Wix AI chat and other UI tasks
```

---

## Phase 5: Create .claude/rules/ Reference Files

Create `~/Projects/fp-consulting/.claude/rules/visual-system.md`:
- Cache of key visual specs from Notion (colors, fonts, modes, photography direction)
- Include the UPDATED social media direction (magazine-cover approach, photography-forward, prism reserved for blog/conceptual only)
- Include Johnson Gill visual formula adapted for FP.
- ~150 lines, loaded on-demand when Claude works with visual files

Create `~/Projects/fp-consulting/.claude/rules/brand-voice.md`:
- Cache of key writing rules from Notion
- Hard rules, calibration scores, anti-patterns
- ~100 lines

---

## Phase 6: Migrate Skills to Global ~/.claude/skills/

### Reusable skills (work across clients):

**~/.claude/skills/fp-wix-blog/SKILL.md**
→ PASTE FROM COWORKER (Florian must provide the content)

**~/.claude/skills/fp-wix-email/SKILL.md**
→ PASTE FROM COWORKER (Florian must provide the content)

**~/.claude/skills/brand-therapy-weekly/SKILL.md**
→ Copy from ~/Documents/Claude/Scheduled/brand-therapy-weekly/SKILL.md
Content already captured in this session (scans Notion, proposes hooks, triggers blog + email workflow)

**~/.claude/skills/daily-pm/SKILL.md**
→ Copy from ~/Documents/Claude/Scheduled/daily-pm/SKILL.md
Content already captured (checks Gmail, scans Notion tasks across all projects, presents grouped list)

### Register as scheduled tasks:
- brand-therapy-weekly: Desktop scheduled task, Monday mornings
- daily-pm: Desktop scheduled task, every weekday morning

---

## Phase 7: Populate Memory

Create memory files in `~/.claude/projects/-Users-florian-Projects-fp-consulting/memory/`:

### From Coworker auto-memory (Florian must provide the 4 entries)
→ Migrate each as a memory file with proper frontmatter

### From this audit session
Create these memory files:

**feedback_direct-recommendations.md**
```
---
name: direct-recommendations
description: Florian wants direct opinions, not menus of options
type: feedback
---
Give direct recommendations. Don't present 3 options and ask which one.
**Why:** Florian explicitly said "I really need direction here" and "don't just agree with what I say."
**How to apply:** When there's a decision to make, state your recommendation and reasoning. Only present options when genuinely uncertain or when the choice has significant trade-offs.
```

**feedback_concise-responses.md**
```
---
name: concise-responses
description: Keep responses short, Florian reads diffs not summaries
type: feedback
---
Keep responses concise and action-oriented. No trailing summaries.
**Why:** Florian processes fast and gets frustrated by verbose responses.
**How to apply:** Lead with the answer or action. Skip preamble. If code was written, don't explain what you just did — he can read the diff.
```

**feedback_organization-matters.md**
```
---
name: organization-matters
description: Clean folder structure and systems matter deeply to Florian
type: feedback
---
Florian cares deeply about clean organization. Messy folders, duplicate files, and unclear structure cause real friction.
**Why:** Self-described OCD about file organization. The Webdesign folder mess was a source of visible frustration.
**How to apply:** When creating files, always use clear naming and put things in the right directory. Never dump files in the project root. Propose folder structure before creating assets.
```

**project_migration-complete.md**
```
---
name: migration-complete
description: Consolidated from iCloud to ~/Projects/ on March 26, 2026
type: project
---
Migrated all FP. Consulting work from ~/Documents/Claude/Webdesign/ (iCloud) to ~/Projects/fp-consulting/ (local).
**Why:** iCloud sync caused risks with Claude Code and .claude directories. Multiple duplicate folders existed.
**How to apply:** Never create files in ~/Documents/Claude/. All work goes in ~/Projects/fp-consulting/.
```

**project_visual-direction-shift.md**
```
---
name: visual-direction-shift
description: Moving away from prism-heavy social media toward magazine-cover photography style
type: project
---
As of March 26, 2026, Florian wants to shift social media visual direction:
- AWAY FROM: prism/3D render imagery dominating social posts
- TOWARD: Johnson Gill / Lark Creatives magazine-cover approach
- Formula: oversized type interacting with B&W photography + purple accent
- Prism imagery STAYS for blog featured images and website conceptual sections
- This requires updating the Visual System and Creative Direction pages in Notion
**Why:** Prism imagery reads as "AI-generated" on social media. Photography-forward approach is more authentic and performs better (Johnson Gill's magazine posts get 3-4x engagement vs casual posts).
**How to apply:** When creating social media visuals, default to B&W photography of Florian with oversized type and purple accent. Only use prism imagery for blog thumbnails and slide/keynote backgrounds.
```

**user_florian-role.md**
```
---
name: florian-role
description: Florian is a brand strategist building his consulting practice and learning AI automation
type: user
---
Florian Philippe is a brand strategist, CMO, and founder of FP. Consulting.
He's building Brand Therapy as his flagship service. Currently focused on his own brand
(website, social media, content) but plans to replicate this system for future clients.
He's learning Claude Code as a power tool and wants to automate as much of the marketing
pipeline as possible. He thinks like a CEO but executes like a one-person team.
French background, cosmopolitan worldview, warm but direct communication style.
**How to apply:** Frame recommendations in terms of both immediate need (his brand) and
future scalability (client work). Treat him as a sophisticated user who wants to understand
the system, not just get output.
```

**reference_notion-workspace.md**
```
---
name: notion-workspace
description: Notion workspace structure for FP. Consulting with all page IDs
type: reference
---
Notion is the SSOT for all brand strategy. Key pages under Florian P. Consulting > Strategy:
- Brand Strategy (parent): 321c22dccbf980f4bd3ed9b6a3d47692
- Brand Voice: 321c22dccbf980f48861fda83a94d2c6
- Visual System: 321c22dccbf980939b05c49dac717118
- Creative Direction: 321c22dccbf980dca7c2d9b7dd101d0d
- Strategy: 321c22dccbf980ec92bacc2b701a74ca
- Marketing Strategy: 321c22dccbf9804180bac0f48500f8d6
- Content Engine: 321c22dccbf980e0b1b2f3cafb5ee12f
- Hook Strategy: 321c22dccbf980bdbae0db037648c701
- Competitive Landscape: 321c22dccbf9801c86c7d80fc1c79c23
- Background & Business: 321c22dccbf98055ada2c4ed033e3457
- Archive (DO NOT USE): 321c22dccbf980efbe32d08f50117dd8
**How to apply:** Always fetch the relevant Notion page before doing brand/content/visual work.
```

---

## Phase 8: Update Notion (Visual System + Creative Direction)

After migration is complete, update the Notion Visual System and Creative Direction pages to reflect the social media direction shift:

### Visual System updates:
- Add a new section under "Two Visual Modes" clarifying that social media uses a photography-forward approach (Johnson Gill magazine-cover formula), not Mode A 3D renders
- Prism/3D imagery is reserved for: blog featured images, slide decks, website dark sections
- Social posts use: B&W photography of Florian + oversized type + purple #5A5CF9 accent
- Add Johnson Gill formula summary (adapted for FP.) as a subsection

### Creative Direction updates:
- Update LinkedIn/Social Posts section with the magazine-cover formula
- Add A/B testing recommendation (2-3 layout variations per concept)
- Add two-mode feed structure (magazine-cover brand posts + casual personal posts)

---

## Phase 9: Verify and Confirm

After all phases complete:
1. Run `ls -R ~/Projects/fp-consulting/` to verify structure
2. Confirm CLAUDE.md loads by starting a fresh session from `~/Projects/fp-consulting/`
3. Test a Notion fetch to confirm page IDs work
4. Verify brand-assets contain all images
5. Confirm old ~/Documents/Claude/Webdesign/ can be archived or deleted

---

## What Florian Still Needs to Provide
1. **fp-wix-blog SKILL.md content** — paste from Coworker
2. **fp-wix-email SKILL.md content** — paste from Coworker
3. **4 Coworker auto-memory entries** — paste the text
4. **Confirmation to delete** ~/Documents/Claude/Webdesign copy/ and moodboard-assets/
5. **GitHub repo verification** — is fp-brand-assets actually set up?

---

## Chrome Extension Access
Yes, Claude Code has the "Claude in Chrome" MCP with full browser automation:
navigate, click, type, read page content, screenshots, file upload. The Wix AI chat
workflow from fp-wix-email will work identically in Claude Code. Scheduled tasks
running as Desktop tasks also have Chrome access since they run on your machine.

## Why Not Cloud Environments
Cloud environments run on Anthropic servers with fresh clones. They cannot access
local files (your images), local Chrome, or local MCP servers. Your workflows
(Wix AI chat, local image generation, brand asset access) all require local.
Use Desktop scheduled tasks, not Cloud tasks. Revisit cloud when your workflows
are API-only.
