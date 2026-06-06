# Beranda

## Mission
Create implementation-ready, token-driven UI guidance for Beranda that is optimized for consistency, accessibility, and fast delivery across documentation site.

## Brand
- Product/brand: PAN
- URL: http://127.0.0.1:5500/
- Audience: perta website visitors, documentation site users, design system site users
- Product surface: partai website, documentation site, design system site

## Style Foundations
- Visual style: clean, functional, implementation-oriented
- Main font style: `font.family.primary=Roboto`, `font.family.stack=Roboto, system-ui, -apple-system, Segoe UI, Roboto, Helvetica Neue, Arial, Noto Sans, Liberation Sans, sans-serif, Apple Color Emoji, Segoe UI Emoji, Segoe UI Symbol, Noto Color Emoji`, `font.size.base=16px`, `font.weight.base=400`, `font.lineHeight.base=24px`
- Typography scale: `font.size.xs=13px`, `font.size.sm=14px`, `font.size.md=14.4px`, `font.size.lg=16px`, `font.size.xl=17.6px`, `font.size.2xl=20px`, `font.size.3xl=25.6px`, `font.size.4xl=51.2px`
- Color palette: `color.text.primary=#ffffff`, `color.text.secondary=color(srgb 1 1 1 / 0.7)`, `color.text.tertiary=#010608`, `color.text.inverse=#04415f`, `color.surface.base=#000000`, `color.surface.raised=#f1f5f7`, `color.surface.strong=#0154a2`
- Spacing scale: `space.1=5px`, `space.2=8px`, `space.3=10px`, `space.4=12px`, `space.5=14px`, `space.6=15px`, `space.7=16px`, `space.8=18px`
- Radius/shadow/motion tokens: `radius.xs=8px`, `radius.sm=15px`, `radius.md=50px` | `shadow.1=rgba(0, 0, 0, 0.06) 0px 10px 30px 0px`, `shadow.2=rgba(0, 0, 0, 0.1) 0px 4px 15px 0px`, `shadow.3=rgba(0, 0, 0, 0.05) 0px 8px 15px 0px`, `shadow.4=rgba(0, 0, 0, 0.1) 0px 15px 40px 0px` | `motion.duration.instant=300ms`, `motion.duration.fast=500ms`, `motion.duration.normal=600ms`

## Accessibility
- Target: WCAG 2.2 AA
- Keyboard-first interactions required.
- Focus-visible rules required.
- Contrast constraints required.

## Writing Tone
Concise, confident, implementation-focused.

## Rules: Do
- Use semantic tokens, not raw hex values, in component guidance.
- Every component must define states for default, hover, focus-visible, active, disabled, loading, and error.
- Component behavior should specify responsive and edge-case handling.
- Interactive components must document keyboard, pointer, and touch behavior.
- Accessibility acceptance criteria must be testable in implementation.

## Rules: Don't
- Do not allow low-contrast text or hidden focus indicators.
- Do not introduce one-off spacing or typography exceptions.
- Do not use ambiguous labels or non-descriptive actions.
- Do not ship component guidance without explicit state rules.

## Guideline Authoring Workflow
1. Restate design intent in one sentence.
2. Define foundations and semantic tokens.
3. Define component anatomy, variants, interactions, and state behavior.
4. Add accessibility acceptance criteria with pass/fail checks.
5. Add anti-patterns, migration notes, and edge-case handling.
6. End with a QA checklist.

## Required Output Structure
- Context and goals.
- Design tokens and foundations.
- Component-level rules (anatomy, variants, states, responsive behavior).
- Accessibility requirements and testable acceptance criteria.
- Content and tone standards with examples.
- Anti-patterns and prohibited implementations.
- QA checklist.

## Component Rule Expectations
- Include keyboard, pointer, and touch behavior.
- Include spacing and typography token requirements.
- Include long-content, overflow, and empty-state handling.
- Include known page component density: links (44), lists (8), cards (4), navigation (2), buttons (1).

- Extraction diagnostics: Audience and product surface inference confidence is low; verify generated brand context.

## Quality Gates
- Every non-negotiable rule must use "must".
- Every recommendation should use "should".
- Every accessibility rule must be testable in implementation.
- Teams should prefer system consistency over local visual exceptions.
