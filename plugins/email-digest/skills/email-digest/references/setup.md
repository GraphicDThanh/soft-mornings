# Email digest — setup and scheduling

## Setup (chat only, never in a scheduled run)

All checks are read-only. Never create labels or filters.

1. Run `list_labels` and ask for every optional setting from SKILL.md Config in ONE message,
   with examples: approval subject words (`leave, wfh, approval`), bracket-only words, company-wide
   group (`all@example.com`), training group (`training@example.com`), mentee subject
   prefixes (`intern, training`), report subject prefix (`[team][training]`), project labels
   (`Projects/Smoliv`). Leave empty to skip. Also ask if any default should change (most users
   keep them) and the timezone if unsure. Example preset: [example-config.md](example-config.md).
2. Verify each set value (words, groups, prefixes, labels) with a search over the last 14 days
   and show the count, e.g. "`label:"<label>"` → 28 threads, correct?". 0 results → say so and
   ask again.
3. A section whose settings are empty stays hidden (rules in SKILL.md Step 2).
4. Show the scheduled task prompt to paste (below), with every set value.

## Scheduling

A scheduled run can't ask, and each run is a fresh session, so the prompt must carry every set
value and any changed default:

```
Run the email-digest skill.
Approval subject words: <word>, ...                (each line optional, only if set)
Bracket-only words: <word>, ...
Company-wide group: <address>
Training group: <address>
Mentee subject prefixes: <prefix>, ...
Report subject prefix: <[prefix][training]>
Project labels: "<Parent/Child>", "<Parent/Child>"
Timezone: <IANA name>
```

Schedule: weekdays 08:00 in the user's timezone unless changed. Never create the task without
asking.
