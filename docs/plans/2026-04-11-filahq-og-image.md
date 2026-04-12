# FilaHQ OG Image Implementation Plan

> **For Claude:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task.

**Goal:** Generate a text-first Statify Open Graph image and wire it into the Astro page metadata.

**Architecture:** Keep the asset pipeline simple by generating one final bitmap, saving it under `public/`, and referencing it directly from the layout metadata. Do not add image-generation abstractions or a custom asset system.

**Tech Stack:** Astro 6, static public assets, built-in image generation workflow

---

### Task 1: Add the design note

**Files:**
- Create: `docs/plans/2026-04-11-filahq-og-image-design.md`

**Step 1: Save the approved OG image design**

- Record the headline, format, palette, and composition.

### Task 2: Generate the OG image asset

**Files:**
- Create: `public/og-statify.png`

**Step 1: Generate a single text-first poster image**

- Use the approved headline.
- Match the site palette and direction.
- Save the selected final image into `public/`.

### Task 3: Wire the metadata

**Files:**
- Modify: `src/layouts/Layout.astro`

**Step 1: Add Open Graph and Twitter image metadata**

- Reference `/og-statify.png`
- Keep the title and description aligned with the current landing page.

### Task 4: Verify output

**Files:**
- Verify: `public/og-statify.png`
- Verify: `src/layouts/Layout.astro`

**Step 1: Run the build**

Run: `npm run build`
Expected: Astro build succeeds.
