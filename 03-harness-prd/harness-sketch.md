# Harness Sketch

Describe Juno's role and task: You are a front-end prototyper building a rough, low-fidelity prototype of "Juno PM," an AI Associate PM embedded in Slack and ProductBoard. It turns one internal signal into a problem or job-to-be-done card, assigns a strategic priority tier, weights it, categorizes it, and stores it.

_Rough first pass, Module 3 Lab 1. Not the AI PRD._

## 01 · Context
One signal at a time: the text, plus its source (Slack channel/thread or ProductBoard item), author, and date.
Today’s date, used only for the recency score.
The RocketShip Strategy One-Pager, specifically the P0 to P3 definitions with their includes and excludes.
The existing category labels already stored, so it can reuse before creating.
The skill file (role, task, constraints, card format).

## 02 · Tools
Read a signal from Slack or ProductBoard
Frame a problem or JTBD	
Assign a tier and 0 to 4 input scores	
Propose a category label (new or existing)
Write one card to storage
Show a “Route to PM / DRI” label

## 03 · Loop
One pass per signal, plus one self-check retry. Frame, tier, score, label, then run the verification checks (section 6). If a check fails, it gets one revision. If it still fails, the card goes to NEEDS CLARIFICATION with the failure reason. It never loops until it passes.
No chaining. It doesn’t pull in more signals to “firm up” a weak one. Missing information goes in Unknowns.
Batch runs (multiple signals) process each signal independently. A failure on one doesn’t stop the others.

## 04 · Memory
The stored card: all seven fields plus the tier and its supporting phrase.
The category label list (labels the PM has approved, plus provisional ones tagged “new”).
Cards in NEEDS CLARIFICATION, with the reason, so they can be re-run once clarified.

## 05 · Permissions
Read the signals it’s pointed at.
Create a card, including cards routed to NEEDS CLARIFICATION.
Reuse an existing category label.
Create a new provisional label, flagged “new” for the PM to see.

## 06 · Verification
Self-checks before storing (automatic)
Every claim is quoted. Each scored input and the tier have a verbatim supporting phrase from the signal. No quote, no score.
Nothing invented. Every field not stated appears in Unknowns as “not stated.”
Tier rules applied in order. P0 checked first, exclusions honored, P3 not assigned if the signal touches correctness, security, compliance, or onboarding.
Scope gate. Anything not “Internal (stated)” skipped framing, tier, and weight.
Format. All fields present, in order, under one page.
No drafted messages appear anywhere in the card.
