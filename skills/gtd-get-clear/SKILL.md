---
name: gtd-get-clear
description: Run the first part of David Allen's Weekly Review with the person, get clear, by gathering every item in the garden's intrays and presenting each one for their decision on what it is and where it goes. Use when they ask to get clear, to clarify or empty an intray, or as the first of the three parts of the weekly review; not for capturing a new item, which the capture skill does.
---

Empty the intrays with the person. An intray holds only what is not yet
clarified; this skill is how an item leaves it. Follow the authority boundary
in the garden's `AGENTS.md`.

Every decision is the person's and is made with them present. The skill gathers
and presents, and may suggest. It moves nothing on its own judgment.

## Gather

Do this before they sit down, or as the sitting opens. It decides nothing.

1. Run `./bin/pos-view intray` from the garden root. It lists every open item
   under "Unsorted" in each scope's `intray.org`.
2. Read each item's body in its file, and what it links to when the title
   alone does not say what it is.
3. List the finished items still in each intray, `DONE` and `CANCELLED`.
4. Run `./bin/pos-view scheduled` and note the trackers' sweep items that are
   due: an issue tracker is another intray.

## Present

Take the items one at a time, the oldest first. Put nothing back unclarified.
For each, show them:

- the item, in the words it was captured in, and the scope it is in;
- what it is, in one line, if the title does not say;
- a suggestion: one of the dispositions below, and the home.

Ask Allen's questions in order: what is it; is it actionable; if so, what is
the next action.

## Decide and record

The person chooses one disposition. Record it at once, then present the next.

| Disposition | What is written |
|-------------|-----------------|
| Do it now | Only if they say so. Allen's rule is two minutes; do it, then mark it `DONE` |
| A next action | Move the item to its project's file, or to the "Tasks" of its responsibility or of the root, as `NEXT` |
| A later action | The same move, as `TODO` |
| Waiting on someone or something | The same move. For a person, then run `./bin/pos-person wait TARGET PERSON [NOTE]`, which sets `WAITING`, links the person and records the date; do not write the property by hand. For a thing, move it as `WAITING` and say what in the item |
| Not committed to | The same move, as `SOMEDAY` |
| A project | It needs more than one action: use `project-handling` |
| Reference | Its content goes where the understanding is kept; the item is marked `DONE` |
| Trash | Mark it `CANCELLED` with one line saying why |

Move an item with `./bin/pos-place TARGET FILE UNDER STATE` from the garden
root: it moves the heading, its properties, its body and its children,
sets the state and records where the item came from. `TARGET` is the item's
ID or `FILE:LINE`; `--help` has the rest. To mark an item `DONE` or
`CANCELLED` where it is, run `./bin/pos-state TARGET STATE 'NOTE'`. Each
move shifts the lines below it in the intray, so read the item's line again
before the next move, or name items by ID. `pos-place` prints each link that
names the item's old place; repair those. After the sitting, run
`./bin/doctrine-audit links .`.

## Close

Say how many items were clarified and how many are left. An intray need not
be emptied in one sitting; say so plainly if it was not. Commit only when they
ask.

## Learn from use

After each use, note in the handover which suggestions they took, which they
changed, and where the presentation wasted their time. Refine this skill from
that.
