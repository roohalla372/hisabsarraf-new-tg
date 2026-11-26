# Hesab Sarraf — Public Web Release

This repository is the public deployment surface for Hesab Sarraf.

- The authoritative application source remains in the private repository: `roohalla372/q7v-n4x-k9p2-z8m61`.
- Only the built web output is intended to be published from this repository.
- Never commit private source archives, database exports, customer records, financial transactions, service-role keys, passwords, or other secrets here.

## Release pipeline

GitHub Actions fetches the temporary preview source branch `work/v22-device-layout-refinement-20261126`, builds the static browser application, and deploys the generated output to GitHub Pages. The build uses the existing public Supabase project URL and publishable browser key. No database schema, user records, financial records, backend functions, or secrets are modified by this deployment.

## Current release

A deployment has been triggered for version 21 source commit `8b4dfd50a544c4a0a1bbbcf50d7744ebfd1fd90e`. This release includes the approved login-page updates and the pre-login AI help interface. The browser build is not a certification that login or AI runtime behavior has been tested, and the application is not being declared approved for live financial operations.
