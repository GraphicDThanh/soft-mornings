# writing-training-reports

Claude Code plugin with one skill that writes daily or weekly training report emails (subject `[team][training] YYYYMMDD` plus hashtags) from your notes and saves them as a Gmail draft.

Interactive guide (setup, example report, commands): [Training Report Guide](https://claude.ai/artifact/Ls7AqENKvcMyG9nfERHWqU)

## Requirements

- Gmail connector (to create drafts)

## Install

```
/plugin marketplace add GraphicDThanh/soft-mornings
/plugin install writing-training-reports@soft-mornings-kit
```

## First run

The first run asks for a profile (team prefix, recipients, and so on) and offers to save it to memory. Say "update my profile" to change it later.

## Configure

The first run asks for your profile: name, team prefix, supporters, CC addresses, course, default hashtags and repo.
