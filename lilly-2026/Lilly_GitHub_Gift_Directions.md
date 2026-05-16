# Directions for Claude: Build the Lilly Conference Gift Page

*Paste this into your chat with Claude. It contains everything needed to build the page.*

---

## What you're building

A single-page **GitHub Pages site** — the take-home resource hub ("the gift") for faculty
who attended Megan Alstot's Lilly Conference session, **What are U.S. Undergraduate
Students Really Doing with GenAI?** (Austin, May 18, 2026).

Match the *structure and feel* of Megan's existing gift page —
https://malstot.github.io/cultivating-attention/ — single page, anchored sections, clean,
generous whitespace, calm and editorial. **But the visual brand is different.** That page
used Baylor green/gold; this one uses Megan's personal brand, **Editorial Mono**.

Build it as a static site: one `index.html` with embedded CSS in the `<head>`. Minimal to
no JavaScript — there is **no copy-to-clipboard feature** on this page. It is a clean,
branded landing page with five linked resources. It will be hosted via GitHub Pages.

---

## Brand: Editorial Mono

This is Megan's personal presentation brand. The gift page should feel like a natural
extension of her slide deck — same palette, same type pairing, same restraint.

### Palette — WCAG-verified, do not substitute

```
NEAR-BLACK            #0F0F0F   dark backgrounds, anchor text on light bg
OFF-WHITE             #FAFAFA   primary page background (the canvas)
PURE WHITE            #FFFFFF   card backgrounds sitting on the off-white canvas
SECONDARY (on light)  #595959   secondary/body text on off-white  (6.71:1, AA)
SECONDARY (on dark)   #9E9E9E   secondary text on near-black       (7.15:1, AAA)
SPARK (on light)      #8B2860   deep magenta — accents on light bg (7.83:1, AAA)
SPARK (on dark)       #E27DA8   pink magenta — accents on dark bg  (7.06:1, AAA)
RULE / BORDER         #D4D4D4   hairline borders, dividers
```

**Dual-spark rule — important.** No single magenta passes WCAG AA on both near-black AND
off-white. Use **deep magenta `#8B2860`** for any magenta element on a light background.
Use **pink magenta `#E27DA8`** for any magenta element on a dark background. They read as
the same color family. Never use `#8B2860` on dark or `#E27DA8` on light — both fail
contrast. Same logic for grays: `#595959` on light, `#9E9E9E` on dark.

**Backgrounds.** The page canvas is off-white `#FAFAFA`. The header (hero) band and the
footer are near-black `#0F0F0F`. Resource cards are pure white `#FFFFFF` with a hairline
`#D4D4D4` border. Avoid pure-white page background — the warm off-white is the brand.

### Typography

- **Headlines:** a serif — Georgia is the safe default. If you want a sharper option,
  load a web font (Source Serif 4 or similar) but Georgia is fully acceptable and
  dependency-free.
- **Body / labels / buttons:** a clean sans-serif — system stack is fine
  (`-apple-system, Segoe UI, Helvetica, Arial, sans-serif`).
- **Sentence case** for headlines, not Title Case.
- **Sparse bold.** Build hierarchy through size and color, not heavy body bolding.

### The magenta-period signature

Megan's brand signature: section headings end with a **period rendered in the spark color**.
On the off-white canvas that period is deep magenta `#8B2860`; in the dark header it is
pink magenta `#E27DA8`. The heading text itself is the normal text color — only the final
period carries the spark. Apply this to the hero headline and every section heading. It is
small, consistent, and the whole brand identity in one mark — get it right.

### The HITL identity

Megan's identity has two components that work together:

1. **The mark** — a circular **dotted ring** with **four small filled dots** at the
   cardinal positions (top, right, bottom, left). The dots and ring are in the spark color
   (`#E27DA8` on dark, `#8B2860` on light).
2. **The wordmark** — the text **HITL²**, where the `²` is a true superscript rendered in
   the spark color while "HITL" is in the standard text color. "HITL²" expands to
   *Humans-In-The-Learning-Loop, squared* — the squaring is the concept, so the `²` must
   be visible and colored, not muted chrome.

