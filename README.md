# Hesab Sarraf — Public Web Release

This repository is the public deployment surface for Hesab Sarraf.

- The authoritative application source remains in the private repository: `roohalla372/q7v-n4x-k9p2-z8m61`.
- Only the built web output is intended to be published from this repository.
- Never commit private source archives, database exports, customer records, financial transactions, service-role keys, passwords, or other secrets here.

## Release pipeline

GitHub Actions in this public repository checks out this deployment repository, securely clones the selected branch from the private source repository using `PRIVATE_SOURCE_TOKEN`, runs `npm install` and `npm run build`, uploads only `private-source/dist`, and publishes that artifact to GitHub Pages. The deployment repository is therefore the publishing bridge; the private source repository remains authoritative.

The selected preview branch is `work/v22-device-layout-refinement-20261126`. The build uses the existing public Supabase project URL and publishable browser key. It does not run database migrations or modify database schema, user records, financial records, backend functions, or secrets.

## Current source revision

- Latest mobile navigation repair: `80b1f88d6e78c2bbfe9517ed2f4ca315cdb77f65`.
- Desktop-site mode correction: phone browsers that expose a wide desktop viewport while retaining a narrow physical screen are now classified into the laptop composition. Laptop-specific dashboard sizing and the 11-item desktop toolbar are also enabled at compact desktop viewport widths; tablet classification remains separate.
- The change is limited to device-layout detection and CSS presentation. It does not alter icon definitions, navigation handlers, routes, accounting logic, authentication, or Supabase data.


- Private source branch: `work/v22-device-layout-refinement-20261126`
- Source commit: `f5a02d7431bd19850bf50ece09bf1bd6bb3c0be4`
- Updates the existing 14-icon row to use the same 11-item toolbar definition as the reference. The existing navigation handlers are retained. The rendered layout still requires visual QA on all four device classes.

A successful source build alone is not proof of a successful Pages deployment. Verify the latest GitHub Actions run and the live site before treating this revision as published. The browser build is not a certification that login, AI runtime behavior, or live financial operations have been tested.



- Follow-up device classifier commit: `00c47c6b6d03a21a0adcb531d3164d705406358d`. It distinguishes physical phone hardware from the browser's requested desktop viewport using touch capability and the shortest physical screen side, so resizing a laptop browser does not turn it into a phone layout.
- Device-layout correction source commit: `c3087712ffb759313526283a98b000b4458851e3` (CSS); JSX device-detection commit: `3e9cba873a9fd393c1acd2dbfa8de1243a444fca`.
- The resulting live page must still be verified in Android/iOS desktop-site mode and on a physical laptop before the layout is considered accepted.


## Laptop layout and navigation numbering — 2026-11-26

- Private source revision: `88fc3f4937a8468d6f0e37147f024620b0c5ecd3`.
- The Sarraf workspace now displays stable page numbers 01–24 across the dashboard, page headings, desktop toolbar and mobile feature list.
- The seven main menus are numbered 01–07. Their submenu entries use stable hierarchical identifiers such as 02.03; the same submenu identifier is retained on desktop and mobile, even when an item is intentionally omitted from one menu.
- Laptop toolbar icons are larger, labels have an 11px minimum, and the 11-item row scrolls horizontally instead of shrinking the icons when the browser viewport is narrow.
- Narrow laptop windows retain the laptop composition and reflow dashboard panels; they do not switch to the phone navigation solely because the viewport is narrow.
- Source build passed. Physical laptop, tablet, phone and browser desktop-site visual QA is still required before calling the layout fully verified.
- No database migration, Supabase data modification, customer/transaction/balance change, or accounting logic change was made.
