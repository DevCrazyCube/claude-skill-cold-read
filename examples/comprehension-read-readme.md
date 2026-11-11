# Comprehension read: the README of a small command-line tool

The page read: the README of [`agent-progress-log`](https://github.com/DevCrazyCube/claude-skill-agent-progress-log),
before the fixes below.

**Reader:** a fresh agent, used once, allowed to read only that page · **Run:** 1 · Its answer is unedited.

## The task given

> Set this up in a new project of mine that has two milestones and one check called `tests`, then record my first
> work session, then make sure the generated page is up to date in CI.

## Pass criteria (written before the read)

- Its one sentence says: one small file per work session, and a generated progress page.
- Its steps work when I run them.
- Nothing I forgot shows up as "NOT STATED".

## Answer

> **1. What it is for.** A Claude skill plus one Node script: each work session writes its own small file in
> `progress/`, and `PROGRESS.md` (now / milestones / log) is generated from those files, so parallel agents never
> conflict.
>
> **2. What I would type, in order.** Clone the skill, `mkdir -p scripts`, copy `progress.mjs` in.
> `progress.config.json` — NOT STATED: where it lives (I assume the project root). Then
> `node scripts/progress.mjs new --agent claude --milestone M0 --tests green`, edit the printed file, and
> `node scripts/progress.mjs`. NOT STATED: that `progress/`, `PROGRESS.md` and the config must be committed (I
> assume yes). CI step: `node scripts/progress.mjs --check`. NOT STATED: a workflow file, the Node setup step, or
> that it exits non-zero.
>
> **3. Where I hesitated.**
> - "Every key is optional" — the config's location is never given.
> - "left out means not run" versus "a check that is not stated" — does omitting `--tests` fail `--check`?
> - "fill in Did / Next / Blockers" — I never see the template; what goes in Blockers when there are none?
> - "PROGRESS.md ← 3 fragment(s)" — took a re-read to see this is output, not syntax.
> - "`--done`" — if I forget it, may I add `done: true` by hand, given "an earlier fragment is never edited"?
> - "as a Claude Code skill (personal)" — unclear whether the script works without installing the skill, and
>   whether `progress/` is created for me.
> - "fail when PROGRESS.md is stale" — is the generated page deterministic (no generation timestamp)?
>
> **4. Expected but missing.** A copy-paste CI snippet with the exit-code behaviour of `--check`.

(The reader's code blocks in part 2 are folded into a sentence here to keep the page short; nothing else is changed.)

## What it showed

| Place | What the reader did | Fix made on the page |
|---|---|---|
| Where the config lives | NOT STATED, assumed the root | Said: in the folder you run the script from, normally the project root |
| What to commit | NOT STATED, assumed yes | Said: commit the config, `progress/` and `PROGRESS.md` |
| CI | NOT STATED | Added a workflow snippet and the exit codes (0, 1, 2) |
| A check left out of `new` | Could not tell if `--check` then fails | Said: it is written as `not-applicable`, which `--check` accepts |
| The fragment's template | Never saw it | Showed the file `new` writes, with `**Blockers:** nothing` |
| The output line | Read it as syntax | Moved the output out of the command line |
| Forgetting `--done` | Rule looked contradictory | Said: this session's fragment is yours to edit until you commit it |
| Skill or script | Unsure the script works alone | Said: the script is all a project needs; the skill is for Claude |
| Is the page deterministic | Unsure | Said: no timestamp of its own, same fragments give the same bytes |

## Verdict

**Failed** on the third criterion: three things were forgotten, not left out. Its one sentence was right and its
steps work (run by hand afterwards: the page generates and `--check` exits 0).

Nine fixes from one read. The author had re-read the page before the read and found none of them.

## What the read could not find

Running the reader's steps by hand found a tenth thing, in the tool and not on the page: `--check` accepted a
fragment whose `Did` and `Next` were still empty. A reader tells you where the page fails. Only a run tells you
where the thing it describes fails. Do both.
