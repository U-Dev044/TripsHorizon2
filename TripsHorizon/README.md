# TripsHorizon — Static demo (Version 1.7)

TripsHorizon is now a static website built with HTML, CSS and vanilla JavaScript. It can be hosted on GitHub Pages or any static web host. No Node.js server, backend, build step or package installation is required.

## Files

- `index.html`, `styles.css`, `script.js` — homepage, search interface, destination discovery, sample listings and quick-answer travel assistant.
- `destination.html`, `destination.css`, `destination.js` — destination guide pages (Santorini, Bali, Dubai and Cinque Terre).
- `reservation.html`, `reservation.css`, `reservation.js` — sample flight, stay and car options with an estimated trip summary and direct WhatsApp enquiry.
- `site-config.js` — the single place to change the public reception WhatsApp number.

## Change the WhatsApp number

1. Open `site-config.js`.
2. Find `whatsappNumber: '12025550147'`.
3. Replace it with your international number: country code followed by the phone number, digits only (no `+`, spaces or punctuation).
4. Save and upload the changed file to GitHub.

Example format for a Nigerian number: `2348012345678` (use your own real number).

## Preview locally

You can open `index.html` directly in a browser. For a more reliable local preview, use the VS Code Live Server extension or Python's built-in static server:

```bash
python -m http.server 8000
```

Then visit `http://localhost:8000`.

## Deploy with GitHub Pages

1. Create a GitHub repository, for example `tripshorizon`.
2. Upload all files and folders from this project to the repository's root. Keep `index.html` at the root.
3. In the repository, open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select the `main` branch and `/ (root)` folder, then save.
6. Wait for GitHub Pages to publish the site. The public URL will appear in the Pages settings.

## What this static edition can and cannot do

- The site pages, responsive styling, sample search results, trip estimates and destination guides run in the browser.
- The reservation button opens WhatsApp with the selected trip details prefilled. The visitor still has to press Send in WhatsApp.
- The floating travel assistant uses built-in quick answers only; it does not call a hosted AI model.
- Listings and prices are illustrative, not live inventory or supplier quotes.
- There is no backend, customer account system, admin dashboard, booking database, secure payment processing or saved reservation record in this edition.
- Do not put API keys, passwords or private credentials in this public repository. The WhatsApp number in `site-config.js` is public by design.

This is an educational/demo website. Reception must verify availability, final prices and payment instructions directly with the customer. No booking or payment is confirmed by this site.
