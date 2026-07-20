---
name: shopee-listing
description: Automate Shopee seller-center login, product listing, and delisting with Chrome/Playwright. Use when Codex needs to run or maintain a Shopee automation project, open the seller backend for a manual login step, or execute listing/unlisting workflows from prepared product data.
---

# Shopee Listing

## Overview

Use this skill to operate the local Shopee automation project in E:\电商\自动化\shopee.
Keep the workflow short and explicit: log in with Chrome, load product data, then run listing or delisting commands.

## Workflow

1. Open the project at E:\电商\自动化\shopee.
2. Run npm.cmd run login to launch Chrome and save a seller-session profile.
3. After manual login, reuse the saved profile for npm.cmd run list or npm.cmd run unlist.
4. Keep product records in data/products.example.json or a file pointed to by SHOPEE_PRODUCTS_FILE.
5. Update src/shopee.js when the seller-center UI changes or when a different shop/site needs new selectors.

## Execution Rules

- Prefer the existing scripts in the workspace instead of inventing a new flow.
- Do not assume the seller is already logged in; verify with the login script first.
- Treat selector changes as normal maintenance and patch src/shopee.js rather than scattering page logic elsewhere.
- Keep listing data in structured JSON; do not hard-code product details into the automation.

## Relevant Files

- [README.md](file:///E:/电商/自动化/shopee/README.md)
- [src/login.js](file:///E:/电商/自动化/shopee/src/login.js)
- [src/list.js](file:///E:/电商/自动化/shopee/src/list.js)
- [src/unlist.js](file:///E:/电商/自动化/shopee/src/unlist.js)
- [src/shopee.js](file:///E:/电商/自动化/shopee/src/shopee.js)
