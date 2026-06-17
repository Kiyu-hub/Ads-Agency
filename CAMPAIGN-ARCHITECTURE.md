# Campaign Architecture — Clasikal Homes

## Naming Convention
```
[Platform]_[Objective]_[Audience]_[Geo]_[YYYYMM]
```
Examples:
- `META_CONV_ASC_GH_202607`
- `GOOG_SHOP_PMax_CoreProducts_GH_202607`
- `TIKTOK_CONV_Prospecting_GH_202607`

---

## Meta Ads Architecture

```
Meta Account — Clasikal Homes
│
├── META_CONV_ASC_GH_202607
│   [Advantage+ Sales Campaign — always-on, primary revenue driver]
│   └── ASC Ad Set (broad, Meta optimizes)
│       ├── Ad: Carousel — Living Room Collection
│       ├── Ad: Reel — "Elevate Every Corner" transformation
│       ├── Ad: Static — Hero product with royal blue overlay
│       ├── Ad: Collection — Shop the Look (dining room)
│       ├── Ad: Reel — Craftsmanship close-up story
│       └── Ad: Static — Founder story / brand trust
│
├── META_CONV_Prospecting_GH_202607
│   [Manual interest targeting — mid-funnel]
│   ├── Ad Set: Interior design enthusiasts (GH, 28-50)
│   │   ├── Ad: Transformation before/after
│   │   └── Ad: "Your home deserves better" static
│   └── Ad Set: Homeowners + Luxury lifestyle (GH, 30-55)
│       ├── Ad: Room makeover carousel
│       └── Ad: Product spotlight with emotional headline
│
├── META_CONV_Retargeting_GH_202607
│   [Bottom funnel — warm audiences]
│   ├── Ad Set: Website Visitors 7 days
│   │   └── Ad: "Still thinking about it?" — product reminder
│   ├── Ad Set: Add to Cart / Initiate Checkout 14 days
│   │   └── Ad: Offer or free delivery incentive
│   └── Ad Set: Video Viewers 75% (30 days)
│       └── Ad: Social proof + strong CTA
│
└── META_CONV_Testing_GH_202607
    [Creative and audience experiments — 10% budget]
    ├── Ad Set: UGC-style creative test
    └── Ad Set: WhatsApp click-to-chat conversion test
```

---

## Google Ads Architecture

```
Google Account — Clasikal Homes
│
├── GOOG_BRAND_Search_GH_202607
│   [Brand protection — always-on, low spend]
│   └── Ad Group: Brand terms
│       Keywords: "clasikal homes", "clasikal furniture", "clasikalhomes.com"
│
├── GOOG_SHOP_PMax_CoreProducts_GH_202607
│   [Performance Max — primary Shopping driver]
│   ├── Asset Group: Living Room
│   │   Texts: "Luxury Living Room Decor Ghana" / "Transform Your Living Space"
│   │   Images: Editorial living room photos (1200×628 + 1200×1200)
│   │   Videos: Room tour / product highlight (optional)
│   ├── Asset Group: Dining Room
│   └── Asset Group: Bedroom & Accessories
│
├── GOOG_SEARCH_NonBrand_GH_202607
│   [High-intent search capture]
│   ├── Ad Group: Home Decor Ghana
│   │   Keywords: "home decor ghana", "luxury home decor accra",
│   │             "buy furniture ghana", "interior decor shop ghana"
│   └── Ad Group: Room-Specific
│       Keywords: "living room furniture ghana", "dining room set accra",
│                 "home accessories ghana", "modern furniture ghana"
│
└── GOOG_SHOP_Standard_GH_202607
    [Standard Shopping — fallback / price-sensitive segments]
    └── Product feed from clasikalhomes.com
```

---

## TikTok Ads Architecture

```
TikTok Account — Clasikal Homes
│
├── TIKTOK_CONV_SmartPlus_GH_202607
│   [Smart+ — TikTok's equivalent of ASC]
│   └── Ad Group: Broad Ghana targeting
│       ├── Ad: Before/after room transformation (15s)
│       ├── Ad: Styling tip with product feature (30s)
│       └── Ad: "POV: Your home after Clasikal Homes" (15s)
│
└── TIKTOK_AWARE_Prospecting_GH_202607
    [Brand awareness — secondary]
    └── Ad Group: Interior design interest, 22-40, GH
        └── Ad: Founder story / brand intro (30s)
```

---

## Audience Definitions

| Audience | Platform | Definition |
|----------|----------|------------|
| Core Prospecting | Meta | GH, 28–50, interests: interior design, home decor, luxury lifestyle, real estate |
| Homeowners | Meta | GH, 30–55, life event: new home, interests: furniture |
| Website Visitors 7d | Meta | All website visitors, last 7 days |
| Cart Abandoners 14d | Meta | AddToCart event, last 14 days, exclude Purchasers |
| Video Viewers 75% | Meta | Watched 75%+ of any video ad, last 30 days |
| Purchaser Lookalike | Meta | 5% lookalike of past purchasers (Ghana) |
| Brand Search | Google | "clasikal*" keyword match |
| High-Intent Search | Google | "buy home decor ghana", "luxury furniture accra" |
| Product Feed | Google | All active products from site catalog |
| Broad GH | TikTok | Ghana, 22–45, broad interest in home/lifestyle |
