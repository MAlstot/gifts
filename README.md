# gifts/ecs-2026 — upload notes

Drop this whole folder into the **MAlstot/gifts** repo as a sibling of `moody-2026`,
so it publishes at:

    https://malstot.github.io/gifts/ecs-2026/

That is the URL encoded in the QR code on slide 25 of the deck.

## Contents

    ecs-2026/
      index.html                         the gift page
      TeachForIntegrity-ECS-2026.pdf     the slides (PLACEHOLDER — replace, see below)

## Two things to do after you push

1. **Replace the PDF.** The one in here was rendered by LibreOffice and the fonts are
   approximate. Export your own from PowerPoint using the exact same filename
   (`TeachForIntegrity-ECS-2026.pdf`) so the link on the page keeps working.
2. **Scan the slide-25 QR from your phone** once the folder is live, before the session.

## How this one differs from moody-2026

The Moody gift was a frozen, self-contained snapshot — every tool copied into the folder.
This one links to the live tools already published in `gifts/moody-2026/` and
`AI-literacy/` instead of duplicating them. One copy to maintain, and fixes you make in
either repo show up here automatically. If you would rather freeze it, copy the six
linked HTML files into this folder and change the absolute URLs in `index.html` to
relative ones.

## The six tools on the page (v3 — Megan's selection)

    1  Learner Information Survey     gifts/moody-2026/learner-survey.html  (+ .docx)
    2  The Eleven Reasons             AI-literacy/tfm6elevenreasons.html
    3  Guardrail starter handout      Google Doc — see the warning below
    4  The AI Literacy Continuum      AI-literacy/tfm4continuumcognitive.html
    5  Assignment Integrity Stress Test  gifts/moody-2026/copilot-paste-prompt.html
    6  Draft Your Disclosure Stance   AI-literacy/tfm6disclosurestance.html

Also linked: gifts/moody-2026/attribution-license.html

**Deliberately NOT here:** the Integrity Diagnostic (`tfm6integritydiagnostic.html`) —
Megan uses the Eleven Reasons matrix instead. Also dropped from v1 of this page: the
CARE reference, the continuum self-evaluation, the Design Prompt Starters, and the
Guardrail Starters builder.

## ⚠ Google Doc sharing — check this before the session

The guardrail starter handout is a Google Doc, not a page in this repo:

    https://docs.google.com/document/d/1JXOGM3bCO37cRWAm5fiJ5qbMCuwZZFu4BNJTFOc9GGs

The page links `/view` and offers `/copy` as a secondary link. **Both fail unless the
doc's sharing is set to "Anyone with the link — Viewer."** Check it from a logged-out
browser before you hand out the QR.
