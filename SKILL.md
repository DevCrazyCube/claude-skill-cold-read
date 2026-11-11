---
name: cold-read
description: Test something you wrote on a fresh agent that has seen none of your context, before a person sees it. Two forms - a surprise read (does the reader guess the punchline, twist or reveal before it comes) and a comprehension read (can a stranger do the task from this README, prompt, brief or instruction alone). Use before sending a pitch, joke, hook, headline, README, prompt for another agent, onboarding page or hand-off note to its real audience, and whenever you catch yourself thinking "this is clear" about your own text.
---

# Cold read

You wrote it, so you cannot read it for the first time. You know what the turn is, so it cannot surprise you. You
know what the missing step is, so you do not see that it is missing. A fresh agent has neither problem.

A cold read is cheap and narrow. It catches two things: **the predictable** (the reader saw it coming) and **the
unexplainable** (the reader cannot say why it happened, or cannot do the task). It does not tell you whether
something is good.

## The rules that make it a cold read

1. **A reader that has seen nothing.** Start a new agent. Never fork yourself, never continue an agent that has
   read an earlier version, never paste your reasoning "for context".
2. **Give it only what the audience gets.** The text on screen, the page, the prompt. Not the file name that gives
   it away, not your notes, not the goal you were aiming for.
3. **Ask for what it understood, never for an opinion.** "What happens next?" and "What would you type?" give
   evidence. "Is this clear?" and "Is this funny?" give politeness.
4. **Do not lead.** No "note that", no hint about what a good answer looks like, no second try with a nudge.
5. **A reader is used once.** After a rewrite, use a new one. The old one knows the answer.
6. **Write the pass criteria before you read the answers.** Otherwise every answer looks like a pass.
7. **Keep the answers.** Paste them, unedited, under the thing they are about, so the person who decides sees them.

## Surprise read (a turn, twist, punchline, reveal, hook)

Two messages, so the reader cannot see the turn early. Use an agent you can send a second message to.

**Message 1: only the setup.** Everything the audience has before the turn, and:

> What is the situation, in one sentence?
> What happens next? Give your three most likely guesses.

**Message 2: the turn.** And:

> Why did that happen, in one sentence?
> Would someone in the audience pass this on, and to whom?

It passes when all four hold:

| Check | Pass | What a fail means |
|---|---|---|
| The situation | It names the situation you meant | The setup is unclear; fix that first, the rest of the read is void |
| The three guesses | None of them is your turn | Predictable: the ending only illustrates the setup |
| The reason | It gives your reason, unprompted | Random: the turn does not follow from anything shown |
| Passing it on | Yes, and to a kind of person ("a flatmate who does this") | "Maybe", "a like, not a share" or "a friend" is a no |

**When a guess was your turn: keep the setup, drop the turn.** The three guesses are now your list of what
everyone expects. Write a turn that comes after them, and read it cold again with a new reader. Do not loosen the
rule to save a turn you like.

Read the guesses for more than pass or fail. A reader sometimes guesses a better turn than the one you wrote.

## Comprehension read (a README, prompt, brief, instruction, hand-off)

One message. Give the reader the page and a task a real reader would have, and:

> 1. In one sentence, what is this for?
> 2. The exact steps you would take, in order. Where the page does not tell you something, do not guess
>    silently: write "NOT STATED:" and what is missing.
> 3. Every place you hesitated, re-read, or had to assume something.
> 4. One thing you expected to find and did not.

Let it read only the page. If it may open the code, it will fill the gaps from there, and your reader will not.

It passes when:

- its one sentence is what you would have said;
- its steps would work, and you can check that by running them yourself;
- every "NOT STATED" is something you chose to leave out, not something you forgot.

Every hesitation is a fix, even when the reader got it right in the end. A person hesitates in the same place and
has less patience.

For a prompt you wrote for another agent, the task is the prompt's own task, and the question is: "Before you
start: what do you think is being asked, what would you do first, and what would you have to guess?"

## Reporting

Use `templates/surprise-read.md` or `templates/comprehension-read.md`. State the criteria, paste the answers,
give the verdict per criterion, and say what you changed. When a read fails, say so plainly: a stopped pitch with
its three guesses is a more useful thing to hand over than a pitch that was let through.

## Limits

- An agent is a weak stand-in for the audience. It has read more jokes, more READMEs and more twists than any
  person, so it guesses turns a person would not, and it understands pages a person would not. A pass is not a
  promise.
- It measures prediction and comprehension. It does not measure taste, timing, delivery or whether a picture
  works. Something can pass and be dull.
- One reader is one sample. For something that matters, use three readers and look at what they agree on.
- A reader finds where the page fails, not where the thing it describes fails. After a comprehension read, run the
  steps yourself: in the example here, that run found a bug in the tool that no reader of the page could see.
- The first trial of the surprise read stopped four of four pitches, each because the turn was among the guesses,
  and every reader named the situation correctly. Whether that predicts what makes a person laugh is not known.
