# Rock Solid Shutters

Front‑end: GitHub Pages  
Payments: Square Web Payments SDK (Vercel functions) + PayPal Smart Buttons  

## Deploy (Front‑end)
1. Upload to your repo: Dmouser86/Rock-Solid-Shutters-V3
2. GitHub → Settings → Pages → Deploy from main / root
3. Visit: https://dmouser86.github.io/Rock-Solid-Shutters-V3/

## Deploy (Payments on Vercel)
1. Import this repo
2. Add env vars (see `.env.example`), start with Sandbox
3. Ensure `/api/create-payment.js` builds with `square` SDK
4. Put Apple Pay verification at `/public/.well-known/apple-developer-merchantid-domain-association`
5. Update `assets/scripts/checkout-square.js` → applicationId, locationId, apiBase

## Switch to Live
- Change `SQUARE_ENVIRONMENT` to `production`
- Use `https://web.squarecdn.com/v1/square.js` in `pages/checkout.html`
- Replace PayPal Client ID with your Live ID

## Edit Products
- Update `/assets/scripts/pricing.js`
