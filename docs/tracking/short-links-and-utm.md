# Short Links And UTM Guide

This guide defines a practical tracking system for DolOffer creator and
affiliate campaigns. It separates click tracking from order attribution so
marketing reports stay useful and honest.

## Recommended Setup

Use a branded short-link domain:

- `go.doloffer.com` for public creator links.
- `d.doloffer.com` only if a very short domain is needed.

Each short link should redirect to a DolOffer page with UTM parameters and, when
available, the creator affiliate identifier or promo code.

```text
Short link:
https://go.doloffer.com/chatgpt-creator-a

Redirect target:
https://doloffer.com/?utm_source=youtube&utm_medium=creator&utm_campaign=chatgpt_recharge_2026_q2&utm_content=creator_a_video_001
```

## Naming Rules

Keep names lowercase, readable, and stable. Use underscores instead of spaces.

| Field | Purpose | Examples |
|---|---|---|
| `utm_source` | Traffic source or platform | `youtube`, `tiktok`, `instagram`, `x`, `blog`, `newsletter`, `telegram`, `discord`, `github` |
| `utm_medium` | Channel type | `creator`, `short_video`, `review`, `community`, `email`, `social`, `affiliate` |
| `utm_campaign` | Campaign or product theme | `chatgpt_recharge_2026_q2`, `youtube_premium_2026_q2`, `creator_launch_2026` |
| `utm_content` | Creator, placement, or asset ID | `creator_a_video_001`, `creator_b_bio`, `newsletter_may_01` |
| `utm_term` | Optional keyword or audience label | `ai_tools`, `student_plan`, `music_apps` |

## Short-Link Structure

Use one short link per creator, channel, and content asset when possible.

```text
go.doloffer.com/{product}-{creator}
go.doloffer.com/{product}-{creator}-{channel}
go.doloffer.com/{campaign}-{creator}-{asset}
```

Examples:

```text
go.doloffer.com/chatgpt-alex
go.doloffer.com/youtube-premium-alex-tiktok
go.doloffer.com/creator-launch-may-newsletter-001
```

## Creator Tracking Checklist

Before a creator publishes, confirm:

- the short link redirects to the correct DolOffer page;
- UTM values match the campaign naming rules;
- affiliate link or promo code is connected to the creator account;
- disclosure text appears near the first link or promo code;
- the product page still supports the claim being made;
- the creator has a unique link for each major channel.

## Reporting Model

Track three layers separately:

1. **Short-link clicks:** useful for traffic quality and channel comparison.
2. **Website events:** useful for registrations, product views, checkout starts,
   and other pre-order actions.
3. **Affiliate dashboard orders:** source of truth for commission, refund,
   payout, and valid attribution.

Short-link clicks are not the same as orders. Some clicks come from link
previews, bots, repeated tests, or users who are not ready to purchase.

## Bot And Preview Filtering

When reviewing click data, watch for:

- many clicks from the same IP or user agent;
- clicks immediately after publishing, before humans likely saw the content;
- social preview crawlers and messaging-app preview fetches;
- traffic spikes with no product views, registrations, or orders;
- geographic patterns that do not match the creator audience.

Do not pay commissions from short-link clicks alone. Use the DolOffer affiliate
dashboard and partner agreement as the source of truth.

## Tool Recommendations

Good short-link tools for this workflow:

- **Dub:** strong fit for branded short links, UTM templates, and affiliate-style
  attribution workflows.
- **Rebrandly:** good for teams that need branded links, roles, and reporting.
- **Short.io:** cost-effective choice for custom domains and API-driven link
  management.
- **Bitly:** familiar enterprise option with broad analytics support.
- **YOURLS:** self-hosted option when DolOffer wants full control over link data.

## Minimum Data To Store

For each short link, store:

- short URL;
- final destination URL;
- creator name or partner ID;
- product or campaign;
- channel;
- asset ID or content URL;
- UTM values;
- promo code, if used;
- creation date;
- owner or operator responsible for the link.

## Safe Public Wording

```text
Use this DolOffer link to check the current product details. This may be an
affiliate link, which means I may receive a commission or other benefit if you
purchase through it. Prices, availability, supported regions, refund rules, and
delivery methods can change, so verify the live page before ordering.
```
