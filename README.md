# Hesab Sarraf — Public Web Release

This repository is the public deployment surface for Hesab Sarraf.

- The authoritative application source remains in the private repository: `roohalla372/q7v-n4x-k9p2-z8m61`.
- Only the built web output is intended to be published from this repository.
- Never commit private source archives, database exports, customer records, financial transactions, service-role keys, passwords, or other secrets here.

## Release pipeline

GitHub Actions in this public repository checks out this deployment repository, securely clones the selected branch from the private source repository using `PRIVATE_SOURCE_TOKEN`, runs `npm install` and `npm run build`, uploads only `private-source/dist`, and publishes that artifact to GitHub Pages. The deployment repository is therefore the publishing bridge; the private source repository remains authoritative.

The selected preview branch is `work/v22-device-layout-refinement-20261126`. The build uses the existing public Supabase project URL and publishable browser key. It does not run database migrations or modify database schema, user records, financial records, backend functions, or secrets.

## Current source revision

- Latest mobile navigation repair merged into the selected private source branch: `80b1f88d6e78c2bbfe9517ed2f4ca315cdb77f65`.
- The repair suppresses duplicate mobile navigation rows on the home dashboard; it preserves existing icon definitions, routes, handlers, and accounting behavior.


- Private source branch: `work/v22-device-layout-refinement-20261126`
- Source commit: `f5a02d7431bd19850bf50ece09bf1bd6bb3c0be4`
- Updates the existing 14-icon row to use the same 11-item toolbar definition as the reference. The existing navigation handlers are retained. The rendered layout still requires visual QA on all four device classes.

A successful source build alone is not proof of a successful Pages deployment. Verify the latest GitHub Actions run and the live site before treating this revision as published. The browser build is not a certification that login, AI runtime behavior, or live financial operations have been tested.
