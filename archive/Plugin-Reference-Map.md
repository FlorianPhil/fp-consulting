# Plugin Reference Map — FP. Cowork Setup

**Last updated: March 18, 2026**

---

## The Problem (and fix)

You have **two copies** of four plugins installed: the original Anthropic marketplace versions (remote) and your customized FP. versions (local). They share the same skill names, so when you call a command, it's ambiguous which version runs.

**Fix:** Disable the four remote/Anthropic marketplace plugins. Keep only your customized local versions active. They are your SSOT.

---

## How to Disable Remote Plugins

1. Open the **slash command menu** (type `/` in chat)
2. Scroll to **Manage plugins** at the bottom
3. You'll see each plugin listed twice. The ones to **disable** are the Anthropic marketplace originals. They will NOT have "(local)" or similar label — look for the ones that came from the marketplace.
4. Toggle them off (disable, don't uninstall — so you can re-enable later to check for updates)

The four to disable:
- Marketing (marketplace)
- Productivity (marketplace)
- Sales (marketplace)
- Design (marketplace)

After disabling, you should see only ONE entry per category in the menu.

---

## What You Keep Active (Local / Customized)

These are your FP.-customized versions. Every skill below was modified to include your brand context, Notion page IDs, ICPs, content pillars, and strategic guardrails.

### Marketing Plugin (local v1.1.0)

| Skill | What was customized |
|---|---|
| `brand-voice` | Added Notion SSOT fetch (page `321c22d...`), voice DNA, hard rules (no em dashes), anti-patterns, quality gate |
| `campaign-planning` | Added Phase 1 context, 3 ICPs, strategic guardrails (no new products until 10 clients, etc.) |
| `competitive-analysis` | Added competitive landscape Notion page, positioning summary, category definition, key differentiators |
| `content-creation` | Added 5 content pillars, content mix ratios, GEO-over-SEO strategy, Notion page IDs for Content Engine and Strategy |
| `performance-analytics` | Added analytics tools list (GA4, Wix, GSC, SEMrush, LinkedIn), Phase 1 leading indicators |

**Commands (7):** brand-review, campaign-plan, competitive-brief, draft-content, email-sequence, performance-report, seo-audit

### Design Plugin (local v1.1.0)

| Skill | What was customized |
|---|---|
| `accessibility-review` | Customized for FP. brand color combinations |
| `design-critique` | Evaluates against FP. visual system |
| `design-handoff` | Specs for Wix implementation specifically |
| `design-system-management` | Manages FP. design tokens and component library (renamed from `design-system`) |
| `user-research` | Same as remote |
| `ux-writing` | Writes microcopy for florianp.com in Florian's voice (renamed from `ux-copy`) |

**Note:** The local Design plugin has 6 commands that the remote version didn't have: accessibility, critique, design-system, handoff, research-synthesis, ux-copy

**Skills renamed from remote:**
- `ux-copy` (remote) → `ux-writing` (local)
- `design-system` (remote) → `design-system-management` (local)

**Skills removed from local:** `research-synthesis` (still available as a command)

### Sales Plugin (local v1.1.0)

| Skill | What was customized |
|---|---|
| `account-research` | Identical to remote (no changes) |
| `call-prep` | Updated description to reference Wix CRM, Gmail, Google Calendar instead of generic CRM |
| `competitive-intelligence` | Pre-configured seller context (Florian Philippe, Brand Therapist, Brand Therapy service) |
| `create-an-asset` | Pre-configured seller context for Florian Philippe |
| `daily-briefing` | Rebranded from "Daily Sales Briefing" to "Daily Briefing", references Wix CRM and Gmail |
| `draft-outreach` | Updated proof points to use credibility stack (10 years, 6 countries, Acer, NYC incubator) |

**Commands (3):** call-summary, forecast, pipeline-review

### Productivity Plugin (local v1.1.0)

| Skill | What was customized |
|---|---|
| `memory-management` | Updated examples to use Brand Therapy language instead of generic sales examples |
| `task-management` | Added Notion + Apple Reminders context, content pipeline section, structured task categories |

**Commands (2):** start, update

---

## Plugins That Are NOT Duplicated (no action needed)

These are standalone and have no conflicts:

| Plugin/Skill | Location |
|---|---|
| `fp-wix-blog` | Custom skill (your own) |
| `fp-wix-email` | Custom skill (your own) |
| `doc-coauthoring` | Anthropic built-in |
| `web-artifacts-builder` | Anthropic built-in |
| `skill-creator` | Anthropic built-in |
| `theme-factory` | Anthropic built-in |
| `mcp-builder` | Anthropic built-in |
| `internal-comms` | Anthropic built-in |
| `canvas-design` | Anthropic built-in |
| `algorithmic-art` | Anthropic built-in |
| `xlsx` | Anthropic built-in |
| `pptx` | Anthropic built-in |
| `pdf` | Anthropic built-in |
| `docx` | Anthropic built-in |
| `schedule` | Anthropic built-in |
| `cowork-plugin-management` | Anthropic built-in |

---

## How to Handle Future Anthropic Updates

When Anthropic updates the marketplace plugins:

1. **Re-enable** the remote plugin temporarily
2. **Diff** the updated remote skill against your local version
3. **Merge** any improvements into your local copy
4. **Disable** the remote plugin again

This keeps your local versions as SSOT while still benefiting from Anthropic's improvements.

---

## Quick Command Reference

When calling skills after cleanup, you'll use these (all will route to your local/customized versions):

```
/marketing:brand-voice
/marketing:campaign-plan
/marketing:draft-content
/marketing:competitive-brief
/marketing:email-sequence
/marketing:performance-report
/marketing:seo-audit
/marketing:brand-review

/design:ux-copy
/design:critique
/design:accessibility
/design:design-system
/design:handoff
/design:research-synthesis

/sales:call-prep
/sales:call-summary
/sales:forecast
/sales:pipeline-review

/productivity:start
/productivity:update
```