Use the mark + wordmark together as a small lockup. Place it in the **header** (near
Megan's name) and again in the **footer**. It does not need to repeat in every section —
it is a bookend, like on her slides. Build the ring with CSS (a `border` with
`border-style: dotted` on a circular element) and position the four dots as small
absolutely-positioned circles, or build the whole mark as a small inline SVG — either is
fine; SVG will be crisper.

### Overall feel

Calm, editorial, confident. Lots of whitespace. One column, comfortable reading width
(roughly 720–820px max content width, centered). Nothing busy. The page should feel like
the last page of a well-designed book, not a software dashboard. Restraint is the brand.

---

## Page content & structure

Single page, anchored sections. Recommended order:

### 1. Header (hero band — near-black background)

- Small eyebrow line in pink magenta: `Lilly Conference — Austin · May 18, 2026`
- Hero headline (serif, off-white, with pink-magenta period):
  **What are U.S. undergraduate students really doing with GenAI.**
  *(Note: on the slide deck the title ends in a question mark; for the gift page a period
  is fine, or keep the question mark in pink magenta — Megan's choice, default to the
  period for signature consistency.)*
- One-line subtitle in `#9E9E9E`: something like
  *Resources from the session — the framework, the lenses, and tools to take with you.*
- Presenter line: **Megan Alstot, Ph.D.** · Postdoctoral Research Associate, AI &
  Emerging Technologies · Academy for Teaching & Learning, Baylor University
- The HITL mark + HITL² wordmark lockup, small, in this header

### 2. Short intro / welcome (off-white canvas)

Two or three sentences, warm and brief. Purpose: orient the visitor and set the tone.
Megan will likely refine the wording; placeholder copy is fine. Something like:

> *Thank you for spending part of your afternoon with these nine students. Everything we
> looked at together is here — plus the framework and the practical tools, ready for you
> to use and adapt. Take what's useful.*

### 3. The five resources

These are the heart of the page. Present them as **resource cards** — pure-white cards
with a hairline border on the off-white canvas, each with a heading (magenta-period
signature), a 1–2 sentence description, and a clear link/button. Cards can be a simple
responsive grid or a single stack; given there are five, a stack of full-width cards or a
2-column grid both work. Keep link buttons consistent — near-black button with off-white
text, or off-white with a deep-magenta border; pick one and use it for all five.

The five resources, each its own card:

1. **The Conceptual Framework.**
   *Alstot's Conceptual Framework for AI Literacy in a GenAI-Integrated Knowledge Network.*
   Display the framework image on the card (file provided — see Assets below).
   No external link needed; the image is the resource. Optionally allow it to open
   full-size.

2. **The Lenses for AI Literate Learning.**
   *Alstot's Lenses for AI Literate Learning — a practitioner tool for locating where your
   teaching meets students' AI literacy.*
   Display the lenses image on the card (file provided — see Assets below).
   Same treatment as the framework.

3. **The Guardrail Prompt Library.**
   *A faculty resource for building student agency with AI — a master guardrail prompt,
   discipline-specific prompts, executive-function supports, and syllabus language.
   Copy and personalize for your courses.*
   Link out to the Google Doc. **[ MEGAN: paste Google Doc URL ]**

4. **The Presentation Slides.**
   *The full session deck as a PDF.*
   Link to the PDF. **[ MEGAN: paste slides PDF URL — or note if the PDF will live in
   the GitHub repo itself, in which case link to the relative path ]**

5. **The Padlet.**
   *The collaborative wall from our session — the room's collective noticing about each
   student.*
   Link to the Padlet. **[ MEGAN: paste Padlet URL ]**

### 4. The research behind it (off-white canvas)

A short section pointing to the dissertation:

- One or two sentences framing it: *This session draws on a two-year mixed-methods study
  of U.S. undergraduate AI use.*
- Link to the dissertation in ProQuest. **[ MEGAN: paste ProQuest URL ]**
- Citation in small `#595959` text:
  *Alstot, M. (2026). Generative artificial intelligence and the metaliterate learner: A
  mixed methods study of AI-literacy and US undergraduate students' interaction within an
  AI-integrated knowledge economy [Doctoral dissertation, Pepperdine University].*

### 5. Footer (near-black background)

- The HITL mark + HITL² wordmark lockup again
- Megan's name and contact: **megan_alstot@baylor.edu**
- Optional: *Academy for Teaching & Learning, Baylor University*
- Keep it quiet and simple — pink-magenta accents, `#9E9E9E` secondary text

---

## Assets you'll need in the project

Megan will provide these files — make sure they're in the project before building:

- `HITL_framework.jpg` — the conceptual framework graphic (for resource card 1)
- `HITL_lenses.jpg` — the lenses graphic (for resource card 2)
- For GitHub Pages, place images in the repo (e.g., an `/images` folder) and reference
  them with relative paths in `index.html`.

The three external links (Guardrail Google Doc, Padlet, ProQuest dissertation) and the
slides PDF link are placeholders above — Megan will paste the real URLs.

---

## Technical notes for GitHub Pages

- Deliver a single `index.html` with all CSS embedded in a `<style>` block in the `<head>`.
- Include `<meta name="viewport" content="width=device-width, initial-scale=1">` and make
  the layout responsive — it must read well on a phone, since faculty will scan a QR code
  to reach it. Single-column, fluid width, comfortable tap targets.
- Include a meta description for the page.
- Set the page `<title>` to something like:
  *What U.S. Undergraduates Are Doing with GenAI — Faculty Resources | Megan Alstot*
- Accessibility: maintain the WCAG ratios above, use real heading hierarchy
  (`h1` → `h2` → `h3`), give every image meaningful `alt` text, ensure links are
  descriptive (not "click here"), and make sure focus states are visible.
- No build tooling, no frameworks — plain HTML/CSS so it drops straight into a GitHub
  Pages repo. Minimal or zero JavaScript.

---

## Working style

- Confirm the plan before building, then build the full `index.html`.
- After building, describe what was made briefly — don't over-explain.
- If something is ambiguous, ask one clear question rather than guessing.
- Megan has strong design taste and edits ruthlessly; push back honestly if a request
  would weaken the page.

---

*End of directions.*
