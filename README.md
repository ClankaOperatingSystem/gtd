# gtd

David Allen's Weekly Review as four skills: one for each of its three
parts, get clear, get current and get creative, and one that runs the
three in order.

| Skill | What it does |
|-------|--------------|
| `gtd-get-clear` | Empties the intrays, one item and one decision at a time |
| `gtd-get-current` | Brings the next, waiting, dated and review lists up to date |
| `gtd-get-creative` | Reads the items set aside, and captures what is new |
| `gtd-weekly-review` | Runs the three parts in order and marks the weekly review done |

A garden declares this methodology in its configuration, at a tag:

    methodologies:
      - source: git@github.com:ClankaOperatingSystem/gtd.git
        ref: TAG

`clankos-run install` copies each folder under `skills/` into the
garden's `.agents/skills/`.

The skills run the garden's `bin/startup-prompt`, `bin/pos-place`,
`bin/pos-state`, `bin/pos-person` and `bin/pos-lint`, and name its
`capture` and `project-handling` skills and ClankOS's `clankos-review`.
