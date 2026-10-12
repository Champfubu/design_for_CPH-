---
name: design-for-cph
description: Design or improve UX/UI and visual artifacts for Chaiyaphum Hospital (CPH, โรงพยาบาลชัยภูมิ), combining UI/UX Pro Max, Frontend Design, and Taste guidance with the real hospital logo, purple-led purple/green/orange colors, and logo backgrounds or watermarks. Use when CPH branding is requested or the artifact is explicitly for CPH; do not apply this identity to unrelated organizations.
---

# design_for_CPH

Create a recognizable Chaiyaphum Hospital identity with frequent, purposeful use of its logo, purple as the dominant brand color, and green/orange as supporting colors. Apply to CPH websites, apps, dashboards, presentations, documents, and graphics while respecting the requested scope and existing technology.

## Compose the three design skills on invocation

When this skill is invoked for design work, load the installed entrypoints below before choosing the design approach. Read them once per task, then use only the guidance applicable to the requested surface. These are local instruction files to read and apply, not executable skill calls or separate agents.

| Installed entrypoint (relative to this skill folder) | Skill name | Contribution |
| --- | --- | --- |
| [UI/UX Pro Max](../ui-ux-pro-max/SKILL.md) | `ui-ux-pro-max` | Searchable UX, accessibility, responsive layout, interaction, charts, and implementation guidance |
| [Frontend Design](../frontend-design/SKILL.md) | `frontend-design` | Intentional visual direction, Thai-capable typography, hierarchy, spacing, purposeful copy, and visual critique |
| [Taste](../taste-skill/SKILL.md) | `design-taste-frontend` | Brief-driven polish, audit before redesign, consistent shape/theme, restrained motion, and avoidance of generic landing-page patterns |

Resolve sibling links from this skill's directory, not the project's working directory. The default installation is `C:\Users\user\.codex\skills`. If a skill is missing, state which one is unavailable and continue with the available guidance plus the CPH rules; do not pretend it was loaded. Installation sources and pinned revisions are in [references/design-skill-sources.md](references/design-skill-sources.md).

### Decide by surface

- **Hospital public site, landing page, or welcome/login surface:** combine all three. State the audience and design direction briefly, choose a calm, trustworthy CPH identity, and inspect existing content before a redesign. For Taste dials, public-service starting values are `DESIGN_VARIANCE: 3`, `MOTION_INTENSITY: 2`, `VISUAL_DENSITY: 5`; adjust to the actual brief.
- **Clinical/operational dashboard, data table, or multi-step form:** use UI/UX Pro Max for workflow and interaction and Frontend Design for visual craft. Taste explicitly excludes these product surfaces: record that applicability decision and do not force its marketing layouts, abbreviated content, image quotas, or hero rules onto them. Preserve useful data density, actions, filters, and form sequence.
- **Documents, slides, and static graphics:** draw relevant typography, contrast, alignment, visual hierarchy, and consistency principles from the three skills. Use the appropriate artifact skill for implementation and rendering. Web frameworks, animation libraries, web vitals, hero constraints, and web interaction checklists do not apply to printed/static output.
- **A focused component fix:** read the entrypoints but keep application focused on that component; use targeted UX search and relevant craft checks rather than rebuilding the page.

### Search, synthesize, implement

1. Inspect the audience, main task, existing components/tokens, and actual technology. Summarize the intended direction briefly; proceed with a reasonable choice when context is sufficient.
2. For a new interface or broad redesign, run UI/UX Pro Max's local search with `--design-system`. For a focused concern use `--domain ux` (or the relevant domain). Use a separate `--stack` search only for the detected stack; do not assume React/Next.js. Use generic English queries such as `hospital patient portal` or `keyboard focus modal`, without patient or confidential project data.
3. Invoke `../ui-ux-pro-max/scripts/search.py` by its resolved absolute path with a working Python 3 interpreter. On this machine, if the Windows `python` alias is unavailable, the bundled interpreter is `C:\Users\user\.cache\codex-runtimes\codex-primary-runtime\dependencies\python\python.exe`; use `-X utf8`. Example arguments: `"hospital patient portal" --design-system -p "CPH" --variance 3 --motion 2 --density 5`. Do not rely on the upstream Claude plugin path.
4. Check that results fit the surface. Retry an off-topic or empty search once with a narrower query, then label general guidance as fallback if needed. Convert verified recommendations into a compact CPH design plan: brand tokens, Thai typography, layout/hierarchy, interaction states, logo placement, and watermark placement. Search-generated palettes and font pairs are suggestions; replace conflicting colors with the CPH palette and select fonts that actually support Thai.
5. Implement with the existing stack and shared components. Apply Frontend Design's plan/build/critique approach and Taste's applicable polish checks. Fix usability and accessibility first, then hierarchy and spacing, then decoration. Choose purposeful feedback and respect reduced motion.
6. Validate against the CPH checks below and the applicable source-skill checks. In delivery, briefly identify which sources informed the work, any applicability exclusions, and the verification actually completed.

### Resolve conflicts in favor of the CPH brief

The user's current request, CPH identity, accessibility, and real workflow govern the synthesis. Generic stylistic defaults must adapt to them:

