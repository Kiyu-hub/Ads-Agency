# Tracking Setup — Clasikal Homes

## Priority Order

Install in this sequence — don't launch ads without completing P1.

| Priority | Platform | Tracking | Status |
|----------|----------|---------|--------|
| P1 | Meta | Pixel + Standard Events | ☐ |
| P1 | Meta | Conversions API (CAPI) | ☐ |
| P1 | Google | gtag.js or GTM | ☐ |
| P1 | Google | Enhanced Conversions | ☐ |
| P2 | TikTok | Pixel + Events API | ☐ |
| P2 | All | Google Analytics 4 | ☐ |
| P3 | All | Server-Side GTM (sGTM) | ☐ |

---

## Meta Pixel Setup

### 1. Install Pixel
- Go to Meta Events Manager → Add Data Source → Web
- Pixel ID: get from Events Manager
- Add to `<head>` of every page on clasikalhomes.com OR via GTM

### 2. Standard Events to Fire

| Event | Trigger | Parameters |
|-------|---------|------------|
| `PageView` | Every page load | — |
| `ViewContent` | Product page view | `{content_id, content_name, value, currency: "GHS"}` |
| `AddToCart` | Add to cart button | `{content_id, value, currency: "GHS"}` |
| `InitiateCheckout` | Checkout start | `{value, currency: "GHS", num_items}` |
| `Purchase` | Order confirmation | `{value, currency: "GHS", order_id, content_ids[]}` |
| `Search` | Search results | `{search_string}` |

> **Critical:** Set `currency: "GHS"` (Ghana Cedi) on all value events.

### 3. Conversions API (CAPI)
- Required to recover iOS14+ signal loss
- If site is Shopify: install Meta's Shopify app (built-in CAPI)
- If custom: implement server-side event mirroring via Meta Business SDK
- Deduplication: send `event_id` on both browser and server events

### 4. Verify
- Use Meta Pixel Helper Chrome extension
- Check Events Manager → Test Events
- Ensure `Purchase` event fires on order confirmation with correct `value`

---

## Google Tracking Setup

### 1. Install Google Tag Manager
- Create GTM container at tagmanager.google.com
- Add GTM snippet to `<head>` and `<body>` of clasikalhomes.com
- All other tags go through GTM

### 2. Google Ads Conversion Actions

| Conversion | Tag | Value |
|------------|-----|-------|
| Purchase | Google Ads conversion tag | Dynamic (actual order value) |
| Add to Cart | Google Ads conversion tag | Dynamic or fixed value |
| Contact/WhatsApp Click | Google Ads conversion tag | $5 estimated |

### 3. Enhanced Conversions
- Enable in Google Ads → Conversions → Enhanced Conversions
- Sends hashed email/phone to improve match rate (privacy-safe)
- Required for Smart Bidding to perform well

### 4. Google Analytics 4
- Create GA4 property at analytics.google.com
- Link GA4 to Google Ads account
- Enable Enhanced Measurement (pageview, scroll, outbound clicks, site search)
- Set up custom events: `purchase`, `add_to_cart`, `view_item`

### 5. PMax Feed Requirements
For Google Shopping/PMax to work, submit a product feed:
- Via Google Merchant Center
- Required fields: `id`, `title`, `description`, `link`, `image_link`, `price`, `availability`, `condition`
- Currency: GHS
- Optimize titles: "Clasikal Homes [Product Name] [Key Feature] — [Category]"

---

## TikTok Pixel Setup

### 1. Install TikTok Pixel
- TikTok Ads Manager → Assets → Events → Web Events
- Add pixel to `<head>` via TikTok Tag or GTM

### 2. Events to Track

| Event | Trigger |
|-------|---------|
| `ViewContent` | Product page |
| `AddToCart` | Add to cart |
| `InitiateCheckout` | Checkout start |
| `PlaceAnOrder` | Purchase confirmation |

### 3. Events API (Server-Side)
- Mirror all events server-side for iOS signal recovery
- Include `ttclid` parameter from TikTok click URLs
- Pass `user_data`: hashed email, phone, IP

---

## WhatsApp Conversion Tracking

WhatsApp is a critical conversion path in Ghana. Track it:
- Add UTM parameters to all WhatsApp links: `https://wa.me/233XXXXXXXXX?text=Hi...&utm_source=meta&utm_medium=paid&utm_campaign=[campaign_name]`
- Create a Meta custom conversion for "WhatsApp Click" (click event on WhatsApp button)
- Track WhatsApp leads separately in a CRM or spreadsheet as "offline conversions"

---

## Verification Checklist

Before launching ads, confirm:
- [ ] Meta Pixel fires `Purchase` on order confirmation with correct GHS value
- [ ] CAPI events mirror browser events with matching `event_id`
- [ ] Google Ads shows conversion data within 24h of test purchase
- [ ] GA4 shows e-commerce events in DebugView
- [ ] Google Merchant Center shows products as "Active" (not disapproved)
- [ ] TikTok Pixel fires on product pages and checkout
- [ ] WhatsApp CTA links include UTM parameters
