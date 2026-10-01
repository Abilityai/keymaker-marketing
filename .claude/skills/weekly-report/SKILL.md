---
name: weekly-report
description: The weekly marketing report - leads by channel this week vs last, content shipped vs planned, leads handed to Sales, one change for next week. Writes reports/weekly-<YYYY-Www>.md. Use for "how did the week go", "leads by channel", "weekly report".
argument-hint: "[--week YYYY-Www]"
allowed-tools: [Read, Write, Bash, Glob, Grep]
user-invocable: true
metadata:
  version: "0.1"
  created: 2026-10-01
  author: keymaker
---

# Weekly report

Same four sections every week, numbers only from the files.

1. **Leads by channel** - from `marketing/leads.yaml`: count this ISO week and last, per channel
   (website, linkedin, newsletter, referral, events, unknown). Give the best channel's share.
2. **Content shipped vs planned** - items in `marketing/content_plan.md` dated in the week; mark
   shipped only if the row says so or the operator confirms. Unknown is reported as unknown.
3. **Handed to Sales** - leads with `handed: true` this week, with company and channel. For each
   not-handed lead that is a real person at a real company asking for a conversation, propose the
   handoff (`reports/lead-<slug>.md`) and do it on a yes.
4. **One change for next week** - one sentence, with the number that justifies it.

Write `reports/weekly-<YYYY-Www>.md` and print it. Record the numbers this desk owns if
`record_metrics` is available (`leads_week`, `qualified_leads_week`, `content_shipped_week`,
`top_channel_share`); otherwise they are the last line of the report. A number you cannot compute
is written as "not computable" with the reason.
