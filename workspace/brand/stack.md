# Brand Stack

## Ad Accounts

| Platform | Account ID | Status |
|----------|-----------|--------|
| Meta | — | Add META_AD_ACCOUNT_ID to .env |
| Google Ads | — | Add GOOGLE_ADS_CUSTOMER_ID to .env |

## Performance Targets

| KPI | Target | Notes |
|-----|--------|-------|
| Meta ROAS | — | Set after first campaign |
| Meta CPA | — | Set after first campaign |
| Google CPA | — | Set after first campaign |
| Google ROAS | — | Set after first campaign |

## Brand

- **Business:** —
- **Website:** —
- **Industry:** —
- **Primary offer:** —

## Creative Guidelines

See `creative-kit.md` once populated by `/ads dna <url>`

## Notes

Populate this file by running:
1. `/ads start` — first-run wizard, fills account IDs and brand context
2. `/ads dna <url>` — extracts brand profile → `brand-profile.json`
3. `meta-ads-audit` — Meta account health check, saves `meta/business-context.json`
4. `google-ads-audit` — Google account health check, saves `business-context.json`
