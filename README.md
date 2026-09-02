# VOC Delivery & Pickup - Modular HTML Demo

This version separates the original single `index.html` into smaller files so each feature is easier to edit.

## File structure

- `index.html` - page layout / HTML only
- `css/styles.css` - all visual styles
- `js/state.js` - demo seed data and shared application state
- `js/helpers.js` - common utilities, storage, escaping, badges
- `js/assets.js` - add/edit/remove multiple devices and asset rendering
- `js/dashboard.js` - dashboard, supervisor queue, admin queue, statistics
- `js/auth.js` - role login, logout, tabs, navigation
- `js/request-form.js` - employee form, validation, draft, review, submit, receipt
- `js/workflow.js` - approvals, admin processing, request detail/history
- `js/app.js` - application startup only
- `original_index.html` - copy of the original single-file version for reference

## How to edit

For request fields or submission validation, edit `js/request-form.js` and the form markup in `index.html`.
For device behavior, edit `js/assets.js`.
For Supervisor/Admin workflow, edit `js/workflow.js` and `js/dashboard.js`.
For colors/fonts/layout, edit `css/styles.css`.
For role behavior, edit `js/auth.js`.

## Run

Open `index.html` in a browser. For more reliable local testing, use a simple local web server (for example VS Code Live Server).

## Important production note

This demo still uses browser `localStorage`. For a real shared VOC application, replace the persistence functions with your secure API / Azure SQL or Dataverse backend and replace role selection with Microsoft Entra ID authentication and server-side authorization.
