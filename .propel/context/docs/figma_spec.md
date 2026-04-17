# Figma Specification: Appointment Booking & Clinical Intelligence Platform

**Document Version:** 1.0  
**Created:** April 17, 2026  
**Status:** Draft  
**Related Artifacts:** `.propel/context/docs/spec.md`, `.propel/context/docs/design.md`

---

## 1. Purpose

This document defines the Figma design specification for the Appointment Booking & Clinical Intelligence Platform. It translates product requirements, user roles, and architecture into a screen inventory, interaction flows, component library, and visual design rules.

### Goals
- Capture the core patient, staff, and admin experiences in a consistent Figma file structure.
- Define screen states, component behavior, and transitions for booking, scheduling, reminders, and analytics.
- Enable rapid handoff to UI engineering and visual design teams.
- Ensure accessibility, responsive layout, and product-level design consistency.

---

## 2. Figma File Structure

### Pages
- `00 Cover + Guidelines`
- `01 UI Kit`
- `02 Patient Experience`
- `03 Staff / Scheduler Experience`
- `04 Admin / Analytics Experience`
- `05 Prototype Flows`
- `06 Assets`

### Sections within pages
- `UI Kit` page: Color tokens, typography, spacing, iconography, buttons, form controls, cards, tables, alerts, badges, chips.
- `Patient Experience`: onboarding, search, booking, appointment detail, reminders, profile, history.
- `Staff / Scheduler Experience`: calendar view, provider availability, appointment triage, appointment details, manual booking, workload dashboard.
- `Admin / Analytics Experience`: KPI dashboard, analytics panels, settings, role management, audit logs.
- `Prototype Flows`: appointment booking flow, reschedule flow, reminder flow, no-show workflow, admin report flow.

---

## 3. Screen Inventory

### 3.1 Patient Experience Screens

1. `Patient Landing / Home`
   - Key sections: quick search, upcoming appointment card, action tile to book new appointment, alerts for reminders or survey requests.
   - States: authenticated patient, guest preview.

2. `Patient Search & Availability`
   - Filters: specialty, provider, location, date range, time preference, urgency.
   - List view with provider card, available slots, distance, patient rating, appointment type.
   - Empty state and no-availability state.

3. `Appointment Booking Review`
   - Selected provider and time slot summary, appointment reason, insurance preview, check-in instructions.
   - Confirm/cancel actions and live slot hold indicator.
   - Error state for slot expiry or scheduling conflict.

4. `Appointment Confirmation`
   - Confirmation details, update/cancel buttons, reminder schedule, calendar add action.
   - Communication preferences summary and next steps.

5. `Appointment Calendar & History`
   - Tabbed view: upcoming appointments, past appointments.
   - List and calendar toggle.
   - Appointment card with status pill, provider, location, notes, reschedule/cancel actions.

6. `Appointment Detail`
   - Full appointment details, clinical context, preparation notes, location map, directions, contact options.
   - Status variants: confirmed, rescheduled, cancelled, no-show flagged.

7. `Reschedule Appointment`
   - Alternative slots search, selected slot preview, reschedule confirmation, conflict warning.
   - States for within 24-hour reschedule cutoff and outside cutoff.

8. `Patient Profile & Preferences`
   - Personal details, communication settings, language, accessibility preferences, consent controls.
   - Editable form and save/cancel actions.

9. `Notifications & Reminders`
   - Reminder preference management, active reminder timeline, ability to confirm attendance or reschedule.
   - SMS / email preference toggles and message preview.

### 3.2 Staff / Scheduler Experience

10. `Scheduler Dashboard`
    - Calendar view with provider lanes, day/week toggles, availability overlays, urgent slot indicators.
    - Appointment queue panel for pending requests.
    - Workload summary cards: booked slots, open slots, no-show alerts.

11. `Provider Availability Management`
    - Recurring schedule builder, exception management, location assignment.
    - Slot-type configuration for appointment durations and buffer rules.
    - Conflict indicator and save state.

12. `Appointment Triage & Booking`
    - Form-driven triage panel with chief complaint, appointment type, urgency.
    - Recommended providers and times based on patient profile and risk score.
    - Manual booking override controls.

13. `Appointment Detail (Staff)`
    - Appointment metadata, patient clinical context, risk score, no-show probability, notes.
    - Action buttons: confirm, reschedule, cancel, mark no-show, flag for review.

14. `Patient Lookup & Profile`
    - Search bar with patient matching, demographics, appointment history.
    - Quick access to outstanding balance, high-risk indicators, and communication preferences.

15. `Workload / Operations View`
    - Heatmap of provider utilization, provider workload summary, overbooked/underutilized indicators.
    - Filters for location, provider, date range.

16. `No-Show & Follow-up Workflow`
    - No-show event screen with automatic communication actions, reschedule offer, and status update.
    - History of no-show interventions for patient.

### 3.3 Admin / Analytics Experience

17. `Admin Home / Overview`
    - KPI cards for appointment volume, no-show rate, utilization, patient satisfaction.
    - Alerts for threshold breaches and compliance exceptions.

18. `Analytics Dashboard`
    - Trend charts: appointment volume, no-show rate, capacity utilization, recommendation impact.
    - Filters for date range, location, provider, appointment type.
    - Export actions and scheduled report setup.

19. `Role & Access Management`
    - Role list, permission matrix, user search.
    - Create/edit role workflows and staff account status.

20. `System Configuration`
    - Appointment types and rules, notification templates, triage rule builder, location management.
    - Integration settings for EHR, SMS/email providers, calendar sync.

