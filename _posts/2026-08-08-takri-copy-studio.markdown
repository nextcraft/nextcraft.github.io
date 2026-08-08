---
layout: post
title:  "Takri Copy Studio: A copy bench for design tools that forget the script"
date:   2026-08-08 15:30:00
categories: nextcraft
---

<figure class="post-figure">
  <img src="{{ site.baseurl }}/images/blog/copy-studio-clock.gif" width="482" height="482" alt="Animated clock face over a sunlit mountain valley — time passing while the landscape stays calm." />
  <figcaption>Copy Studio is built for the gap between typing Roman and pasting Takri into a poster — without losing an afternoon to font failures.</figcaption>
</figure>

When a magazine ships, the words do not arrive fully dressed. A designer lays out the page in InDesign. An editor opens the same layout in **Adobe InCopy** and works the text in place — copyfitting headlines, trimming captions, fixing overflows — while the geometry stays under the designer's hand. The editorial layer is a **staging bench**: compose, check, copy at the right granularity, hand off. Nothing about that workflow assumes Latin.

Takri has the opposite problem. Unicode gave it a block (**U+11680–U+116CF**). Noto Sans Takri gave it a face. But the everyday path from "I know what this should say" to "this line is on my Canva poster" still breaks: design tools like **Canva** and **Adobe Express** paste boxes instead of glyphs, and fixing one word means retyping the whole sentence.

Today we are adding **[Copy Studio](https://nextcraft.github.io/takri-tools/#/copy-studio)** to **[Takri Tools](https://nextcraft.github.io/takri-tools/)** — a browser workspace I built so anyone working with those design tools has a smoother experience when staging Takri input: compose in Roman, verify through Devanagari, and hand off Takri text in the slice your layout actually needs.

## What professional copy studios do — and what we borrowed

In publishing, a **copy studio** (or copy desk) is not the printing press. It is the room where text is prepared for layout: checked against a second script, trimmed to fit, and released in pieces the production team can place without re-keying.

Adobe InCopy's model is the reference most designers know:

- **Parallel work.** Editors refine copy while layout evolves; neither side waits for a PDF round-trip.
- **Layout-aware editing.** You see real fonts and sizes, not a Word approximation.
- **Granular handoff.** A headline, a caption, a pull quote — copied at the unit the frame needs.
- **Copyfitting signals.** Overflow and fit are visible before ink hits paper.

Takri Copy Studio borrows that editorial shape, not the Adobe stack. You are not opening an INDD file. You are staging Roman input, verifying through Devanagari, and exporting Takri in the slice your design tool expects — sentence, line, word, or grapheme.

## What Copy Studio does

Open **[nextcraft.github.io/takri-tools/#/copy-studio](https://nextcraft.github.io/takri-tools/#/copy-studio)**. The page is a single-screen workshop tagged *Pahari script workshop · click to copy*.

### Compose in Roman, preview in two scripts

Type multi-line Roman text using the **Aksharamukha Readable** scheme — the same convention as the Transliterator. Devanagari and Takri previews render side by side at adjustable size (**24–96px**), so you can read the verification rail and inspect the output script at poster scale before you paste into Canva or Express.

Two transliteration modes match the rest of the suite:

- **Offline** — instant, private, no network; built on our shared mapping tables.
- **API** — Aksharamukha for awkward conjuncts; results merge per word so the workspace stays editable.

### Edit one word without rewriting the line

Double-click a word chip (or use the edit control) to change a single Roman token. The offline engine re-transliterates that word in place.

### Copy at sentence, line, word, or grapheme

A tools rail sets **copy granularity**:

| Mode | Use when |
|------|----------|
| **Sentence** | One click copies the full staged text |
| **Line** | Poster titles, stacked verses, address blocks |
| **Word** | Labels, names, single-token badges |
| **Character** | Glyphs that need isolating — conjunct parts, vowel signs, digits |

Grapheme mode uses **`Intl.Segmenter`** with `und-Takr` and `und-Deva` locales so clusters split correctly for Takri and Devanagari, not naive Unicode code points.

Choose **Takri** or **Devanagari** as the copy target. Click words in the interactive preview or the Word Workspace below; a toast confirms what landed on the clipboard.

### Copy Stack — your session's paste history

Every successful copy pushes an entry onto a **Copy Stack** (up to 108 items, persisted in `localStorage`). Re-open a clipped headline, compare two variants, or clear the stack when the layout is done. It is the lightweight traceability layer a copy desk keeps on a notepad — without email attachments.

### PNG export when paste fails

Canva, Adobe Express, and similar tools sometimes reject live Takri text even when the font exists on your system. Copy Studio can **download a PNG** of the full Takri render (Noto Sans Takri, gold on transparent) at your preview size. When the clipboard path breaks, the pixel path still works.

## Where it sits in Takri Tools

Copy Studio is the fourth live instrument in the suite:

1. **Transliterator** — quick one-off conversion
2. **Practice Sheets** — printable learning PDFs
3. **Character Reference** — browse and copy single code points
4. **Copy Studio** — multi-line staging for design production

The Transliterator is for "convert this paragraph once." Copy Studio is for "compose a poster, pull seven words out at different sizes, fix one spelling, paste into Express, export a PNG for the word the tool refused." Same mappings underneath; different editorial posture.

## Why this matters for Takri production

Revival work often stalls at the handoff. A classroom worksheet is printable; a festival poster is still designed in tools that assume Devanagari or Latin. Copy Studio lowers that last mile:

- **From conversion to composition.** Multi-line input, line-aware workspace, per-word surgery.
- **From blind paste to verified copy.** Devanagari preview stays visible while you click Takri words into the clipboard.
- **From font roulette to fallback export.** PNG when the design app's text engine fails.
- **From lost clips to a copy stack.** Session history for multi-asset layouts.

None of this replaces a community font strategy or a proper Takri keyboard. It removes the friction between "the transliteration is correct" and "the poster says it."

## Try it and extend it

**Live:** [nextcraft.github.io/takri-tools/#/copy-studio](https://nextcraft.github.io/takri-tools/#/copy-studio)  
**Source:** [github.com/nextcraft/takri-tools](https://github.com/nextcraft/takri-tools)  
**Suite overview:** [our earlier Takri Tools post]({{ site.baseurl }}{% post_url 2026-05-20-takri-tools %})

We would like to hear where Copy Studio fails in your real layouts — wrong conjunct splits, clipboard quirks in a specific app, PNG sizing for your template. Open an issue or pull request on the repository; MIT-licensed, same as the rest of the suite.

Takri spent decades as text drafted elsewhere first. Copy Studio is a small step toward drafting where the script belongs — and handing it off without the clock spinning on font work.
