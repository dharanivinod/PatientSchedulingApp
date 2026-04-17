# Navigation Map: Appointment Booking & Clinical Intelligence Platform

**Document Version:** 1.0  
**Created:** April 17, 2026  
**Status:** Draft  
**Related Artifacts:** `.propel/context/docs/figma_spec.md`, `.propel/context/wireframes/Lo-Fi/`

---

## 1. Overview

This navigation map outlines the user flows and screen connections for the Appointment Booking & Clinical Intelligence Platform. It provides traceability between screens (SCR-XXX) and validates UXR coverage for key user journeys.

### Navigation Principles
- Hierarchical navigation with breadcrumbs for admin/staff flows
- Tab-based navigation for patient appointment views
- Modal overlays for confirmations and secondary actions
- Progressive disclosure to reduce cognitive load

---

## 2. Patient Experience Flow

### Primary Booking Flow
SCR-001 (Patient Landing) → SCR-002 (Search & Availability) → SCR-003 (Booking Review) → SCR-004 (Confirmation)

### Appointment Management Flow
SCR-001 (Patient Landing) → SCR-005 (Calendar & History) → SCR-006 (Appointment Detail) → SCR-007 (Reschedule)

### Profile & Preferences Flow
SCR-001 (Patient Landing) → SCR-008 (Profile & Preferences) → SCR-009 (Notifications & Reminders)

---

## 3. Staff / Scheduler Experience Flow

### Daily Operations Flow
SCR-010 (Scheduler Dashboard) → SCR-012 (Triage & Booking) → SCR-013 (Appointment Detail Staff) → SCR-014 (Patient Lookup)

### Availability Management Flow
SCR-010 (Scheduler Dashboard) → SCR-011 (Provider Availability) → SCR-015 (Workload View)

### No-Show Handling Flow
SCR-010 (Scheduler Dashboard) → SCR-016 (No-Show Workflow) → SCR-014 (Patient Lookup)

---

## 4. Admin / Analytics Experience Flow

### Overview & Monitoring Flow
SCR-017 (Admin Home) → SCR-018 (Analytics Dashboard) → SCR-021 (Audit Logs)

### Configuration Flow
SCR-017 (Admin Home) → SCR-020 (System Configuration) → SCR-019 (Role Management)

### Intelligence Review Flow
SCR-017 (Admin Home) → SCR-022 (Clinical Insights) → SCR-018 (Analytics Dashboard)

---

## 5. Cross-Flow Connections

### Shared Screens
- SCR-013 (Appointment Detail Staff) ↔ SCR-006 (Appointment Detail Patient) [Different views of same data]
- SCR-014 (Patient Lookup) ↔ SCR-008 (Patient Profile) [Staff vs Patient access]

### Error & Edge Case Flows
- All booking screens → Error Modal (Slot Expired, Conflict Warning)
- SCR-007 (Reschedule) → Warning Modal (24-hour cutoff)
- SCR-012 (Triage) → Override Modal (High-risk patient confirmation)

---

## 6. UXR Coverage Validation

### Patient Journeys Covered
- ✅ New patient onboarding and booking
- ✅ Returning patient rescheduling and management
- ✅ Profile updates and communication preferences
- ✅ Appointment history and preparation

### Staff Journeys Covered
- ✅ Daily scheduling operations and triage
- ✅ Provider availability management
- ✅ Patient lookup and clinical context
- ✅ No-show intervention and follow-up

### Admin Journeys Covered
- ✅ System monitoring and KPI review
- ✅ Configuration and role management
- ✅ Audit compliance and reporting
- ✅ Clinical intelligence oversight

### Accessibility Coverage
- Keyboard navigation paths validated
- Screen reader friendly structure
- Mobile-responsive breakpoints covered
- Error state handling included

---

## 7. Navigation Patterns Used

### Global Navigation
- Top bar: Brand, search, notifications, profile (all user types)
- Sidebar: Section navigation (staff/admin only)
- Breadcrumbs: Contextual location (admin flows)

### Local Navigation
- Tabs: Appointment views (upcoming/past)
- Filters: Data refinement (analytics, search)
- Action menus: Contextual operations (appointment cards)

### Modal Navigation
- Confirmations: Booking, rescheduling, cancellations
- Details: Appointment info, patient profiles
- Settings: Preferences, configurations

---

## 8. Recommendations for Iteration

- Add quick-access shortcuts for power users in scheduler dashboard
- Implement progressive loading for large appointment lists
- Consider collapsible sections for complex admin forms
- Add search within navigation for large screen inventories

---

## 9. Screen Inventory Summary

| SCR-ID | Screen Name | User Type | Primary Flow |
|--------|-------------|-----------|--------------|
| SCR-001 | Patient Landing / Home | Patient | Entry |
| SCR-002 | Patient Search & Availability | Patient | Booking |
| SCR-003 | Appointment Booking Review | Patient | Booking |
| SCR-004 | Appointment Confirmation | Patient | Booking |
| SCR-005 | Appointment Calendar & History | Patient | Management |
| SCR-006 | Appointment Detail | Patient | Management |
| SCR-007 | Reschedule Appointment | Patient | Management |
| SCR-008 | Patient Profile & Preferences | Patient | Settings |
| SCR-009 | Notifications & Reminders | Patient | Settings |
| SCR-010 | Scheduler Dashboard | Staff | Operations |
| SCR-011 | Provider Availability Management | Staff | Configuration |
| SCR-012 | Appointment Triage & Booking | Staff | Operations |
| SCR-013 | Appointment Detail (Staff) | Staff | Operations |
| SCR-014 | Patient Lookup & Profile | Staff | Operations |
| SCR-015 | Workload / Operations View | Staff | Monitoring |
| SCR-016 | No-Show & Follow-up Workflow | Staff | Operations |
| SCR-017 | Admin Home / Overview | Admin | Monitoring |
| SCR-018 | Analytics Dashboard | Admin | Analytics |
| SCR-019 | Role & Access Management | Admin | Configuration |
| SCR-020 | System Configuration | Admin | Configuration |
| SCR-021 | Audit Logs & Compliance | Admin | Compliance |
| SCR-022 | Clinical Intelligence Insights | Admin | Analytics |
