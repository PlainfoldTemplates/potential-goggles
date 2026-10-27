# Plainfold Leases

A single-page online shop that sells state-specific residential rental agreements. There are 51 listings (50 states plus DC) at $12.00 each, and an all-states bundle at $25.00. Each listing is a ZIP containing a print-ready PDF, an editable Word file and a quick-start guide.

## What's in this project

| File | What it is |
|---|---|
| `rental-agreement-shop.html` | The whole website: page, styles, product data and cart logic in one file |
| `Single_State_Listings.csv` | Listing data: state, title, price, tags, file name, description |
| `Single_State_Listings.md` | The same listing data in Markdown |
| `State_Files/` | One ZIP per state (the products customers receive) |

## What the site does

- A state picker in the hero shows each state's deposit cap and return deadline.
- A searchable grid lists all 51 states, with the state rules built into each lease.
- A bundle offer sells every state for $25.00.
- The cart works in the browser. Adding the bundle replaces any individual states.
- It supports light and dark mode and works on phones.

**Checkout is a placeholder.** The site does not take payment or deliver files yet. See "Taking payments" below.

## Put it online for free

The site is one static HTML file, so any free static host works.

1. Rename `rental-agreement-shop.html` to `index.html`.
2. Upload it to one of these:
   - **Netlify Drop:** drag the file onto app.netlify.com/drop. You get a public link in about a minute.
   - **Cloudflare Pages** or **GitHub Pages:** free, with a bit more setup. Better for long-term editing.
3. Optional: connect your own domain in the host's settings.

## Taking payments and delivering files

A static host cannot charge cards or send files, so connect a payment tool:

1. Create a product for each state ZIP, plus the bundle, on **Gumroad**, **Payhip** or **Lemon Squeezy**.
2. Copy each product's checkout link.
3. In the HTML, replace the "Add to cart" behavior with a link to that product's checkout page.

**Etsy:** the CSV already matches Etsy's listing fields (title, tags, price, file, description), so you can list the products there without using this site.

## Editing the site

Open the HTML file in any text editor.

- **State prices and rules:** find `var D=` in the script. Each state is an object like `{"s":"Florida","p":12,"d":[...]}`. `s` is the name, `p` is the price and `d` is the list of state rules.
- **Bundle price:** change `BP=25` in the script. Also update the visible `$25.00` and `$612.00 separately` text in the bundle banner, and the `$25` mention in the FAQ.
- **Brand name:** search for "Plainfold Leases" and replace it.
- **Colors:** change the values at the top of the `<style>` block (`--accent`, `--hl`, `--bg`, `--ink`).
- **FAQ and footer text:** edit the text directly in the HTML.

If you change prices in the CSV, update the `p` values in the HTML to match.

## Before you launch

- Check each state's rules against current law. The listings state that they are general-information templates, not legal advice.
- Confirm every ZIP opens and contains the PDF, the Word file and `READ_ME_FIRST.txt`.
- Add your contact email so buyers can reach you about file problems. The listing copy promises that.
- Add your refund policy. The current copy says digital downloads are not refundable.
- Test the site on a phone and in dark mode.

## Disclaimer

The templates are general-information documents, not legal advice. Laws and local ordinances change often. Buyers should confirm current requirements or consult a licensed attorney before use.
