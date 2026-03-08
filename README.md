# Booko Stripe Redirect Pages

Static pages hosted on `stripe.booko.deals` via GitHub Pages. Used by Stripe Connect onboarding and the Stripe checkout flow.

## Pages

| Page | URL | Purpose |
|:-----|:----|:--------|
| `index.html` | `stripe.booko.deals` | Root fallback — directs merchants back to Booko |
| `return/index.html` | `stripe.booko.deals/return` | Shown after Stripe form submission — confirms details are under review |
| `refresh/index.html` | `stripe.booko.deals/refresh` | Shown when the Stripe session expired or was not completed |
| `checkout.html` | `stripe.booko.deals/checkout.html` | Stripe Elements payment/card capture page used by the app |

## How it works

1. Merchant taps "Setup Payments" in the Booko app
2. `create_stripe_account_link` edge function creates a Stripe account link with:
   - `return_url` → `https://stripe.booko.deals/return`
   - `refresh_url` → `https://stripe.booko.deals/refresh`
3. Merchant completes or exits the Stripe form
4. Stripe redirects to the appropriate page
5. Merchant taps "X" to return to Booko

## Source of truth

These files are maintained in [`booko_platform/stripe_redirect_page/`](https://github.com/joshbooko/booko_platform). When updating, copy the contents of that folder here and push.

## Custom domain

The `CNAME` file points to `stripe.booko.deals`. DNS must have a CNAME record for `stripe` pointing to `joshbooko.github.io`.
