# Hesab Sarraf — Public Web Release

This repository is only the public deployment surface for Hesab Sarraf.

- Authoritative source remains private: `roohalla372/q7v-n4x-k9p2-z8m61`.
- Only the production build output from `private-source/dist` is published here.
- Do not commit private source archives, database exports, customer records, transactions, balances, service-role keys, passwords, or secrets.

## Release pipeline

GitHub Actions securely clones the approved private source branch using `PRIVATE_SOURCE_TOKEN`, builds the Vite application with the existing public Supabase URL and publishable browser key, and deploys only `private-source/dist` to GitHub Pages.

The deployment does not run database migrations or modify Supabase schema, user accounts, customer records, transactions, balances, financial history, backend functions, or authentication.

## Current release source

- Private repository: `roohalla372/q7v-n4x-k9p2-z8m61`
- Branch: `work/v22-device-layout-refinement-20261126`
- Source commit: `ca0e6caff48adf7ff15d419ed5a0bca8fd6b0a21`
- Public site: https://hisabsarraf.new.tg/

## Responsive layout work

- Hardware-aware device classification separates phone, tablet, laptop, and monitor.
- Normal landscape phones retain the mobile interface; phone browsers explicitly requesting desktop-site mode use the laptop composition.
- Laptop and monitor layouts remain desktop layouts when the browser window is narrowed. Their icon rows and tables scroll internally rather than shrinking into mobile controls.
- Phone, tablet, laptop, and monitor have separate final layout styles.
- The 11-item desktop icon row uses readable icon and label sizes.
- The Sarraf workspace contains 24 numbered pages, seven numbered main menus, and 32 mobile submenu entries (31 in the laptop menu because print remains in the action bar).
- The compact laptop accounting workspace styles from the private work branch are preserved; the flex-column table layout is corrected so the accounting table receives the remaining workspace height.

## Automated QA

- Device classifier tests: 11/11 passed.
- Lint and production build: passed.
- Chromium responsive UI tests: 14/14 passed.
- All 24 modules were opened with synthetic data in phone, tablet, laptop, and monitor profiles.
- Laptop and monitor were tested at 14 viewport widths from 320px to 1920px; phone portrait/landscape and tablet width ranges were also checked.
- All seven desktop menus and seven mobile menus were opened; submenu counts and ten schema-backed forms were checked.

These tests use simulated hardware profiles and synthetic records. Physical-device checks for actual Android/iOS desktop-site mode, browser zoom, rotation, and real laptop/tablet/monitor displays remain necessary. A successful deployment does not certify login, AI runtime behavior, or live financial operations.

## Data safety

No real customer, user, transaction, balance, or financial-history records were changed as part of this responsive-layout release.
