# Product Requirements Document (PRD) - TODO App MVP Upgrade

## 1. Overview

We are upgrading the basic TODO app to support due dates, priorities, and task filters so users can better understand what is urgent and organize their work without adding backend complexity. The MVP keeps the app simple and teachable by storing tasks locally and limiting the upgrade to due dates, priority values, and basic date-based filters.

---

## 2. MVP Scope

- Add an optional `dueDate` field to tasks.
  - Use ISO `YYYY-MM-DD` format.
  - Invalid date values should be ignored and treated as absent.
- Add a `priority` field to tasks.
  - Supported values: `P1`, `P2`, `P3`.
  - Default value: `P3`.
- Add task filters:
  - `All`
  - `Today`
  - `Overdue`
- Keep task storage local.
  - No backend changes.
  - No external storage.
- Preserve required title validation.
  - `title` remains required.
  - `priority` must be one of `P1`, `P2`, or `P3`.
  - `dueDate` remains optional.

---

## 3. Post-MVP Scope

- Visually highlight overdue tasks.
  - Overdue tasks should stand out, with red highlighting suggested by the client.
- Add visual priority badges.
  - `P1`: red badge.
  - `P2`: orange badge.
  - `P3`: gray badge.
- Add advanced task sorting.
  - Overdue tasks first.
  - Then sort by priority: `P1`, `P2`, `P3`.
  - Then sort by due date ascending.
  - Tasks without a due date should appear last.

---

## 4. Out of Scope

- Notifications.
- Recurring tasks.
- Multi-user support.
- Special keyboard navigation requirements.
- Backend storage or external storage.