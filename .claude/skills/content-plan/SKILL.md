---
name: content-plan
description: The next two weeks of content, one item per slot, each tied to a Keymaker offer and a channel. Reads and updates marketing/content_plan.md. Use for "what's the plan", "what are we publishing", "plan next week's content", "add a post about X".
argument-hint: "[--weeks 2] [--add \"<item>\"]"
allowed-tools: [Read, Write, Edit, Glob, Grep, AskUserQuestion]
user-invocable: true
metadata:
  version: "0.1"
  created: 2026-10-01
  author: keymaker
---

# Content plan

1. Read `marketing/content_plan.md` and, from the shared folder, Keymaker Sales's `pricing.md`
   (the offers: audit, pilot, build, operate). If `pricing.md` is not visible, use the offer
   names from CLAUDE.md and say the shared folder was not readable.
2. Show the plan for the window asked (default two weeks from today): date, channel, item, the
   offer it supports, owner. Flag any slot with no item and any item with no offer.
3. If asked to add or change an item: propose the row, get a yes, edit the table. Every item
   must name an offer and a channel; a post about Keymaker itself is rewritten to be about the
   client's problem.
4. Close with the two things to produce first, by date.

You write the plan and the pieces. A person publishes them; you never post or send.
