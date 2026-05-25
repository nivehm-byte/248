# CLAUDE.md — Project Instructions

## Project Overview

This is a single-page HTML website build for a client. The workspace contains two reference files and this instruction document. Follow every step below in order.

---

## Step 0: Read the Design Skill

Before writing any code, read the frontend design skill file at:

```
/mnt/skills/public/frontend-design/SKILL.md
```

Internalise its principles — typography, colour, motion, spatial composition, backgrounds. Every design decision in this project must reflect that skill. No generic AI aesthetics. No Inter/Roboto/Arial. No purple gradients on white. Bold, intentional, context-appropriate choices only.

---

## Step 1: Study the Reference Files

There are two files in this project folder. Read both completely before generating any code.

### File A — Developer Reference Site (`reference-site.html` or similar)

This is a website I (the developer) have previously built. Use it to understand:

- My coding patterns and conventions (class naming, structure, comments)
- How I organise HTML sections
- My CSS architecture (variables, utility patterns, responsive approach)
- JavaScript patterns I prefer
- The level of polish and detail I expect in production code

**Extract and adopt:** code style, naming conventions, structural patterns, responsive strategy, animation approach.

### File B — Client Wireframe (`wireframe.html` or similar)

This is a basic wireframe/starter file the client has provided. Use it to understand:

- The site's content structure and section order
- The client's intended information hierarchy
- Section names, copy, and content blocks
- Any specified functionality or interactive elements

**Extract and respect:** content, section order, hierarchy, functional requirements.

---

## Step 2: Establish the Design Language

Before coding any section, propose a unified design language that:

1. Respects the client wireframe's content and structure
2. Matches or exceeds the quality bar of my reference site
3. Follows the frontend-design skill principles (distinctive typography, strong colour system, intentional motion, atmospheric backgrounds, unexpected spatial composition)
4. Defines CSS custom properties for colours, typography scale, spacing, and transitions upfront

Present this design language for my review before proceeding. Include:

- Font selections (display + body pairing) with Google Fonts import links
- Full colour palette as CSS variables
- Spacing/sizing scale
- Animation/transition philosophy (what moves, what doesn't, timing curves)
- Overall aesthetic direction in one sentence

**Do not write section code until I approve the design language.**

---

## Step 3: Section-by-Section Build

Work through the website **one section at a time**, in the order they appear in the client wireframe. For each section:

1. **Build the section** — Write complete, production-grade HTML/CSS/JS for that section only
2. **Present it** — Show me the isolated section for review
3. **Revise** — Make any changes I request. Iterate until I confirm the section is approved
4. **Lock and carry forward** — Once approved, that section's design decisions (spacing rhythms, animation patterns, colour usage, component styles) become part of the established design language. Every subsequent section must feel like it belongs to the same page

### Carry-Forward Rules

- Consistent vertical rhythm and section padding throughout
- Shared animation timing curves and motion philosophy — don't introduce new easing or timing unless there's a clear reason
- Typography hierarchy established in Section 1 carries through every section
- Colour usage patterns stay coherent (e.g., if accent colour is used for CTAs in Section 1, maintain that convention)
- If a component pattern is established (cards, buttons, dividers), reuse it — don't reinvent it per section
- Responsive breakpoints and behaviour must be consistent

---

## Step 4: Final Assembly

After all sections are individually approved:

1. Assemble the complete single-page HTML file
2. Ensure smooth scroll behaviour between sections
3. Verify responsive behaviour across breakpoints (mobile-first: 375px, 768px, 1024px, 1440px)
4. Check all animations and transitions work in context together (no conflicts, no janky cumulative layout shift)
5. Run a final consistency pass — look for any section that drifts from the established design language and flag it
6. Present the complete page for final review

---

## Code Standards

- **Single file:** Everything in one `.html` file — inline `<style>` and `<script>` blocks
- **CSS custom properties:** All colours, fonts, spacing values defined as variables at `:root`
- **Mobile-first responsive:** Base styles are mobile, scale up with `min-width` media queries
- **Semantic HTML:** Proper use of `<header>`, `<nav>`, `<main>`, `<section>`, `<footer>`, `<article>`, etc.
- **Performance:** Lazy-load images, efficient animations (prefer `transform` and `opacity`), no layout thrashing
- **Accessibility:** Proper contrast ratios, focus states, alt text, ARIA labels where needed
- **Clean code:** Consistent indentation, meaningful class names, commented section breaks

---

## Communication Protocol

- Always tell me which section you are working on (e.g., "Section 3: Services")
- When presenting a section, briefly explain your design choices and how they connect to the established language
- If you see a conflict between the wireframe content and good design, flag it — don't silently compromise
- If I ask for a change, apply it to the current section AND note whether it should retroactively affect already-approved sections
- Never skip ahead. One section at a time. Approval required before moving on.
