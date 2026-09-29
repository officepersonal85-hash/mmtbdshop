# MMT BD Shop

A polished, responsive static storefront for **MMT BD Shop** — a curated international e-commerce experience for lifestyle, beauty and gift products from Bangladesh.

The site is intentionally lightweight: it is built with semantic HTML, modern CSS and vanilla JavaScript, so it can be hosted directly on GitHub Pages or any static web host without a build step.

## Highlights

- Responsive storefront layout for mobile, tablet and desktop
- Searchable, filterable product catalogue
- Lightweight shopping bag with `localStorage` persistence
- WhatsApp order handoff with product names, quantities, estimated total and an optional note
- Clear support messaging for bKash, Nagad and delivery confirmation
- Accessible labels, keyboard-friendly controls, focus states and `aria-live` status messaging
- No framework, bundler or server required
- `shop.html` retained as a backwards-compatible alias for the main `index.html` page

## Quick start

1. Clone the repository.
2. Open `index.html` in a browser, or serve the folder with any static server:

   ```bash
   python3 -m http.server 8080
   ```

3. Visit `http://localhost:8080`.

## Configure before launch

The storefront includes a clearly marked placeholder WhatsApp number. Replace it in **both** `index.html` and `shop.html`:

```js
const STORE = {
  whatsapp: "8801XXXXXXXXX",
  currency: "৳"
};
```

Also replace the placeholder number in the `wa.me` links in the navigation story, footer and floating WhatsApp button. Use the international format with no `+`, spaces or punctuation.

Product data is kept near the bottom of each HTML file in the `products` array. Each item supports:

- `name` — product title
- `category` — `beauty`, `lifestyle` or `gifts`
- `price` — numeric price in Bangladeshi Taka
- `emoji` — lightweight visual placeholder that can be replaced with an image later
- `desc` — short product description
- `label` — badge shown on the product card

For production, confirm product availability, final delivery charges, returns policy, payment instructions and any required business information before publishing.

## GitHub Pages deployment

1. Push the repository to GitHub.
2. In the repository, open **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**.
4. Select the `main` branch and `/ (root)` folder.
5. Save and wait for GitHub Pages to publish the site.

Because the site is static, no secrets or server environment variables are required. If the repository is renamed, update any external links that point to it.

## Project structure

```text
.
├── index.html   # Primary storefront and home page
├── shop.html    # Backwards-compatible copy of the storefront
└── README.md    # Setup and deployment documentation
```

## Customization ideas

- Replace emoji artwork with licensed product photography in local `assets/` files.
- Add a real inventory or checkout backend when order volume requires it.
- Add privacy, shipping and returns pages before running paid campaigns.
- Connect the newsletter form to a consent-based email provider; it currently confirms locally without sending data anywhere.

## License

No license has been declared yet. Add a repository license before distributing or reusing the code publicly.
