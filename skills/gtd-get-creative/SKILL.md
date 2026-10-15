---
name: gtd-get-creative
description: Run the third part of David Allen's Weekly Review with the person, get creative, by gathering the garden's SOMEDAY items and presenting each for their decision to take it up, keep it or cancel it, then asking what is new. Use when they ask to get creative or to look over what is set aside, or as the last of the three parts of the weekly review.
---

Read with the person what the garden keeps and is not committed to, and make
room for what is new. Follow the authority boundary
in the garden's `AGENTS.md`.

Every decision is the person's and is made with them present. The skill gathers
and presents, and may suggest. It takes up nothing and cancels nothing on its
own judgment.

## Gather

Do this before they sit down, or as the sitting opens. It decides nothing.

1. Run `./bin/pos-view someday` from the garden root.
2. Read each item's body and what it links to.
3. For each, look for what has changed since it was set aside: a project
   that now does it, a ruling that replaced it, or work that makes it
   timely.

## Present

One item at a time. Give the scope, the item, when and why it was set aside
if the item says, what has changed since, and a suggestion.

## Decide and record

| Decision | What is written |
|----------|-----------------|
| Take it up | It becomes `TODO` or `NEXT` where it lies or in its home. If it needs more than one action it is a project: use `project-handling` |
| Keep it | Nothing changes |
| Cancel it | Mark it `CANCELLED` with one line saying why |

Then ask them what is new: what they have thought of, want, or have noticed
since the last review. Capture each with the
`capture` skill. It goes to the intray, for the next
get clear.

## Close

Say what was taken up, kept and cancelled, and what was captured. Commit
only when they ask. When this is the last part of a weekly review,
[gtd-weekly-review](../gtd-weekly-review/SKILL.md) closes the review.

## Learn from use

After each use, note in the handover what they took up, what the question
"what is new" produced, and whether the reading was worth their time. Refine
this skill from that.
