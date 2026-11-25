# Hesab Sarraf — Public Web Release

This repository is the public deployment surface for Hesab Sarraf.

- The authoritative application source remains in the private repository: `roohalla372/q7v-n4x-k9p2-z8m61`.
- Only the built web output is intended to be published from this repository.
- Never commit private source archives, database exports, customer records, financial transactions, service-role keys, passwords, or other secrets here.
- The public browser bundle is inspectable by visitors. Only publish code and configuration intended for public clients.

## Release pipeline

GitHub Actions is being prepared to fetch the approved release branch from the private source repository, build it, and deploy the generated static site to GitHub Pages.

Required repository Actions secrets:
- `PRIVATE_SOURCE_TOKEN`: a fine-grained token limited to read-only access to the private source repository.
- `VITE_SUPABASE_URL`: public Supabase project URL, only if the release is approved to connect.
- `VITE_SUPABASE_ANON_KEY`: public anon/publishable key, only after database policies and authentication have been security-reviewed. Never use a service-role key.

The workflow intentionally blocks deployment while the source still identifies itself as a preview. This prevents accidentally presenting a non-operational build as the live financial application.

## Current status

Release build requested from private source branch `delivery/v21-independent` at commit `8b4dfd50a544c4a0a1bbbcf50d7744ebfd1fd90e`. GitHub Actions will build the static browser output and publish it to GitHub Pages. This release is for login-page verification; the application has not yet been approved for live financial operations.
