# Ra Netjer — Public Brand Wiki (Schema & Operating Guide)

This repository is the **public brand wiki** for the Ra Netjer mentorship and spiritual teachings practice. It is a derivative of a larger private brand wiki and is maintained specifically as a shareable, up-to-date reference for:

- **Content volunteers and contributors** drafting posts, captions, and other content
- **Virtual assistants** handling inquiries, scheduling, and audience communication
- **LLMs** that need live brand context to draft on-brand material

**Access pattern:** the repo is *public* on GitHub, but discoverable only through a long, obscure URL. It is intentionally unindexed and unpromoted — a "secret garden" that anyone with the link can read, but which is not advertised.

## What this wiki is — and is not

### It IS
- A current snapshot of Ra Netjer, his brand, his teachings, his public offerings, and his voice.
- Source content for public-facing work: posts, captions, emails, talks, show notes.
- A grounding document for LLMs so that anything they draft "sounds like Ra."

### It is NOT
- The full private brand wiki. Private material (individual mentee information, internal business data, team personnel details, private biographical detail, internal strategy) is kept in a separate private repository and does not belong here.
- A marketing funnel. The voice is reflective and grounded, never promotional.
- A public record of every teaching. Only material Ra shares publicly — in satsangs, on the website, in published work — belongs here.

## Ownership model

- **This wiki is LLM-maintained** under supervision. A contributor asks for a change; the LLM updates the relevant article and the index in the same pass.
- **Contributors do not hand-edit articles** unless they are certain about the material and the voice. The default move is: ask, don't write.
- **Schema changes** (this file) co-evolve with the maintainer; flag any proposed schema change explicitly.

## Directory structure

```
wiki/
  identity/       — who Ra is, origin, lineage, mission
  seekers/        — who Ra serves (generalized — no individual profiles)
  teachings/      — the WHAT: concepts, distinctions, signature teachings
  frameworks/     — the HOW: structured methodologies
  transmissions/  — the public-facing offerings
  voice/          — how Ra speaks, signature phrases, tone
  community/      — the I AM Community's public culture

wiki/index.md     — catalog of every article
wiki/log.md       — append-only log of edits
```

## Article conventions

Every article is a markdown file with this frontmatter:

```markdown
---
title: <human-readable title>
category: <identity | seekers | teachings | frameworks | transmissions | voice | community>
status: <active | draft>
last_updated: <YYYY-MM-DD>
---
```

After frontmatter, use H2 / H3 headings. Keep articles focused — one concept per file. Cross-reference other articles with relative markdown links: `[voice guide](../voice/voice-guide.md)`.

**Voice of the wiki itself:** reflective, grounded, precise. No marketing hype. No "unlock," "transform your life," "proven system." Let Ra's own voice emerge through quoted material in the voice/ articles.

## What goes in — and what stays out

### Include

- Material Ra shares publicly (satsangs, website, podcast appearances, published writing)
- The names of teachers Ra publicly acknowledges (Sai Maa, Ahjan at a high level, lineage teachers like Ramana Maharshi, Mahavatar Babaji)
- Public offerings and how to participate
- Signature teachings Ra teaches openly
- Signature phrases from public settings

### Exclude

- Individual mentee names, stories, or arcs (these belong to private containers)
- Internal business data: specific pricing tiers, revenue, team compensation, org charts, LLC / tax structure
- Team personnel details beyond what's publicly known
- Private biographical detail Ra has not chosen to make public (specific family information, specific health / crisis episodes, private correction events from his own teachers, etc.)
- Strategy / positioning intended for internal consumption
- Anything sourced from private mentorship calls, private operational meetings, or closed-door conversations

**When in doubt, leave it out.** This wiki is readable by anyone with the URL — treat it that way.

## Workflows

### Update

When a contributor asks for a wiki update (e.g. "Ra mentioned a new teaching on Sunday's public satsang — please add it"):

1. Confirm the material is from a public setting.
2. Route to the right article (or create a new one).
3. Update `wiki/index.md` in the same pass.
4. Append a one-line entry to `wiki/log.md`.

### Draft content using the wiki

When drafting a post, caption, email, or other content:

1. Read `wiki/index.md` to find relevant articles.
2. Read those articles in full.
3. Quote Ra directly where precision matters; paraphrase in the same register elsewhere.
4. Never invent quotes. If a phrase doesn't appear in a sourced article, don't put it in Ra's mouth.
5. Run the draft past the voice guide's "do not" list before finalizing.

### Remove

If material in the wiki turns out to be inappropriate for public access (contains private detail, misattributes a quote, etc.), remove it and log the removal. Err toward removal.

## Guardrails

- **Never invent quotes.** Attribution requires a sourced public appearance.
- **Never add private detail.** If you're unsure whether something is public, treat it as private and omit.
- **Never use marketing hype.** The voice is grounded, not promotional.
- **Never publicly name individual mentees.** Use generalized language: "a mentee," "a student," "someone Ra works with."
- **Default to Ra's own words** wherever possible. The voice guide articles are primary sources — use them.
