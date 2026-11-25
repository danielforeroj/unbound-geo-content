# geo-content

An agent skill that writes short-form content about AI search visibility from one report you paste. A video script, an Instagram carousel, a caption and an X thread, and it refuses to invent a number.

It is the skill Unbound GEO uses for every video on its own account. Every number in the output comes with the report line it came from. A number with no line gets deleted.

## A 20 second example

**You paste** a report (excerpt, fictional).

```
Engine ChatGPT. Date 2026-11-10. 5 questions, 10 runs each.
R3  Emergency dentist open Saturday. This clinic named in 0 of 10. Another clinic 9 of 10.
R8  This clinic 312 reviews, 4.9 stars.
R10 The other clinic's emergency page was cited in 7 of 10 answers.
R11 This clinic's Saturday hours appear only as an image in the footer.
```

**You ask** "60 second script about the biggest gap."

**You get** (excerpt).

```
SCENE 1 | 0 to 7 s | [serious]
SAY  This clinic has a 4.9 star rating. ChatGPT named it in 0 of 10 answers
     for a Saturday emergency dentist. Why?

SCENE 2 | 7 to 17 s | [serious]
SAY  Another clinic was named in 9 of 10. In 7 of those 10 answers, ChatGPT
     cited one page. A page called emergency dentist.

...

| Number    | Where   | Report line | Source text in report                 |
| 4.9       | Scene 1 | R8          | "312 reviews, 4.9 stars"              |
| 0 of 10   | Scene 1 | R3          | "This clinic named in 0 of 10"        |
| 7 of 10   | Scene 2 | R10         | "cited in 7 of 10 answers"            |
```

The full outputs are in [`examples/`](examples/).

## Install

### Claude Code

Copy the skill folder into your skills directory.

```bash
git clone https://github.com/danielforeroj/unbound-geo-content.git
mkdir -p ~/.claude/skills
cp -r unbound-geo-content/geo-content ~/.claude/skills/geo-content
```

On Windows PowerShell.

```powershell
git clone https://github.com/danielforeroj/unbound-geo-content.git
Copy-Item -Recurse unbound-geo-content\geo-content $HOME\.claude\skills\geo-content
```

Restart Claude Code. The skill loads when you ask for a script, reel, carousel, caption or thread about AI search.

### Claude.ai

1. Download `geo-content.zip` from [Releases](https://github.com/danielforeroj/unbound-geo-content/releases), or zip the `geo-content` folder yourself so the folder is the root of the zip.
2. Go to Settings, then Capabilities, then Skills.
3. Upload the zip and turn the skill on.

### ChatGPT and other assistants

Paste the contents of [`geo-content/SKILL.md`](geo-content/SKILL.md) as the project instructions (ChatGPT Projects, a custom GPT, or any system prompt). To keep the full behavior, also attach the six files in `geo-content/references/` as project files.

## How to use it

1. Run an AI visibility report on the business. No report yet? The free scan at [unboundgeo.com](https://unboundgeo.com) gives you one.
2. Paste the report into the conversation.
3. Ask for what you want.
   - "60 second script about the biggest gap in this report."
   - "Carousel from this report."
   - "Full package. Script, carousel, caption and X thread."
4. Read the number check table at the end. It lists every number and the report line behind it. Spot check two or three.
5. Post.

If you ask before pasting a report, the skill asks for the report and stops. That is the skill working.

## The rules, in short

1. No report, no writing.
2. Every number is in the report, in the same unit. "Named in N of M". A percentage only beside its count.
3. Every number carries the engine and the date in the caption.
4. No real business names in public copy.
5. Spoken lines have no colons. Short sentences. A question and an answer beat a statement.
6. The first sentence opens a curiosity gap and carries an emotion.
7. A number check table closes every deliverable. No line, no number.

House style on top of those.

- Value first, brand last. Problem and fix before any product name.
- Tactical advice with the literal how. What to write, where to submit, who to email, what to say.
- One idea per video. Breakdown in the video, detail in the resource.
- Counted on screen means shown in full.
- CTA with an outcome. "Comment WORD and we'll send you X, so you can Y."
- Never "share of voice". Never promise rankings.
- Carousels. Dark, one accent, a named framework, one idea per slide with a diagram, an example, a payoff, a closing slide with a series hook.
- US English. No em or en dashes.

## What is in the repo

```
geo-content/
  SKILL.md                  the skill (zip this folder)
  references/
    hooks.md                hook formula, 8 good, 4 bad
    video-script.md         scene structure, timing, tone tags
    carousel.md             slide grammar
    captions-and-x.md       caption and thread rules
    number-check.md         the table format, worked example
    cta.md                  outcome CTAs
examples/
  sample-report.md          a fictional report
  example-video-script.md
  example-carousel.md
  example-caption-and-thread.md
```

To build the zip for Claude.ai.

```bash
zip -r geo-content.zip geo-content
```

## Sibling skills

- [unbound-geo-audit](https://github.com/danielforeroj/unbound-geo-audit)
- [unbound-seo-geo](https://github.com/danielforeroj/unbound-seo-geo)

## License

MIT. See [LICENSE](LICENSE).

---

Built by Unbound GEO. unboundgeo.com. Get named. Then PROVE it.
