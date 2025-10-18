# Stripe Connect Redirect Page

## What This Is

This HTML file needs to be hosted on **booko.deals** to handle Stripe Connect redirects.

When merchants complete Stripe onboarding, they'll be sent to:
`https://booko.deals/merchant_stripe_connect_return`

This page will automatically open the Booko app using the deep link `booko://`.

## How to Deploy

Upload `index.html` to your booko.deals hosting at:
- **Path**: `/merchant_stripe_connect_return/index.html`
- **Full URL**: `https://booko.deals/merchant_stripe_connect_return`

### If using Netlify:
1. Create a folder named `merchant_stripe_connect_return`
2. Put `index.html` inside it
3. Upload to your booko.deals Netlify site

### If using cPanel/FTP:
1. Navigate to public_html (or www)
2. Create folder `merchant_stripe_connect_return`
3. Upload `index.html` inside it

### If using Vercel/GitHub Pages:
1. Add the folder to your repository
2. Deploy

## Testing

After uploading, visit: `https://booko.deals/merchant_stripe_connect_return`

You should see a nice page that tries to open the app.

## That's It!

Once this page is live, the Stripe Connect flow will work:
1. User taps "Setup Payments" in app
2. Stripe onboarding opens in browser
3. User completes onboarding
4. Stripe redirects to booko.deals
5. Page opens the Booko app automatically
