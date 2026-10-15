---
name: gtd-get-current
description: Run the second part of David Allen's Weekly Review with the person, get current, by gathering the garden's next actions, waiting items, dates, reviews due and projects with no next action, and presenting each for their decision. Use when they ask to get current or to check what is next, waiting or due, or as the second of the three parts of the weekly review; not for reviewing one project in depth, which the project-review skill does.
---

Bring the garden's lists up to date with the person, so that what they say is
true. Follow the authority boundary
in the garden's `AGENTS.md`.

Every decision is the person's and is made with them present. The skill gathers
and presents, and may suggest. It changes no item on its own judgment.

## Gather

Do this before they sit down, or as the sitting opens. It decides nothing.

1. Run `./bin/pos-view next waiting scheduled deadlines reviews
   reviews-to-schedule stuck` from the garden root.
   The waiting view lists items under each person they wait on. Its list
   "WAITING on no person" is one to fix: each item there waits on a thing,
   which its text should say, or on a person not yet linked, which
   `./bin/pos-person wait TARGET PERSON` links.
2. For each `NEXT` and `WAITING` item, read its body and find when it last
   changed: `git log -1 --format=%ad -- FILE` is a first measure.
3. The `stuck` view lists each project whose `STATUS` is `WIP` and none of
   whose files has a `NEXT` or `WAITING` item.
4. Read the repository a task names before saying what state it is in. A
   task can ask for something another repository already has.

## Present

Present by list, in this order, one item at a time. Give the scope, the
item, what bears on it, and a suggestion where there is one.

| List | The question for each item |
|------|----------------------------|
| `NEXT` | Is it done? Is it still the next action? |
| `WAITING` | Has it arrived? Is it time to ask again? Is it still wanted? When a thing has come, run `./bin/pos-person arrived TARGET` |
| Scheduled and deadlines, late or in the coming week | Do it, move the date, or drop it? |
| Reviews due | Review the project now, in its own sitting, or move the date? |
| `WIP` projects with no next action | What is its next action, or is it waiting, set aside or finished? |
| Projects, responsibilities or the root with no review scheduled | When is it reviewed? |

## Decide and record

Record each decision in the item's own file as they give it: the keyword, the
date, or a line under the item. A project review is the
`project-review` skill's work and may take a
sitting of its own; setting a project aside or closing it is
`project-handling`'s.

## Close

Say what changed in each list and what was left as it was. Commit only when
they ask.

## Learn from use

After each use, note in the handover which lists they worked through and which
they passed over, and where a suggestion was wrong. Refine this skill from
that.
