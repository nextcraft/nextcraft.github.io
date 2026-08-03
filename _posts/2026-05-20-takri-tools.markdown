---
layout: post
title:  "Takri Tools: Putting a living script back on the keyboard"
date:   2026-05-20 10:00:00
categories: nextcraft
---

<figure class="post-figure post-figure--emblem">
  <img src="{{ site.baseurl }}/images/blog/takri.png" width="500" height="500" alt="Ornate gold emblem on black: the word Takri written in Takri script, ringed by a traditional floral circular border." />
  <figcaption><span class="takri takri--display">𑚔𑚭𑚊𑚤𑚯</span> — Takri, rendered in its own script.</figcaption>
</figure>

Scripts do not disappear overnight. They fade when it becomes harder to type them than to abandon them — when learning materials thin out, when fonts fail, when every draft has to be drafted somewhere else first. **Takri** (<span class="takri">𑚔𑚭𑚊𑚤𑚯</span>) has lived that story for generations of Dogri, Kangri, and other Pahari speakers across the western Himalayas.

Today we are releasing **[Takri Tools](https://nextcraft.github.io/takri-tools/)**: a small, open suite for producing Takri text and practising the alphabet in the browser. The source lives with us at [github.com/nextcraft/takri-tools](https://github.com/nextcraft/takri-tools). This post is about the script, the tools, why they matter, and where we hope the work goes next.

## A script with roots — and a Unicode address

Takri belongs to the Brahmic family. It is a sibling of Devanagari more than a stranger to it: the inventories line up closely enough that someone who can read Hindi or Dogri in Devanagari already holds a map of Takri’s vowels, consonant rows, and signs. Historically it carried local languages of Himachal and Jammu — not as a museum curiosity, but as ordinary writing.

What changed in the digital era was infrastructure. Takri entered Unicode in version 6.1, in the block **U+11680–U+116CF**: independent vowels, consonants, vowel signs, virama, nukta, digits, and related marks. Encoding is necessary; it is not sufficient. Without fonts that render, keyboards that compose, and tools that teach, a code chart stays a chart. Noto Sans Takri and related open fonts closed part of that gap. The remaining gap is everyday practice — typing, checking, and learning without a specialist toolchain.

That is the gap Takri Tools aims at.

## What we shipped

### Transliterator

You type in **Roman** using the Aksharamukha Readable scheme and see **Devanagari** and **Takri** side by side. The Devanagari column is deliberate: it is the verification rail for readers who already know that script. Once the line looks right there, the Takri column is ready to copy.

Two modes cover different needs:

- **API mode** calls the public [Aksharamukha](https://aksharamukha.appspot.com/) service for high-accuracy conversion, including awkward conjuncts.
- **Offline mode** runs a built-in tokenizer and mapping engine from our shared Takri/Devanagari/Roman tables — instant, private, and usable without a network.

A keyboard-mapping reference chart is in the same page, so the Roman scheme does not have to be memorized before the first useful sentence.

### Practice sheets

Learning a script by staring at a chart is slow. We generate **printable PDF worksheets**: choose vowels, consonant rows, or numerals; set how many practice rows you want; pick Takri alone or Takri with Devanagari and Roman glosses; preview; download for A4 or Letter. Guide glyphs sit in the early cells so a learner’s hand has something to follow before the ruled lines take over.

Under the hood, shared data in `takri-mappings` is the single source of truth for both tools — Unicode characters, Devanagari peers, and Roman keys stay aligned as we grow the suite.

## Why this is impactful for Takri

Preservation is often framed as archiving. Archiving matters. But a script survives when people **produce** with it: a caption, a classroom handout, a name on a poster, a line in a notebook. Takri Tools lowers the cost of that production.

- **From encoding to expression.** Unicode made Takri representable; the transliterator makes it reachable from a Latin keyboard without installing an IME on day one.
- **From chart to muscle memory.** Practice sheets turn the block U+11680 into something you can photocopy for a workshop or a kitchen table.
- **From specialist stack to a URL.** Teachers, students, and curious readers do not need a local build of Aksharamukha to try a sentence. Open the site, type, copy.
- **From opaque conversion to checkable output.** Pairing Takri with Devanagari respects how bilingual literacy actually works in the region and reduces silent errors.
- **From closed tooling to a forkable commons.** MIT-licensed code, mappings credited to Aksharamukha and Unicode, fonts from Noto — the path to improve the tools is the same path as using them.

None of this revives a script alone. It removes friction that has kept revival work stuck in PDFs and private notes.

## Directions we want to take next

The roadmap is open on purpose. Ideas we care about:

1. **Richer input.** Direct Takri and Devanagari keyboards in the page; better handling of edge cases offline so API and offline stay closer.
2. **Teaching packs.** Ready-made lesson sequences, stroke order where sources allow, and worksheets tuned for Dogri or Kangri orthography rather than a generic chart.
3. **Corpus helpers.** Lightweight utilities to convert short passages, gloss parallel text, or check consistency against known mappings — still in-browser where we can.
4. **Community fonts and samples.** Showcase pages that stress-test Noto and other Takri faces; sample texts with clear licensing for classrooms.
5. **Applied AI, carefully.** Evaluation sets for transliteration quality, assistive suggestions that stay inspectable, and localization of UI copy into regional languages — always with humans in the loop for cultural claims.
6. **More instruments in the suite.** Dictionaries, flashcards, and reading views belong beside the two tools we have now.

If one of those is your itch, we would rather you open an issue than wait for us to invent your use case.

## Contribute

Takri Tools was built and released together under Next Craft because this is what the collective is for: member ideas reaching daylight, in the open, where the next person can extend them.

You can help by:

- **Using the tools** and telling us where they fail — wrong conjuncts, missing glyphs, awkward worksheet layouts.
- **Improving mappings and tests** in the repository so offline mode earns more trust.
- **Writing or translating** short teaching notes that we can link from the app.
- **Filing issues and pull requests** at [github.com/nextcraft/takri-tools](https://github.com/nextcraft/takri-tools).
- **Carrying worksheets into a real room** — a class, a reading group, a family — and reporting what learners actually needed.

Live site: [nextcraft.github.io/takri-tools](https://nextcraft.github.io/takri-tools/)  
Source: [github.com/nextcraft/takri-tools](https://github.com/nextcraft/takri-tools)  
Unicode chart: [U+11680](https://www.unicode.org/charts/PDF/U11680.pdf)

Takri has a code point range. With enough shared craft, it can have a keyboard habit again. We hope you will help us build toward that.
