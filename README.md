# AI Content Team: Starter Kit

A small team of three AI agents for [Claude Code](https://claude.com/claude-code) that turns
verified facts into a social-media hook and caption.

**Researcher** collects the facts (and never invents any) → **Copywriter** writes the hook
and caption in your brand voice → **QA reviewer** checks the draft against the facts before
you see it.

The kit includes a fictional example brand with offline facts, so you can run the whole
chain in a few minutes without writing anything first.

## What is in the box

```
CLAUDE.md                      instructions for the orchestrator (your main Claude Code session)
.claude/agents/                researcher, copywriter, qa-reviewer (all run on Sonnet)
.claude/skills/plain-voice/     plain everyday wording, short sentences, no hype
.claude/skills/hook-writer/    five hook candidates from facts, using six patterns
brand/voice.md                 your brand voice template (fill this in)
examples/facts.md              fictional sample facts, no web needed
examples/sample-output.md      what a finished run looks like
output/                        your results land here
```

## What is not in the box

This is one part of a working system, not the whole thing. It does not include design or
graphics, video, sound, scheduling or posting, automations, live status views,
approval gates and hooks, onboarding, or updates. It writes text drafts. You review and
post them yourself.

## Requirements

- Claude Code, tested with version 2.1.118. Use that version or newer (`claude --version`).
- Your own Claude subscription or API access. The kit does not include any.

## Setup in 3 steps

1. **Get the kit.** In a terminal:
   ```
   git clone https://github.com/SHOHREHDESIGN/ai-content-team-starter.git
   cd ai-content-team-starter
   ```
2. **Start Claude Code in that folder.** Run `claude` and accept the prompt to trust
   the folder. The three agents and two skills load automatically from `.claude/`.
3. **Run the team on the example.** Paste this into Claude Code:
   ```
   Run the content team on examples/facts.md. Topic: "Why a steady wake-up time beats a perfect bedtime". Platform: Instagram Reel.
   ```
   You get a hook, a caption, a fact map and a QA verdict, saved in `output/`. Compare it with
   `examples/sample-output.md`. The first run uses a neutral fallback tone and tells you so.

## Make it yours

1. Open `brand/voice.md`, fill in the sections, and change the first line to
   `STATUS: FILLED`. Until you do, the team writes in a neutral fallback tone and says so
   in every result.
2. Replace `examples/facts.md` with your own facts file (same format: one fact per line with
   an ID), or paste your facts into the chat.
3. Ask for the topic and platform you need.

If you do not give the team a source of facts, it asks you for one. It does not make facts up.

## How the chain behaves

- Workers run on Sonnet. Your main session only coordinates.
- If QA finds problems, the copywriter gets one correction round (two at most), then the
  team stops and shows you what is still open.
- Nothing is published or sent. Every result is a draft for you to read.
- Health, money and legal topics: the team describes what your sources say and does not
  promise results. You remain responsible for what you publish.

## Get the full system

This kit is three agents. Our full team has more than twenty: design, video, sound,
automation, scheduling and a quality gate, all trained on our own craft and run for you.

Want the full system, done for you? Send us a DM with the word FULL on Instagram:
[@shohreh.design](https://ig.me/m/shohreh.design).

## Support and issues

This kit is provided as is. There is no support and no guaranteed updates. GitHub Issues
are turned off.

## License

All rights reserved. You may use this kit for your own work. You may not resell it or
pass it on as a product. See [LICENSE](LICENSE).
