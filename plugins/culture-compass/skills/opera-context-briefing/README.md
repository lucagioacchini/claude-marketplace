# Opera Context Briefing
 
Part of the **Culture Compass** plugin.
 
## What it does
 
Generates a spoiler-free "pre-experience briefing" for a film, book, or series — before the user watches or reads it. The briefing covers the real-world story behind the work (why and how it was made) rather than the story told within it, so the user can go in with useful context instead of a synopsis or someone else's interpretation.
 
Concretely, it covers:
 
- The author's/director's personal and professional situation at the time of creation
- How the project came to be (genesis of the idea, related or abandoned earlier projects)
- The creative process (drafting/shooting timeline, working titles, stated influences)
- Production or publishing circumstances (cast and crew, or publisher/editor, locations, scale/budget)
- The historical and social context of the period it came out in (contemporary events, cultural climate — kept separate from any claim about what the work "means")
- How it was received and positioned critically at the time (awards, career context)
- Practical tips on how to approach the experience (pacing, attention, mindset)
It closes with sources only if the user explicitly asks for them.
 
## What it deliberately leaves out
 
This is the core guarantee of the skill: **no plot beyond the bare, already-public premise, and no interpretive or thematic reading** — no symbolism, no "what it's really about," no hints at the ending or emotional arc. Historical context is reported as external fact, never used to imply what the work itself means. If the user later asks to discuss the work after having seen/read it, that restriction lifts only for that follow-up request.
 
## When it triggers
 
Use this skill whenever the user:
- asks for context, background, or "how it was made" about a film, book, or series they're about to watch or read
- explicitly asks to avoid spoilers or interpretive framing before experiencing something
- says things like "tell me about this before I watch/read it, but don't spoil anything"
It's designed to work across languages — it responds in whichever language the user writes in.
 
## Inputs
 
| Parameter | Description | Required? |
|---|---|---|
| `media` | Type of work — film, book, series (or adaptable: play, comic, etc.) | Yes, but can be inferred from title if omitted |
| `titolo` / `title` | Title of the work | Yes |
| `autore` / `author` | Director, writer, or showrunner | Can be looked up automatically if omitted and the title is unambiguous |
 
If the title itself is ambiguous (e.g. a remake or a very common title), the skill asks one clarifying question before proceeding — otherwise it proceeds directly with a stated assumption.
 
## Design principles
 
- **Complete on the first pass.** The skill is written to front-load research and deliver a fully detailed briefing immediately, rather than a shallow first answer that waits for the user to ask for "more depth." Later requests to expand only add to what was already given — nothing already delivered gets cut.
- **Facts vs. criticism, clearly separated.** Any critical judgment quoted (an award, a historian's line) is attributed to its source and never adopted as the skill's own interpretive claim.
- **Sources on demand only.** Citations/links are surfaced only if the user explicitly asks where the information came from, via a link preview card — never inline in the main briefing.
## Example prompts
 
- "Sto per guardare Persona di Bergman, dammi il contesto ma niente spoiler"
- "Devo leggere Cent'anni di solitudine, spiegami come è nato prima che inizi"
- "Voglio guardare questa serie stasera, dammi solo il contesto storico e produttivo"
## Related
 
This skill is one of several planned for the Culture Compass plugin, alongside skills for in-depth analysis (albums, novels, art) and cultural discovery (exhibitions, events, concerts).