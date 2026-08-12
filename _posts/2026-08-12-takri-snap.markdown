---
layout: post
title:  "Takri Snap: Match the letter, beat the clock"
date:   2026-08-12 23:59:00 +0530
categories: nextcraft
---

<figure class="post-figure post-figure--emblem">
  <img src="{{ site.baseurl }}/images/blog/kalaa.png" width="500" height="500" alt="Ornate gold emblem on black: the Takri word for play (khelā) ringed by a traditional floral circular border." />
  <figcaption><span class="takri takri--display">𑚸𑚲𑚥𑚭</span> — khelā, play. The arcade face of Takri Tools.</figcaption>
</figure>

Charts teach you what a letter looks like. Worksheets teach your hand to draw it. Neither one trains the split-second judgment you need when a glyph flashes past and you have to say: *is that the right pair?*

That judgment is how bilingual readers actually use Takri in the wild — not by recalling a Unicode chart, but by recognizing whether 𑚊 belongs with क, or whether someone just put the wrong neighbour on the card.

Today we are adding **[Takri Snap](https://nextcraft.github.io/takri-tools/#/trainer)** to **[Takri Tools](https://nextcraft.github.io/takri-tools/)** — a browser arcade for letter recognition. Swipe YEP or NAH. Or pick the matching Takri from two options. Blitz against a clock, or Flow until you are done. Same mappings as the rest of the suite; different posture: play until the eye gets faster than the doubt.

## Why a game, not another chart

Takri and Devanagari sit close enough that a reader of Hindi or Dogri already holds a map. The hard part is making that map automatic. A reference page lets you look something up. A practice sheet lets you copy a row. Snap forces a binary call under light pressure:

- Does this Takri letter match the claimed Devanagari (or Roman) pair?
- Or is it a distractor from the same row — the neighbour that looks almost right until you look twice?

Fake pairs are not random noise. Distractors prefer the same consonant row or vowel group whenever the deck allows, so mistakes feel like real confusions rather than lottery tickets. That is the pedagogical bet: recognition sticks when the wrong answer is *plausible*.

## How to play

Open **[nextcraft.github.io/takri-tools/#/trainer](https://nextcraft.github.io/takri-tools/#/trainer)**. The lobby is tagged *Arcade mode*. Choose a play style, a timer, a deck, and go.

### Swipe — YEP or NAH

Each card shows a Takri letter against a claimed pair. Fling **right** if they match (YEP), **left** if it is a fake (NAH). Buttons and keyboard arrows work the same way for desks without a touch surface.

You can set the claim side to **Devanagari** or **Roman**, depending on which verification rail you already trust.

### Pick — tap the matching Takri

A Devanagari and Roman pair sits in the centre. Two Takri options flank it. Tap the one that belongs. Same decks, same scoring — a calmer layout when you want less fling and more deliberate choice.

### Blitz or Flow

| Mode | What it does |
|------|----------------|
| **Blitz** | 45-second clock. Streak multipliers boost score. Every 5-streak earns **+3 seconds** (capped at 60s). |
| **Flow** | Same cards, no timer. End the round when you are ready. |

Streaks matter. Score scales with how long you stay hot; milestones toast *Nice streak!*, *On fire!*, *Unstoppable!*, *Legendary!* — light noise for a serious drill.

### Decks that match the worksheets

Snap reuses the Practice Sheets groupings so a classroom can move from paper to play without remapping the alphabet:

- **Core letters** — vowels plus the main consonant rows
- **Vowels only** / **All consonants** / **Numerals**
- Optional **vowel signs & special consonants** when you want the advanced edge of the block

Deep links from Character Reference can pre-select a group in the lobby, so a glyph you just looked up can become the next drill set.

## After the round

Results show score, accuracy, best streak, and a **glyphs to review** list — misses from this session first, otherwise your weakest letters from saved history. Tap a glyph to open it in Character Reference. Or send the missed groups straight into Practice Sheets for a printable follow-up.

Progress lives in `localStorage`: games played, best Blitz score, best streak, and per-glyph hit/miss counts. No account. No leaderboard server. Just enough memory that tomorrow's lobby remembers yesterday's fire.

## Where it sits in Takri Tools

Snap is the recognition instrument beside the production and reading tools:

1. **Transliterator** — convert a line once
2. **Practice Sheets** — print and write
3. **Character Reference** — look up a code point
4. **Copy Studio** — stage text for design tools
5. **Takri Reader** — decode and study passages
6. **Takri Snap** — train the eye under a clock

The Reader teaches you to *read* a word in context. Snap teaches you to *trust* a letter when the pair is either true or almost true. Different muscles; same script.

## Why this matters for Takri learning

Revival work needs production tools and teaching tools. It also needs low-friction practice that people will actually open twice.

- **From looking up to recognizing.** Charts answer "what is this?"; Snap answers "do these belong together?" before you have time to open the chart.
- **From isolated glyphs to row-aware mistakes.** Same-section distractors mirror how learners actually confuse letters.
- **From one-shot worksheets to a loop.** Miss → review in Character Reference → print the group → play again.
- **From specialist software to a URL.** Teachers and curious readers get an arcade without installing anything.

None of this replaces a teacher, a corpus, or a proper keyboard. It turns idle minutes into letter judgment — the skill that makes every other Takri tool feel less foreign.

## Try it and extend it

**Live:** [nextcraft.github.io/takri-tools/#/trainer](https://nextcraft.github.io/takri-tools/#/trainer)  
**Source:** [github.com/nextcraft/takri-tools](https://github.com/nextcraft/takri-tools)  
**Suite overview:** [our earlier Takri Tools post]({{ site.baseurl }}{% post_url 2026-05-20-takri-tools %})

We would like to hear which decks feel too easy, which distractors feel unfair, and whether Blitz or Flow is what you actually use in a classroom. Open an issue or pull request on the repository; MIT-licensed, same as the rest of the suite.

Takri revival needs keyboards and corpora. It also needs the habit of *seeing* the script correctly, fast. Snap is a small arcade for that habit — YEP when they match, NAH when they do not, until the eye stops hesitating.
