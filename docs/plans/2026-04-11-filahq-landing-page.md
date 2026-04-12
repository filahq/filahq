# FilaHQ Landing Page Implementation Plan

> **For Claude:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task.

**Goal:** Replace the default Astro starter page with a Statify-led FilaHQ landing page that highlights the three current products and their cross-platform workflow.

**Architecture:** Keep the implementation intentionally small by using the existing Astro layout and a single landing page entrypoint. Put page metadata and global tokens in the layout, and keep the landing page structure and section styling in `src/pages/index.astro`.

**Tech Stack:** Astro 6, plain `.astro` templates, scoped CSS

---

### Task 1: Replace the default document shell

**Files:**
- Modify: `src/layouts/Layout.astro`

**Step 1: Update metadata and base document styling**

- Set a FilaHQ/Statify page title and description.
- Add font preconnect/import if needed.
- Establish background and text defaults for the new dark theme.

**Step 2: Run build to catch document-level issues**

Run: `npm run build`
Expected: Astro build succeeds.

### Task 2: Build the landing page structure

**Files:**
- Modify: `src/pages/index.astro`

**Step 1: Remove the starter import and write the page sections**

- Add hero, workflow, integration teaser, product detail, closing CTA, and footer sections.
- Add current product copy for:
  - Statify
  - Statify Easy Widget
  - Statify Extension

**Step 2: Add direct action links**

- Add two Composer install actions.
- Add one Chrome Web Store action placeholder that can be swapped to the live URL.

**Step 3: Run build to verify page compiles**

Run: `npm run build`
Expected: Astro build succeeds with the new page.

### Task 3: Apply the approved visual direction

**Files:**
- Modify: `src/pages/index.astro`
- Modify: `src/layouts/Layout.astro`

**Step 1: Add the design tokens and section styles**

- Use `#ffcc00` and `#343434` as the primary palette anchors.
- Create a full-bleed hero treatment with strong typography.
- Add lightweight motion and reveal effects with CSS only.
- Make the layout responsive for desktop and mobile.

**Step 2: Run build again**

Run: `npm run build`
Expected: Astro build succeeds after styling changes.

### Task 4: Final verification

**Files:**
- Verify: `src/layouts/Layout.astro`
- Verify: `src/pages/index.astro`
- Verify: `docs/plans/2026-04-11-filahq-landing-page-design.md`
- Verify: `docs/plans/2026-04-11-filahq-landing-page.md`

**Step 1: Review copy and CTA destinations**

- Confirm Statify remains the flagship.
- Confirm FilaHQ is positioned as the studio behind the stack.
- Confirm future integrations are presented as coming soon, not already shipped.

**Step 2: Run final build**

Run: `npm run build`
Expected: Astro build succeeds with no errors.
