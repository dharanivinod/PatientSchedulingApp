# Design System: Appointment Booking & Clinical Intelligence Platform

**Document Version:** 1.0  
**Created:** April 17, 2026  
**Status:** Draft  
**Related Artifacts:** `.propel/context/docs/figma_spec.md`, `.propel/context/docs/spec.md`, `.propel/context/docs/design.md`

---

## 1. Design System Overview

This document defines the core design tokens, components, layout principles, and interaction patterns for the Appointment Booking & Clinical Intelligence Platform. It supports consistency across patient, staff, and admin interfaces and partners with the Figma spec for implementation.

### Design System Objectives
- Provide reusable UI building blocks for rapid product development.
- Ensure consistent visual language across patient and clinical user journeys.
- Support accessibility, responsiveness, and brand clarity.
- Enable a scalable token-driven design system for engineering handoff.

---

## 2. Design Tokens

### 2.1 Color Palette

#### Primary
- `Primary / Blue 700`: #1F4E8D
- `Primary / Blue 500`: #3B6FB7
- `Primary / Blue 300`: #7DA9E3
- `Primary / Blue 100`: #D7E4F7

#### Neutral
- `Neutral / Gray 900`: #101820
- `Neutral / Gray 800`: #242F3D
- `Neutral / Gray 700`: #3B4B60
- `Neutral / Gray 500`: #6E7D92
- `Neutral / Gray 300`: #CBD2DE
- `Neutral / Gray 100`: #F4F6FA
- `Neutral / White`: #FFFFFF

#### Success / Positive
- `Success / Green 600`: #1F7A4C
- `Success / Green 100`: #D8EFDE

#### Warning / Caution
- `Warning / Amber 600`: #C47A00
- `Warning / Amber 100`: #F7E8C8

#### Danger / Error
- `Danger / Red 600`: #B32A2A
- `Danger / Red 100`: #F7D6D6

#### Info
- `Info / Teal 600`: #0B7B8B
- `Info / Teal 100`: #D8F1F4

#### Status
- `Status / Confirmed`: #1F7A4C
- `Status / Pending`: #FFB500
- `Status / Rescheduled`: #5B68D8
- `Status / Cancelled`: #B32A2A
- `Status / No-Show`: #8B3D3D
- `Status / High-Risk`: #A34C8B

### 2.2 Typography

#### Font Families
- `Display / Headings`: Inter, 600
- `Body / UI`: Inter, 400
- `Mono`: Inter, 400 (or monospace for code-like labels)

#### Heading Scale
- `H1`: 40px / 48px line-height / 700
- `H2`: 32px / 40px line-height / 700
- `H3`: 24px / 32px line-height / 600
- `H4`: 20px / 28px line-height / 600
- `H5`: 16px / 24px line-height / 600

#### Body Text
- `Body Large`: 18px / 28px line-height / 400
- `Body Standard`: 16px / 24px line-height / 400
- `Body Small`: 14px / 20px line-height / 400
- `Label`: 12px / 16px line-height / 600

### 2.3 Spacing Scale
- `Space 4`: 4px
- `Space 8`: 8px
- `Space 12`: 12px
- `Space 16`: 16px
- `Space 20`: 20px
- `Space 24`: 24px
- `Space 32`: 32px
- `Space 40`: 40px
- `Space 48`: 48px
- `Space 64`: 64px

### 2.4 Elevation and Surfaces
- `Surface / Level 1`: #FFFFFF, shadow `0 1px 3px rgba(16, 24, 40, 0.08)`
- `Surface / Level 2`: #F4F6FA, shadow `0 4px 12px rgba(16, 24, 40, 0.12)`
- `Surface / Level 3`: #E9EEF6, shadow `0 8px 24px rgba(16, 24, 40, 0.16)`

### 2.5 Border Radius
- `Radius / Small`: 4px
- `Radius / Standard`: 8px
- `Radius / Large`: 16px

### 2.6 Iconography
- Use a system icon set with clear healthcare semantics.
- Primary icon stroke weight: 1.5px.
- Sizes: 16px, 20px, 24px, 32px.
- Use icons for contextual actions only; labels are mandatory for critical controls.

---

## 3. Component Library

### 3.1 Buttons
- `Button / Primary`: solid primary blue, white text.
- `Button / Secondary`: white background, primary border, primary text.
- `Button / Tertiary`: text-only with neutral gray.
- `Button / Danger`: solid red, white text.
- `Button / Ghost`: transparent background, neutral text.
- `Button / Icon`: square with minimal padding for toolbar actions.

### 3.2 Form Controls
- `Input / Standard`: full-width, 16px border radius, neutral border.
- `Input / Focused`: border `Primary / Blue 500`, subtle shadow.
- `Input / Error`: border `Danger / Red 600`, error text below.
- `Select / Dropdown`: consistent with inputs, with chevron icon.
- `Checkbox / Radio`: accessible labels, 20px tap target.
- `Textarea`: multiline support with resize disabled in UI.

### 3.3 Status Chips
- Confirmed: `Success / Green 600` background, white text.
- Pending: `Warning / Amber 600` background, white text.
- Rescheduled: `Primary / Blue 500` background, white text.
- Cancelled: `Danger / Red 600` background, white text.
- No-Show: `Danger / Red 100` background with red text.
- High-Risk: `Status / High-Risk` background with white text.

