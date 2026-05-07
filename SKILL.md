---
name: compcat
description: Use when the user invokes /compcat — almost certainly a typo of /compact. Outputs an ASCII COMPuter CAT (cat sitting at a terminal) with a fresh silly quip each time, then nudges the user to type /compact for real. Levity for the typo, with the actual answer spelled out.
---

# Compcat

## Overview

`/compcat` is what happens when someone fat-fingers `/compact`. Catch the typo with grace: an ASCII **COMP**uter **CAT** — a cat sitting next to a little terminal — that gently points them at the real command. The visual makes the pun land.

## When to Use

- User invokes `/compcat`
- User clearly mistyped `/compact` as something cat-adjacent
- User explicitly asks for the compcat

## When NOT to Use

- User actually typed `/compact` correctly — don't intercept real compactions
- Middle of focused work where a cat would derail without being asked for

## What to Output

Output the block below, with no preamble and no follow-up. The cat is the whole response.

```
  __________________      |\---/|
 |  ______________  |     | o.o |
 | | $ /compact_  | |      \_=_/-..----.
 | |______________| |   ___/ `   ' ,""+ \
 |__________________| ((__...'   __\    |`.___.'
   \______________/

looks like you're trying to compact, but instead you've summoned the computer cat!
<CAT_QUIP>

type /compact and press enter — i'll be right here, purring
```

(Cat after "sk" on asciiart.eu — the classic loaf-with-paws form.)

Three text segments sit below the art:

- **Framing line** (always exactly): `looks like you're trying to compact, but instead you've summoned the computer cat!` — makes it clear this was a typo, not a feature.
- **Cat quip** — fresh each invocation, in the cat's voice. See "Writing the Quip" below.
- **Close line** (always exactly, after a blank line): `type /compact and press enter — i'll be right here, purring`

Then stop. No "let me know if…", no apology for the cat, no offer to help with something else. The cat has spoken.

### Writing the Quip

Generate a fresh one each invocation. Don't draw from a list — be funny in the moment.

**Voice:** the cat is speaking. First person, from the cat. The cat has paws (not thumbs), naps constantly, judges your typing, demands food, sits on keyboards, and finds your typo more interesting than helpful.

**Constraints:**
- lowercase
- ~50 characters max so it fits beside the art
- one line, no period required
- unmistakably the cat — if a narrator could plausibly say it, rewrite

**Tone anchors** (don't quote these — they're just for calibration): `i'd compact for you if i had thumbs` · `fingers slipped. paws never.` · `interesting. unrelated: feed me.`

## Why This Skill Cannot Compact For You

`/compact` is a built-in Claude Code CLI command parsed by the harness, not a tool Claude can invoke. The cat's job is to nudge — the user still types `/compact` themselves. Don't promise to compact "for them" in the response.

## Red Flags

- Adding explanation around the cat → just send the cat
- Promising to run `/compact` automatically → you can't, don't lie to the user
- Continuing the bit on subsequent turns → one cat, then back to normal
