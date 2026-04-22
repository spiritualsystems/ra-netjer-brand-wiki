# Wiki Log

Append-only record of edits to the public wiki. Each entry: one line. Never edit old entries.

---

## [2026-04-20] init | Public brand wiki scaffolded from the private Brand Wiki 2.0 | Created: CLAUDE.md, README.md, DEPLOY.md, wiki/index.md, wiki/log.md + initial article set across identity/, seekers/, teachings/, frameworks/, transmissions/, voice/, community/

## [2026-04-21] update | Large propagation pass from private wiki (grown from ~30 → 128 articles in the week since init) | Type: schema + propagate + sanitize

### Schema
- Updated `CLAUDE.md` with three standing directives from the source wiki (2026-04-21): (1) primary audience is AI-grounding / context; (2) name Sai Maa only when lineage context is essential — don't default to it; (3) retreat pricing logic is internal-only.

### Sanitize
- Audited 9 public articles for Sai Maa over-naming; pruned 11 of 18 mentions; kept 7 load-bearing lineage references.
- Updated `voice/voice-guide.md` "do not" list to codify the naming + pricing directives.

### Propagate — created
- **Teachings (22 new):** `how-deep-is-your-yes`, `dark-night-of-the-soul`, `beginners-mind`, `summa-iru-simply-be`, `trust-as-spiritual-foundation`, `breathe-notice-let-go`, `only-enlightenment-is-real`, `seven-myths-of-spiritual-awakening`, `redefine-i-am`, `sacred-silliness`, `self-sabotage-in-awakening`, `imperfection-as-key`, `ups-and-downs-liberating-truth`, `three-jewels-of-buddhism`, `find-your-inner-guru`, `the-clear-mirror`, `ten-thousand-dimensions`, `enlightenment-as-new-normal`, `you-begin-enlightened`, `bhakti`, `ascension-as-applied-enlightenment`, `martial-arts-as-spiritual-practice`.
- **Frameworks (3 new):** `aspect-work-inner-child`, `toroid-transmission-model`, `mantra-practice`.
- **Identity (2 new):** `sri-raghunath-guruji` (Ra's father and first teacher — Sai Datta Peetha, publicly recorded succession 2022-09); `youtube-channel` (public catalog of 188 videos).
- **Transmissions (1 new):** `member-led-teachings` (stub).

### Propagate — updated
- `identity/origin-story.md` — expanded with Good Shepherd Convent, actor/photographer phase, 6-month CS in 20 days, Dream Catcher Podcast reference, Mangalore kundalini origin.
- `identity/teacher-profile.md` — added brand tagline + mission phrasing + "Enlightened Transmission Teacher" title variant.
- `identity/mission-and-values.md` — added both mission formulations + audience-positioning reference.
- `transmissions/meditative-eating.md` — promoted stub → active with 2023-04-18 YouTube primary source.
- `transmissions/retreats.md` — added Hawaii Aug 14–23 2026 as publicly advertised; stripped pricing-mechanics paragraph per internal-only directive.
- `voice/voice-guide.md` — added permission / trust / BNL / keynote / new-normal / myth-busting / aspect-work / mantra registers; added naming + pricing "do not" entries.

### Deliberately skipped (and why)
- Individual seeker / mentee profiles (private by policy — public wiki keeps the generalized `seekers/who-ra-serves.md` only).
- Individual testimony articles from private Fathom calls (private). Public-consent testimonials (Michelle Davis, Heidi, Kathryn, Ching, Becky Morrison) deferred for a focused testimonies pass.
- `teachings/subconscious-release-without-story`, `jealousy-to-inspiration`, `anxiety-as-ego-self-love`, `embracing-aspects-into-the-light`, `transparentize-not-transcend`, `divine-masculine-integration`, `habit-chaining-zen-mornings` — single-source from private mentorship calls; not abstracted in this pass.
- `teachings/energy-balance-commitment`, `karma-yoga-as-apprenticeship`, `compassion-sales` — explicitly flagged internal-only in the source wiki.
- Team / operations / pricing tiers / revenue / internal-strategy material.
- `identity/life-story.md` — private-intimacy threshold; the public `origin-story.md` absorbs the public-safe subset.

### Index
- Regenerated `wiki/index.md` to reflect the new shape (6 identity / 1 seekers / 33 teachings / 5 frameworks / 9 transmissions / 1 voice / 1 community).

## [2026-04-21] llm-optimization | Make the public wiki more suitable as LLM context for content generation | Type: meta + navigation + voice-depth

### Created
- `wiki/START-HERE.md` — single-file brand-context brief (~3,600 words): identity, seekers, top ~20 teachings with verbatim quotes, frameworks, voice registers, offerings, do-not list, worked example, pointers. Designed as the canonical LLM-grounding entry point; readable in ~15 min.

### Updated
- `README.md` — rewrote around a one-paragraph brand summary, an explicit *"If you are an LLM drafting content — read in this order"* section, and a task-oriented category table.
- `wiki/index.md` — added a brand snapshot + **task-oriented routing table** at the top (*"if drafting X, open Y"* mapping 12 draft types to the articles to open). Existing catalog retained below.
- `wiki/voice/voice-guide.md` — added 5 worked examples across registers (social caption, satsang invitation, consultation reply, daily-practice micro-teaching, keynote reconciliation) and 5 micro-templates (satsang opening, teaching-forward post, consultation reply, retreat invitation, bio blurb). Each worked example labeled with register + length + notes.
- `CLAUDE.md` — updated the "Draft content using the wiki" workflow to point at `START-HERE.md` first and `index.md`'s routing table second.

### Rationale
Primary audience per standing directive is AI-grounding. A dense single-file brief + task routing makes that materially faster for an LLM to use. The worked examples translate "voice" from abstract register labels into concrete outputs the LLM can pattern-match against. No new teachings or offerings were added — this pass is purely LLM-usability and navigation.
