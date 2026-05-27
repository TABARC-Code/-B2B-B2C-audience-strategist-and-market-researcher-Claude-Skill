# audience-profiles

**Author:** TABARC-Code  
**Version:** 1.0.4 
**Works with:** Claude (claude.ai, Claude Code, Claude Desktop)

---

A reusable Claude skill for building, applying, and improving audience personas. Built for newsletter writers, content creators, and anyone who makes decisions about what to write, what to sell, and how much to charge — and wants those decisions to be grounded in something more reliable than intuition.

The skill was built for the TABARC-Gaming / Games Haven Substack context, but the methodology is general. If you have an audience you want to understand properly, it works.

---

## What It Does

So most audience research produces a flat document nobody reads twice. A paragraph about demographics. A list of "pain points." A vague before/after that sounds like every other before/after. It goes in a folder and gets forgotten.

This skill does something different. It builds a persona in three layers — core profile, psychological depth, buying behaviour — and then actively routes that persona into decisions. Content, offers, pricing, product. Each domain has its own protocol inside the skill. You don't just have a persona; you use it.

The other difference is the Kaizen loop. The persona isn't a one-time deliverable. It versioned. It improves with every application. When a reader replies with specific language, that goes in verbatim. When an offer doesn't land the way you expected, the buying profile gets updated. Nothing is deleted — old versions are dated and archived so drift is visible.

---

## Contents

```
audience-profiles/
├── SKILL.md                          # Entry point — routing and protocols
└── references/
    ├── persona-framework.md          # Full question bank (58 questions, 3 layers)
    ├── application-playbook.md       # Domain protocols: content, offers, pricing, product
    └── kaizen-loop.md                # Improvement protocol and versioning system
```

---

## Installation

### Claude.ai

1. Download `audience-profiles.skill`
2. Go to **Settings → Profile → Skills**
3. Click **Add skill** and upload the file
4. The skill becomes available in all future conversations

### Claude Code / Claude Desktop

```bash
claude skill install audience-profiles.skill
```

Or place the unpacked `audience-profiles/` folder in your skills directory and Claude will detect it automatically.

---

## How to Use It

Once installed, the skill triggers on phrases like:

- "who is my audience"
- "build a persona for my Substack"
- "what does my reader want"
- "help me create an offer"
- "what angle should I take for this post"
- "price this for my audience"
- "who am I writing for"

You don't need to name the skill. Just talk about your audience the way you'd normally would.

### Quick Examples

**Building a persona:**
```
I run a Substack about tabletop gaming strategy. Help me build an audience persona.
```

**Applying a persona to content:**
```
Using my audience profile, help me write an intro for a post about getting started with 
Flesh and Blood.
```

**Pricing with the persona:**
```
I'm thinking of launching a paid tier at £7/month. Run my audience profile against this.
```

**Improving the persona after feedback:**
```
A subscriber replied saying "I always feel like I'm three steps behind everyone else at 
the table." What does this update in the profile?
```

---

## The Three Layers

The persona framework works in layers. You don't always need all three.

**Layer 1 — Core Profile.** Always completed. Role, goals, pains, stakes, discovery, trigger to subscribe. This is the foundation.

**Layer 2 — Psychological Profile.** Add this for content and copywriting decisions. Hopes, fears, internal dialogue on open, emotional triggers, what keeps them, what loses them.

**Layer 3 — Buying Profile.** Add this for offer, pricing, and product decisions. Willingness to pay, objections, decision dynamics, before/after, how they'd recommend it.

---

## The Kaizen Loop

The skill includes a structured improvement protocol. After every significant application — publishing a post, launching an offer, making a pricing change — you run a brief note:

- What did this reveal about the audience that wasn't in the profile?
- What assumption changed?
- What's the next open question to watch for?

Quarterly, you run a full loop. Pull signals (open rates, replies, purchases, unsubscribes), check each assumption in the persona against what actually happened, version the profile, and set new open questions.

The verbatim language rule matters here. When a reader uses specific words — in a reply, a DM, a comment — those go into the persona exactly as written. Not paraphrased. Their actual sentence. That language becomes the source for subject lines, offer copy, and positioning.

---

## Skill Structure for Developers

The skill follows the standard TABARC-Code progressive disclosure pattern:

| Level | File | When loaded |
|-------|------|-------------|
| Metadata | SKILL.md frontmatter | Always in context |
| Main instructions | SKILL.md body | When skill triggers |
| Persona question bank | `references/persona-framework.md` | When building a persona |
| Application protocols | `references/application-playbook.md` | When applying to a domain |
| Improvement protocol | `references/kaizen-loop.md` | When running a loop |

Claude reads only the reference files needed for the current task. The full question bank doesn't sit in context for a pricing decision; the full playbook doesn't load for a quick persona build.

---

## Compatibility

| Platform | Status |
|----------|--------|
| Claude.ai (web) | ✅ |
| Claude Desktop | ✅ |
| Claude Code | ✅ |
| Claude iOS / Android | ✅ |
| API (via system prompt) | ✅ (paste SKILL.md contents) |

---

## Related Skills

Other TABARC-Code skills that work well alongside this one:

- [`blog-writer`](../blog-writer) — apply your persona directly to post drafts
- [`web-seo-master`](../web-seo-master) — align SEO strategy with persona language
- [`forensic-style-auditor`](../forensic-style-auditor) — match your voice to what your audience expects

---

## Licence

MIT. Use it, fork it, adapt it. If you build something better, consider opening a PR.

---

## Author

Built by [TABARC-Code](https://github.com/TABARC-Code) for the TABARC-Gaming ecosystem — tabletop gaming content, community building, and newsletter strategy. I built this as a  quick and dirty audience test skill. It does work and o, but you are always better to use actual feedbak. 

Questions or issues: open a GitHub issue.