- Keep CPH purple even when an anti-template rule discourages generic purple. Use the real logo and restrained brand composition rather than arbitrary purple gradients.
- Keep green/orange as supporting colors even when Taste suggests only one accent. Purple remains primary; semantic and chart colors remain readable.
- Replace generic sales CTAs, pricing, testimonials, certification badges, and proof metrics from search suggestions with the real hospital service workflow and verified content. A hospital-related search can still return a commercial landing pattern; never treat that as evidence that CPH needs sales copy or invented credibility claims.
- Keep the supplied JPEG logo and its white container even when a source favors SVG or off-white surfaces. Never generate a replacement hospital mark.
- Preserve Thai names, content, line breaking, and useful data; English word limits or headline line caps are contextual, not reasons to truncate essential hospital information.
- Respect the existing stack, theme, routes, forms, and design system. Do not add React, Tailwind, GSAP, a new component system, dark mode, or mandatory generated images solely because a source assumes them. Existing assets and the logo watermark may satisfy the actual brief. Generated imagery must not be presented as a real CPH facility, staff member, endorsement, or patient.
- Applying these skills means improving the requested design. Do not rewrite or download newer upstream skills on every invocation. When the user requests a skill update, inspect the new source and adapt this integration deliberately while preserving CPH branding and license/provenance records.

## Logo and placement

- Use the actual logo in [assets/logoCPH.jpg](assets/logoCPH.jpg). It is a bundled, unchanged copy of `C:\Users\user\Documents\CPH\logoCPH.jpg` so the skill remains usable without the original path.
- Include the logo wherever practical: app header or sidebar, login/welcome screen, landing hero, footer, report masthead, presentation title/closing slide, and printable output. Prefer one clear logo per structural area; for a compact dialog or table, inherit branding from the surrounding screen instead of crowding the content.
- Include a subtle logo background or watermark when creating a new CPH screen or major artifact surface. For small scoped edits, add it only within the requested area when suitable. Use a large, softly faded logo on a page, hero, login panel, or report background, normally at 3–6% opacity; a larger range up to 8% may work on spacious cover pages after visual inspection.
- Keep foreground logos legible, preserve their aspect ratio, and leave clear space. Do not crop the hospital name, recolor the official logo, stretch it, recreate it from text, or substitute a generated emblem.
- The supplied JPEG has an opaque white background. On colored surfaces, place the foreground logo in a white container. For a watermark, fade the entire image over a light surface. Do not claim it has transparency or simulate background removal in a way that damages the mark. Use a genuine transparent asset if the user later provides one.
- Copy the asset into the project's normal public/assets location and reference it with a working project URL; never embed a local Windows path into a deployed website. Embed the actual image in documents and slide files.

## Purple-led color system

These seed colors were sampled from the supplied JPEG, not from an official brand manual:

| Role | Color | Use |
| --- | --- | --- |
| Logo purple | `#A05CA5` | Brand accents and visual identity |
| Logo green | `#0F6F41` | Supporting identity and selected positive states |
| Logo orange | `#EC7644` | Small highlights and selected attention states |
| Primary purple | `#74377B` | Main actions, active navigation, emphasis; darker derivative for readability |
| Deep purple | `#54245A` | Hover/pressed emphasis and strong headings |
| Pale purple | `#F5EDF7` | Section backgrounds and selected surfaces |
| Canvas | `#FCFAFD` | Light overall background |
| Ink | `#2D2430` | Main content text |

- Let purple carry the visual identity through primary actions, navigation, headings, focus rings, and light surface tints. Keep green and orange secondary; avoid giving all three colors equal prominence.
- Use neutral space generously so repeated hospital branding remains calm and professional. Avoid generic purple gradients as a substitute for the hospital identity.
- Treat these as starting tokens, adapted to the existing design system. Verify text and control contrast for the actual foreground/background pair. White text over the lighter logo purple or orange needs checking; prefer the darker primary purple for filled actions.
- Keep semantic states clear: errors, warnings, successes, chart series, and clinical status must remain distinguishable with labels/icons as well as color. Brand colors do not override established clinical meaning.

## UX/UI decisions

- Use Thai-first labels when the audience is Thai; use the hospital name `โรงพยาบาลชัยภูมิ` and optional `CHAIYAPHUM HOSPITAL` consistently. Choose an available Thai-capable font with comfortable line height; do not silently add a remote font dependency.
- Prioritize the real workflow: clear page title, visible main action, concise field labels, helpful validation, and appropriate loading, empty, error, and success states. Keep dense operational tables readable and preserve the information needed for the task.
- Make layouts work on desktop and mobile. Preserve keyboard access, visible focus, touchable controls, and readable text. Ensure watermarks never obstruct content or interactions; on the web use a decorative layer with `pointer-events: none` and keep it out of the accessibility tree. Give meaningful foreground logos suitable alt text.
- Respect an established application structure. Introduce reusable brand tokens and logo/background components when they reduce duplication; avoid unrelated navigation or workflow changes just to apply branding.

## Verify and deliver

- Check representative output visually at the relevant screen/page sizes: logo visibility and proportions, purple dominance, faint watermark, Thai text wrapping, contrast, and content readability.
- For websites, confirm the image resolves through the application and the decorative background does not block controls. For documents/slides, confirm the logo is embedded and the watermark survives rendering/export.
- Report the branding changes and the checks actually performed. If visual rendering is unavailable, state that limitation instead of claiming a visual check.