21. `Audit Logs & Compliance`
    - Filterable audit record table, detail pane with access metadata.
    - Export controls and compliance report link.

22. `Clinical Intelligence Insights`
    - Model confidence summary, high-risk patient pipeline, recommendation performance.
    - Ability to inspect sample predictive factors and override behavior.

---

## 4. Interaction Flows

### 4.1 Patient Appointment Booking Flow
1. Patient arrives on Home.
2. Patient searches for provider availability.
3. Patient selects a provider and available time slot.
4. Booking Review screen displays appointment details.
5. Patient confirms booking.
6. Confirmation screen appears and reminder schedule is shown.
7. Appointment appears in Patient Calendar.

### 4.2 Patient Reschedule Flow
1. Patient selects an upcoming appointment.
2. Patient taps `Reschedule`.
3. Available slots screen appears with recommendations.
4. Patient selects new slot and confirms.
5. Confirmation screen updates to show the new appointment.

### 4.3 Scheduler Appointment Triage Flow
1. Scheduler opens appointment request queue.
2. Scheduler selects request and views triage guidance.
3. System recommends provider/time slots.
4. Scheduler confirms appointment or overrides settings.
5. Appointment is booked and patient receives confirmation.

### 4.4 Admin Analytics Review Flow
1. Admin opens Analytics Dashboard.
2. Admin filters by period and location.
3. Admin reviews KPI cards and trend charts.
4. Admin exports a report or schedules recurring delivery.

### 4.5 No-Show Intervention Flow
1. Appointment is marked `No-Show`.
2. System sends follow-up communication and reschedule offer.
3. Staff reviews no-show details and optionally updates patient status.
4. Analytics dashboard reflects no-show event and trend.

---

## 5. Component Inventory

### 5.1 Navigation
- Global header with brand, search, notifications, profile menu
- Sidebar / tertiary navigation for Staff and Admin experiences
- Tabbed navigation for appointment views and analytics filtering

### 5.2 Card Patterns
- Appointment summary cards
- Provider card with availability state
- KPI card with metric, comparison badge, status indicator
- Alert card for reminders and compliance events

### 5.3 Data Tables & Lists
- Appointment list rows with status chips, provider/location, action buttons
- Audit log table with filter bar
- User/role management table with badge status and action menu

### 5.4 Forms & Inputs
- Search input with auto-suggest and filters
- Date/time picker with slot availability
- Select dropdowns for specialty, location, patient status
- Radio groups for reminder preferences, communication channels
- Toggle switches for enabled/disabled settings

### 5.5 Buttons
- Primary action
- Secondary action
- Tertiary text button
- Destructive action (cancel, delete)
- Chip button for quick filters

### 5.6 Status & Feedback
- Success, warning, error, info alert banners
- Toast notifications for saves, bookings, errors
- Progress indicator for multi-step booking and triage flows
- Empty states with guidance and action buttons

### 5.7 Visual Tokens
- Status chips: Confirmed, Pending, Rescheduled, Cancelled, No-Show, High-Risk
- Severity badges: Critical, Warning, Info, Success

---

## 6. Screen-State Requirements

### Appointment Booking States
- `Ready to confirm` — selected slot available, all required fields complete.
- `Slot expired` — user informed and asked to refresh availability.
- `Conflict warning` — booking prevented if patient has schedule conflict.
- `High-risk patient` — risk badge and double-reminder message.

### Provider Availability States
- `Available`
- `Booked`
- `Blocked`
- `Holiday / exception`
- `Recommended`

### Analytics States
- `Healthy` — KPI within target range.
- `Warning` — KPI near threshold.
- `Alert` — KPI exceeded threshold with recommended actions.
- `Data unavailable` — no data for selected period or filtered criteria.

---

## 7. Design Token and Accessibility Guidelines

### 7.1 Responsiveness
- Desktop: 1200px+ viewport with multi-column layout.
- Tablet: 768px–1199px with adaptive cards and stacked navigation.
- Mobile: 320px–767px with single-column vertical flow and condensed controls.

### 7.2 Accessibility
- WCAG 2.1 AA contrast ratios for all text and UI elements.
- Keyboard-focus styles for all interactive controls.
- Screen-reader labels and semantic structure for form fields.
- Color not used as sole indicator; status chips accompanied by text.
- Touch target minimum 44x44 pt.

### 7.3 Visual Hierarchy
- Primary actions use stronger contrast and solid fill.
- Secondary and tertiary actions use outlined or ghost styles.
- Card headings and section titles follow consistent spacing and typography.
- Status and alert messaging placed near related actions.

---

## 8. Prototype and Handoff Notes

### Prototype behavior
- Clickable flow from Home → Search → Booking → Confirmation.
- Interactive provider availability calendar and slot selection.
- Triage recommendations in scheduler flow.
- Admin KPI filters and export interactions.

### Handoff guidance
- Export Figma components as named assets.
- Annotate states for all booking, reschedule, and reminder scenarios.
- Include measurement guides for spacing, typography, and responsive breakpoints.
- Provide token mapping for CSS variables and design system integration.

---

## 9. Recommended Figma Deliverables

- `Design System` page with tokens, icons, components, and patterns.
- `Patient Experience` page with complete booking and history flows.
- `Staff Experience` page with scheduler and appointment operations.
- `Admin Experience` page with analytics, settings, and audit workflows.
- `Prototype Flows` page for primary user journeys.
- `Assets` page with icons, illustrations, and export-ready UI elements.
