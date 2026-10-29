# Recruiting v2 — Visual QA and design-system audit

Status: source-code review complete; live screenshots NOT captured. No deployment or production edits.

## Brand foundations
- Primary: navy `#0F1C2E` — headings, dark backgrounds, dark CTAs.
- Secondary: gold `#F5A623` — primary actions and highlights.
- Accent: dark gold `#B77513` — small labels on light backgrounds.
- Surface: white `#FFFFFF`; alternate surface: cream `#FAF8F3`.
- Text: `#17212F`; muted: `#647083`; border: `#E3E7EC`.
- Typography: **Inter** as primary UI and body font; headings bold with compact line height. Avoid introducing decorative fonts without a reviewed reason.
- Spacing: Tailwind 4px baseline. Use 4, 8, 12, 16, 20, 24, 32, 40, 48, 64, 80 and 96px increments. Tokens live in `v2/shared.css`.
- This is presently **plain CSS aligned to Tailwind tokens**, not an installed Tailwind build. The HTML contains additional inline page-specific CSS still needing migration.

## Priority changes from source audit
1. **Brand fidelity:** real logo references `../images/logo.png`; check its rendered size/contrast on desktop and mobile.
2. **Trust and social proof:** keep all four authentic testimonials and attribution; original photo references in old HTML point to files missing from repository. Do not substitute stock headshots.
3. **Client organisations:** currently display only companies substantiated by testimonials (Gratia, ThirdWay Partners, Windle). Do not claim this is a complete client roster or imply all are direct hiring clients without verification.
4. **Spacing:** remove arbitrary section/card gaps and map to shared spacing scale; page-specific CSS still contains some non-scale values.
5. **Typography:** replace page-specific arbitrary font sizes with Tailwind-compatible type steps, preserving readable body copy and responsive hierarchy.
6. **Mobile navigation:** current implementation hides text links below 900px. Add an accessible mobile menu or compact visible navigation before launch.
7. **Forms:** enquiry form currently launches mailto and does not submit to a backend. Test this on mobile and desktop; configure an approved backend before claiming a submitted enquiry.
8. **Footer:** replace GitHub source link labelled Career services with the actual public Career Services site once verified.
9. **Accessibility:** verify contrast, heading order, keyboard navigation, focus indicators, field labels and reduced-motion behavior.
10. **Screenshots:** capture 1440px desktop and 390px mobile, including hero, client organisations, testimonial cards and enquiry form. Check for overflow, image loading and spacing inconsistencies.

## Release gate
Do not tick screenshot QA or deployment approval until real browser screenshots have been captured and inspected. Preserve the live site until explicit approval.