### 3.4 Cards
- `Card / Default`: white surface, 1px neutral border, 16px radius, 16px padding.
- `Card / Large`: 24px padding.
- `Card / Feature`: more prominent surface with title, value, and action.
- `Card / Metric`: used in dashboards with icon, value, trend line.

### 3.5 Data Table
- Header row with neutral background and bold text.
- Row hover highlight and selectable row state.
- Embedded action menu on row end.
- Responsive shrink-to-stack behavior on tablet/mobile.

### 3.6 Alerts
- Success alert: `Success / Green 100` background, green text.
- Warning alert: `Warning / Amber 100` background, amber text.
- Error alert: `Danger / Red 100` background, red text.
- Info alert: `Info / Teal 100` background, teal text.

### 3.7 Navigation
- `Top Bar`: brand, global search, notifications, user profile.
- `Sidebar`: nav items, section headings, active state highlight.
- `Breadcrumb`: location context for staff/admin flows.

### 3.8 Chart & Analytics Patterns
- Line chart: appointment volume over time.
- Bar chart: provider utilization by location.
- Donut chart: patient segmentation and no-show distribution.
- KPI strip: metric name, value, change percentage, and trend arrow.

---

## 4. Layout & Responsive Rules

### 4.1 Layout Grid
- Desktop: 12-column grid with 24px gutters.
- Tablet: 8-column grid with 20px gutters.
- Mobile: 4-column grid with 16px gutters.

### 4.2 Breakpoints
- `Mobile`: 0–767px
- `Tablet`: 768–1023px
- `Desktop`: 1024px+
- `Wide Desktop`: 1440px+

### 4.3 Container Widths
- Desktop content width: 1160px max.
- Wide content width: 1400px max for analytic dashboards.

### 4.4 Spacing
- Use token-based spacing consistently.
- `Section gap`: 48px.
- `Subsection gap`: 32px.
- `Form row gap`: 24px.
- `Stack gap`: 16px.

### 4.5 Responsive Behavior
- Sidebar collapses to icon-only navigation on tablet.
- Dashboard cards stack vertically on mobile.
- Forms convert from multi-column to single-column.
- Calendar and schedule grids remain scrollable horizontally if needed.

---

## 5. Interaction Patterns

### 5.1 Primary Interaction Rules
- Primary actions are clearly distinct and placed at the bottom-right of modals/forms.
- Secondary actions appear as outline or ghost styles.
- Destructive actions require explicit confirmation.
- Provide undo options for appointment cancellations and reschedules where possible.

### 5.2 Feedback & Validation
- Inline validation appears after field blur and on submit.
- Use toast notifications for success messages and non-blocking confirmations.
- Use modal dialogs for scheduling conflicts and high-risk override warnings.
- Provide progress indicators for multi-step operations.

### 5.3 Accessibility
- Include focus ring for all keyboard-navigable elements.
- Ensure at least 4.5:1 contrast ratio for body text and 3:1 for large text.
- Provide explicit labels and ARIA roles for complex controls.
- Avoid using color alone for status or severity.

### 5.4 Motion and Transition
- Use subtle motion for modal opening, dropdown transitions, and hover states.
- Keep animation duration under 200ms for interface feedback.
- Avoid motion for critical alerts to maintain readability and accessibility.

---

## 6. Content Guidelines

### 6.1 Tone and Voice
- Clear, direct, and action-oriented.
- Avoid clinical jargon in patient-facing screens; use simple language.
- Use professional, precise terminology in staff/admin screens.
- Prefer active voice for instructions and confirmations.

### 6.2 Labels and Microcopy
- Buttons: `Confirm booking`, `Reschedule appointment`, `Send reminder`, `View details`, `Edit settings`.
- Alerts: `Appointment confirmed`, `Slot no longer available`, `Changes saved successfully`.
- Status chips: use single-word, human-readable labels.

### 6.3 Error Messaging
- Provide a clear explanation, recovery action, and next step.
- Example: `Unable to save provider availability. Please refresh and try again.`

---

## 7. Component Naming & Token Mapping

### 7.1 Component Naming
- `Button / Primary / Default`
- `Input / Text / Default`
- `Card / Appointment Summary`
- `Table / Data / Default`
- `Chip / Status / Confirmed`
- `Alert / Inline / Warning`

### 7.2 Token Mapping for Engineering
- `--color-primary-500`: #3B6FB7
- `--color-surface-1`: #FFFFFF
- `--font-size-16`: 16px
- `--radius-standard`: 8px
- `--spacing-16`: 16px

---

## 8. Recommended Delivery

- Publish the Figma file with shared team library access.
- Create a `Design System` library page and expose tokens/components.
- Include sample user flows for booking, rescheduling, and admin reporting.
- Link screen specifications to corresponding requirements in `spec.md` and `design.md`.
- Add annotation layers for component states and responsive variants.

---

## 9. Notes for Future Iteration

- Extend the design system to support patient mobile native app patterns.
- Add language locale variants and RTL layout guidance.
- Include a dedicated `Accessibility` page with audit checklist and keyboard flow diagrams.
- Add `Illustration / Icon` guidelines for brand and healthcare-specific visuals.
