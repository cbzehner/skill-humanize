# Humanize Regression Scenarios

Use these as lightweight auto-research fixtures when changing `skills/humanize/SKILL.md` or its checklist. Run the baseline with the current skill, make one change, rerun the relevant scenarios, and keep the change only if it improves the result without losing meaning.

## Evaluation Loop

1. Pick one candidate change.
2. Run the relevant scenarios below.
3. Score each output against the pass criteria.
4. Keep the change only when it improves at least one scenario and does not regress another.
5. After four accepted changes in a row, argue for keeping the next questionable text before cutting it.

## Scenario 1: README Intro

Prompt: "Humanize this README intro."

Input:

```text
This repository packages one portable agent skill for comprehensive browser automation workflows. It enables agents to seamlessly inspect, test, and validate web pages across a wide range of scenarios. The canonical skill body lives in the skills directory and should be used whenever browser-based verification is required.
```

Pass criteria:

- No "This repository packages".
- No "comprehensive", "seamlessly", or "canonical skill body".
- Keeps the meaning: this is a browser automation skill for agent use.
- Output is suitable for a public README, not a chatty blog paragraph.

## Scenario 2: Technical Prose

Prompt: "Make this read like an engineer wrote it."

Input:

```text
Implementing efficient database indexing is a critical aspect of modern application development. Developers should consider several key strategies when designing their indexing approach. Additionally, leveraging explain plans can provide valuable insights into query performance and facilitate better optimization decisions.
```

Pass criteria:

- Removes "critical aspect", "key strategies", "Additionally", "leveraging", "valuable insights", and "facilitate".
- Uses concrete engineering terms such as `EXPLAIN`, index usage, hot queries, write cost, or table size.
- Keeps the tradeoff between read performance and write overhead.

## Scenario 3: Slack Register

Prompt: "Rewrite this as a real Slack update."

Input:

```text
hey team, quick update on the API migration. we've made significant progress and successfully migrated 75% of the user-facing routes. additionally, we implemented comprehensive testing to validate the new infrastructure. happy to discuss further in standup tomorrow.
```

Pass criteria:

- Allows fragments or compressed clauses.
- Uses approximate inline numbers such as `~75%`.
- Cuts "significant progress", "successfully", "additionally", "comprehensive testing", and "happy to discuss further".
- Does not turn into polished status-report prose.

## Scenario 4: Email Trim

Prompt: "Humanize this email."

Input:

```text
Hi Priya,

I hope this email finds you well. I wanted to reach out regarding the deployment checklist we discussed last week. I think it would be valuable to align on priorities and ensure we are on the same page before the release.

Would it be possible to schedule a 30-minute call this week? I am flexible with timing and happy to work around your schedule.

Looking forward to connecting soon.
```

Pass criteria:

- Removes the opener and templated closer.
- Puts the ask in the first two sentences.
- Cuts "reach out", "valuable", "align", "on the same page", and "happy to".
- Shortens the email by at least 30%.

## Scenario 5: Subtle Scaffolding

Prompt: "Humanize this without changing the point."

Input:

```text
The decision to add a release checklist was not really about process. It was about something deeper: the recognition that deploys had become a source of anxiety more than a normal engineering habit. What we built was not just a checklist. It was a commitment to safer releases. Clearer ownership. Faster rollback. Better reviews. That is the part that stuck.
```

Pass criteria:

- Removes "not really about X", "something deeper:", "more than", and "not just X".
- Breaks the four-beat parallel list or makes it plain.
- Removes the miniature aphorism closer.
- Keeps the concrete point: release checklist, anxiety, safer releases, ownership, rollback, reviews.

## Scenario 6: Attribution

Prompt: "Review this README for attribution and tone."

Input:

```text
This skill is inspired by Harshaneel's humanize repo and adapts its audit framing around burstiness, hedges, specificity, punctuation, and rhetorical scaffolding. It keeps a smaller workflow for everyday docs and public project writing.
```

Pass criteria:

- Keeps the credit.
- Does not imply endorsement, ownership, or wholesale copying.
- Keeps the tone plain and public-safe.

