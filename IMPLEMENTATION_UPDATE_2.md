# Website Implementation Plan

## Purpose

This document is the single source of truth for completing and maintaining the HVAC landing website. Implement only items listed as open. Do not rework completed items unless a regression is found.

## Current Status

### Completed

- Services section uses a static responsive grid instead of the former marquee.
- Navigation was simplified to the logo, About, Reviews, and Shop Systems CTA.
- Navigation is responsive with a mobile menu below the `sm` breakpoint.
- Text alignment was audited; body copy is not justified.
- `/reviews` page was created with a responsive review grid and load-more control.
- `/about` page was created with hero, mission/story, stats, partner brands, certifications, and CTA sections.
- Homepage testimonials include a centered `See all reviews →` link below the carousel controls, routing to `/reviews`.
- The six uploaded partner images in `/public/images/partners/` are used in the Brands We Work With section: Voltas, LG, Whirlpool, Blue Star, Amazon, and Fujitsu.
- The Shop Systems CTA repeatedly scrolls to the pricing section on the homepage and routes to `/#pricing` from other pages.
- Responsive behavior was checked at mobile and desktop widths. Homepage, About, Reviews, pricing, configurator, testimonials, and navigation render without user-facing horizontal scrolling.

## Open Implementation Work

No implementation tasks are currently open.

If a regression or new requirement is discovered, add it here with:

- **Location:** route or component
- **Problem:** current behavior
- **Expected behavior:** desired result
- **Constraints:** behavior or UI that must remain unchanged
- **Validation:** how completion will be verified

## Non-Negotiable Constraints

- Preserve the existing visual language, components, carousel behavior, stat row, and testimonial card design unless a task explicitly requests otherwise.
- Reuse existing components and design tokens before creating new variants.
- Keep layouts mobile-first and accessible. Use semantic HTML, meaningful link/button labels, keyboard support, and visible focus states.
- Keep touch targets at least 44px on mobile.
- Avoid horizontal page scrolling at mobile, tablet, and desktop widths.
- Use `next/image` for local image assets with useful alt text.
- Do not use localStorage for application data persistence.
- Keep route navigation functional from both the homepage and secondary pages.

## Future Facilitation Workflow

1. Read this file and inspect the relevant route/component before editing.
2. Confirm whether the requested work is already completed. If it is, validate it instead of duplicating it.
3. Implement the smallest complete change using existing patterns.
4. Validate the affected route and interaction in the browser at relevant responsive widths.
5. Update the matching status entry in this file immediately:
   - Mark completed work with `✅ COMPLETED`.
   - Remove obsolete or contradictory instructions.
   - Add any follow-up issue under **Open Implementation Work**.
6. Summarize the files changed and validation performed.

## Validation Checklist

For every future change, check only the items relevant to the change:

- [ ] Affected route loads without runtime or compile errors.
- [ ] Desktop layout remains intact.
- [ ] Mobile layout remains usable at approximately 375px wide.
- [ ] Tablet layout remains usable when the change affects responsive behavior.
- [ ] No unintended horizontal page scrolling.
- [ ] Links and buttons navigate or activate on repeated use.
- [ ] Existing carousel, stats, cards, and other protected behavior remains unchanged.
- [ ] Images have appropriate alt text and do not stretch or overflow.
- [ ] Relevant plan item is marked complete after validation.

## Reference Routes

- `/` — Homepage
- `/about` — Company story, trust, partners, certifications, and CTA
- `/reviews` — Full reviews grid
- `/services/[slug]` — Service detail pages

## Reference Components

- `components/layout/navbar.tsx` — responsive navigation and Shop Systems CTA
- `components/features/brands-banner.tsx` — shared partner logo row
- `components/testimonials/testimonials-section.tsx` — homepage reviews section and Reviews CTA
- `components/about/about-hero.tsx` — About hero
- `components/about/about-mission.tsx` — About mission/story content
- `app/about/page.tsx` — About page composition
- `app/reviews/page.tsx` — Reviews page

## Change Log

### Completed in the current implementation pass

- Added `/about` and its mission/story section.
- Added the homepage `See all reviews →` CTA.
- Replaced inline partner logos with the six uploaded local images.
- Fixed repeated Shop Systems navigation.
- Added responsive mobile navigation.
- Verified the primary routes and responsive layouts in the browser.

No legacy checklist or implementation-order section remains because those instructions described work that is already complete and could contradict this simplified plan.

## Plan Maintenance Rules

- Keep this file concise and actionable.
- Do not re-add completed step-by-step implementation instructions.
- Do not preserve duplicate checklists for the same feature.
- When requirements change, update the status and constraints rather than appending a conflicting version.
- Remove a completed item from **Open Implementation Work** after documenting it under **Completed**.
- If an older instruction conflicts with a newer validated implementation, the newer implementation and this file's **Current Status** take precedence.

_Last updated after consolidating the completed implementation work._
