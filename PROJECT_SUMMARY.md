# TindaCheck — Project Summary

**Built at the StellarPH × KMC Claude AI Workshop · Cebu, Philippines · April 10, 2026**

---

## What We Built

**TindaCheck** is a mobile price comparison tool for grocery shoppers. You enter two or more products — different brands, different sizes, different prices — and it instantly tells you which one gives you the most for your money.

---

## The Problem

Standing in a grocery aisle trying to figure out if the 500ml bottle for ₱45 is a better deal than the 1L bottle for ₱82 is genuinely hard. Most people guess. Most people guess wrong.

Pack sizes are never the same. Brands compete on price but hide the real cost behind different volumes and weights. A shopper without a calculator — or the time and confidence to use one mid-aisle — has no good way to compare.

**This hits everyday Filipino grocery shoppers the hardest.** Families stretching a weekly budget, people shopping at S&R, SM, or Puregold, anyone buying in bulk who wants to know if it's actually worth it. The math isn't complicated — it's just inconvenient enough that most people skip it.

---

## How It Works — Screen by Screen

### Compare Tab *(the main screen)*
You land here first. There are two product cards waiting.

Fill in each card:
- **Product name** — type it, or tap the barcode icon to scan the product with your camera
- **Packaging type** — optional label (bottle, can, pouch, sachet, bag, box, tetra pack)
- **Size and unit** — e.g. `500` `ml`, or `1` `kg`
- **Number of packs** — buying two? Enter 2. A live total updates as you type so you can see the combined volume at a glance
- **Total price** — what you'd pay at the shelf

Tap **Compare Prices**. Results appear instantly.

The app normalises everything to the same base unit — per 100ml, per 100g, or per piece — so a 500ml product and a 1L product are on a level playing field.

**Results are colour-coded:**
- 🟢 **Green** = cheapest per unit
- 🟡 **Amber** = middle
- 🔴 **Red** = most expensive

Each non-winner shows a savings line: *"Del Monte is 8% cheaper — saves you ₱0.92 per 100g."* You can add the winner to your cart directly from the results.

Need to compare more than two? Tap **+ Add Another Item** to add up to 5 products at once.

---

### My List Tab
Before you go shopping, build your list here. Add items with a name, size, and unit. When you're in the store and ready to compare, tap **Price Check** on any item — it jumps straight to the Compare tab with that product's details pre-filled. You just enter the prices.

Items already in your cart show a **✓ In Cart** badge so you don't double-add.

---

### Cart Tab
As you do comparisons, add the winning product to your cart. The cart keeps a running total. Each item has **+ / −** quantity buttons if you're buying more than one. When you're ready to check out, tap **Start Grocery Run** to begin a timed shopping trip.

---

### History Tab
Every comparison you've ever run is saved here. Tap any entry to see the full breakdown — all products, per-unit prices, and the winner. Useful for checking what you paid last week, or confirming a regular buy is still the best deal.

**Grocery Runs** also appear here — each completed run shows the date, how long it took, every item bought, and the total spend.

---

### Dark / Light Mode
A toggle in the top-right corner switches between dark and light themes. The app remembers your preference.

---

## Technology

- **Single HTML file.** The entire app is `index.html` — no framework, no build step, no server. Open it in any browser and it works.
- **Vanilla JavaScript.** All comparison logic, state management, and UI rendering written from scratch.
- **localStorage.** Your grocery list, comparison history, cart, and theme preference are saved in your browser. Nothing leaves your device.
- **Inter (Google Fonts).** Clean, readable typeface designed for screens.
- **html5-qrcode library.** Powers the barcode scanner — accesses your device camera and reads EAN/UPC barcodes.
- **Open Food Facts API.** When a barcode is scanned, the app looks up the product name and size automatically so you don't have to type them.
- **CSS custom properties + two full themes.** Dark and light modes built with a complete design token system — colours, shadows, borders, and surfaces all swap cleanly.
- **No login. No account. No install required.**

---

## What Each Team Member Built

| Person | Contribution |
|--------|-------------|
| **Cris Militante** *(Pod Leader)* | Core price comparison engine and formula, barcode scanner integration with Open Food Facts API, My List size/unit pre-fill, Grocery Run feature, UI polish pass (Inter font, refined colour palette, shadows), cart quantity stepper, savings percentage display |
| **Kyle** | Product card redesign and field layout, Obsidian dark theme, size × packs formula refinement, size hint text and live total, packaging dropdown, scanner no-match fix |
| **Kael** | My List tab and Compare pre-fill, comparison history tab, dynamic add/remove product cards |
| **Carl Cabasag** | User testing, demo script, notes documentation |
| **Michael Ian Rule** | User testing, feature feedback, demo preparation |

---

## What We'd Build Next

**Camera price scanning** — point your phone at the shelf price tag and have the price fill in automatically. No typing at all.

**Share a comparison** — send results to a family member via a link or WhatsApp screenshot before you buy.

**Store presets** — save the prices of your regular items at S&R, SM, and Puregold so you can compare across stores, not just across brands.

**Cost per serving** — for coffee, powdered milk, or cereal, compare by cost per cup or per bowl rather than per gram.

**PWA / home screen install** — one tap to add TindaCheck to your phone's home screen so it feels like a native app, not a browser tab.

---

## What We Learned About Building with AI

- **The fastest way to build is to describe the outcome, not the code.** Prompts like *"add a live total that updates as the user types size and quantity"* worked better than trying to specify which function to write. AI fills in the how — your job is to be clear about the what.

- **AI is a great pair programmer but a terrible decision-maker.** Every time we gave Claude a vague instruction, we got a vague result. The sharper the brief, the better the output. Thinking clearly about what you want is still the real skill.

- **You can go from idea to working demo in hours, not weeks.** Five people with no shared codebase, no prior planning, and a 5-hour window built a complete multi-tab mobile app with a barcode scanner, persistent storage, and two full UI themes. That's only possible when AI handles the boilerplate and you focus on the product.

---

## Try It

Open `index.html` in any browser — desktop or mobile. No internet required after first load (barcode lookup needs a connection, everything else is offline-first).

**GitHub:** https://github.com/arc-web/claudeconference-pod-a

---

*Built in 5 hours by Pod A at the StellarPH × KMC Claude AI Workshop, Cebu, April 10, 2026.*
