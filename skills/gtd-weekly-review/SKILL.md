---
name: gtd-weekly-review
description: Conduct David Allen's Weekly Review of the garden with the person, by running its three parts in order, get clear, get current and get creative, and marking the root's weekly review item done. Use when the root's weekly review item falls due, or when they ask for the weekly review; for one part alone, use that part's own skill.
---

Run the Weekly Review as one sitting, or as much of it as the person has time
for. Follow the authority boundary
in the garden's `AGENTS.md`.

The review is three skills, used in this order. This skill adds nothing to
what they say; it orders them and closes the review.

1. [gtd-get-clear](../gtd-get-clear/SKILL.md): empty the intrays.
2. [gtd-get-current](../gtd-get-current/SKILL.md): bring the lists up to
   date.
3. [gtd-get-creative](../gtd-get-creative/SKILL.md): read what is set aside,
   and ask what is new.

Every decision in all three is the person's and is made with them present. Each
part gathers and presents, and may suggest.

## Open

Run `./bin/startup-prompt --view reviews` from the garden root. Find the
root's "Weekly review" item under "Root reviews" and tell them whether it is due today, late
and by how many days, or not yet due. Ask how much time they have.

Do the gathering of all three parts before they begin, where the session
allows it, so that their time goes to deciding.

## Run the three parts

Use each part's skill, to its own close. Between parts, say in one line that
the part is closed and name the next before starting it.

They may stop after any part. Stopping is not a failure of the review: say
which parts were done and which were not.

## Close

When the third part is closed, mark the root's "Weekly review" item done for
this week: run `./bin/pos-state index.org:LINE DONE 'NOTE'` from the garden
root, with the line of the item's heading and one line saying which parts
were run. Org moves its `SCHEDULED` date on by the item's own repeater and
records the change in the item's `LOGBOOK`. The weekday and the interval are
the item's, and the person sets them by editing it; assume neither. If they stopped earlier,
leave the date as it is, so that the item stays due.

Say what the review changed: how many items left the intrays, what changed
in the lists, what was taken up or cancelled, and what was captured. Commit
only when they ask.

## Learn from use

Note in the handover how long the review took, which parts they did, and what
they passed over. Each part's skill keeps its own note. Refine this skill and
the three from that.
