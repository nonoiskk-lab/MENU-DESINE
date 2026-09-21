# LovBites Café & Kitchen — Menu Architecture & Data Notes

Source of truth: `LOVBITES_RESTAURANT_MENU.xlsx` (120 items, 24 raw categories) and the official
LovBites logo (`assets/lovbites-logo.jpg`). No item name, price, or category was changed —
see **Data Issues Flagged** below for the only inconsistencies found; nothing was guessed.

## 1. Data Analysis Summary

- **120 total items** across **24 Excel categories**, grouped below into **13 printed sections**
  (cover + back cover not counted) so the booklet reads as a designed menu, not a spreadsheet.
- **13 items marked signature/bestseller** (⭐ in source) — these get priority placement and,
  when real food photography is available, first choice for a photo.
- Two service windows drive placement: `8 AM – 1 PM` (breakfast items) and `1 PM – CLOSING`
  (lunch/dinner items); `ALL DAY` items are placed with their nearest thematic section.

### Data Issues Flagged (not auto-corrected)

1. **Row 113 — "Packaged Drinking Water"**: price is `As per MRP`, not a number. Printed as
   "As per MRP" rather than a ₹ figure; flagging in case a fixed price should be supplied.
2. **Probable duplicate — rows 15 & 25**: "Paneer Protein Bowl ⭐" and "Paneer Power Bowl ⭐"
   share an identical description ("Paneer, rice, vegetables and light dressing.") and identical
   price (₹249) inside the same category (Protein Power Bowls). Likely the same dish entered
   twice under two names.
3. **Probable duplicate — rows 17 & 27**: "Chicken Protein Bowl ⭐" and "Grilled Chicken Power
   Bowl ⭐" share an identical description ("Grilled chicken with rice and salad.") and identical
   price (₹299), same category. Likely the same dish entered twice.
4. **Price inconsistency — rows 16 & 26**: "Rajma Rice Power Bowl" (₹229) and "Rajma Protein
   Bowl" (₹249) have near-identical descriptions but different prices — worth confirming which
   is correct before print.

Both items in each duplicate pair are kept in the data and on the printed menu (nothing was
removed), flagged here for the owner to resolve before final print.

## 2. Signature / Photography-Priority Items

If/when real food photography is shot, prioritize these 13 (highest visual + commercial value):

| Item | Section | Price |
|---|---|---|
| Chicken Dum Biryani Signature | Rice & Biryani | ₹329 |
| Butter Chicken | Non-Veg Main Course | ₹329 |
| Slow-Cooked Mutton Curry | Non-Veg Main Course | ₹429 |
| Dal Makhani Signature | Veg Main Course | ₹229 |
| Kadhai Paneer Signature | Veg Main Course | ₹249 |
| Chicken Tikka - 8 Pc | Kebab & Tandoor | ₹329 |
| Korean Crispy Chicken | Crispy Chicken | ₹299 |
| Paneer Tikka - 8 Pc | Veg Starters | ₹269 |
| Grilled Chicken Power Bowl / Chicken Protein Bowl | Protein Power Bowls | ₹299 |
| Paneer Power Bowl / Paneer Protein Bowl | Protein Power Bowls | ₹249 |
| Cold Coffee Whey Shake | Protein Shakes | ₹269 |

No AI-generated "photorealistic" food images were created for this pass — per the brief, only
real photography (or images explicitly supplied) should represent LovBites' actual food. The
design below is deliberately typography-led so it looks complete and premium with zero photos,
and has marked photo slots ready to receive real photography later without a re-layout.

## 3. Printed Menu Architecture (page-by-page)

Format assumed: **A4 portrait booklet** (single café + fine-dine menu, not split) — confirm with
owner if A5 or a different trim is preferred before print.

| # | Page | Categories included | Items | Photo slots |
|---|---|---|---|---|
| 1 | Cover | Logo, "Cafe & Kitchen · 8 AM Onwards" | — | 0 (full-bleed brand page) |
| 2 | Brand intro | One-line concept, hours, veg/non-veg legend | — | 0 |
| 3 | Breakfast | Healthy Breakfast, Protein Breakfast | 10 | 2 hero |
| 4 | Desi Breakfast & Eggs | Desi Favourites, Egg Corner | 7 | 1 hero |
| 5 | Protein Lab | Healthy Bowls, Protein Power Bowls | 9 | 2 hero |
| 6 | Shakes, Smoothies & Healthy Drinks | Protein Shakes, Smoothies, Healthy Drinks | 8 | 1 hero |
| 7 | Soups & Veg Starters | Soup (Veg), Veg Starters | 12 | 2 hero |
| 8 | Non-Veg Starters & Crispy Chicken | Soup (Non-Veg), Non-Veg Starters, Crispy Chicken | 10 | 2 hero |
| 9 | Indo-Chinese | Indo-Chinese | 9 | 1 hero |
| 10 | Kebab & Tandoor | Kebab & Tandoor | 10 | 2 hero |
| 11 | Sizzlers & Veg Main Course | Sizzlers, Veg Main Course | 10 | 1 hero |
| 12 | Non-Veg Main Course | Non-Veg Main Course | 8 | 2 hero |
| 13 | Breads | Breads | 9 | 0 (icon-led, no photos needed) |
| 14 | Rice & Biryani | Rice & Biryani | 5 | 1 hero |
| 15 | Salads, Papad & Sides | Salad & Papad | 4 | 0 |
| 16 | Beverages & Add-Ons | Beverage, Add-On | 9 | 0 |
| 17 | Back cover | Address, contact, ordering info (dine-in/delivery/QR) | — | 0 |

Recommended density: **6–12 items per page**, never more than 12 on a single spread, so the
guest can scan a full category without turning back — Breads (9) and Kebab & Tandoor (10) are
the densest pages and get tighter line spacing, not smaller type.

## 4. Design System

- **Colors**: LovBites red `#D62828` (from logo) as the primary accent for category headers,
  prices and the heart mark; near-black `#2B2B2B` for item names and body copy; warm off-white
  `#FFFBF7` page background; a soft neutral `#F4EDE7` for section dividers/photo-slot frames.
- **Typography hierarchy**: category titles in a bold display serif/rounded face (strongest
  weight, largest size, red or near-black); item name second-strongest (bold, near-black);
  description third (regular weight, smaller, gray `#6B6B6B`); price visible but never the
  largest element on the page (bold red, same optical size as the item name or one step down).
- **Price placement**: right-aligned in a fixed-width column per page so every price in a
  category lines up vertically — supports fast scanning without dominating the layout.
- **Veg/Non-Veg marks**: small green/red dot-in-square legend mark before each item name.
- **Whitespace**: minimum 16px gutter between items, generous margin (20mm) on every printed
  page, category header gets extra top space to separate it from the previous section.
- **No black-and-gold luxury styling, no heavy gradients, no clutter** — clean Indian
  contemporary, Instagram-friendly, matches the LovBites red/white brand mark.

## 5. Status

This architecture (steps 1–4) is the approved wireframe layer. `menu/index.html` implements it
as a working, print-ready HTML/CSS booklet using the exact data above — open it in a browser and
use Print → Save as PDF for a production-ready file, or hand the HTML/CSS to a designer to
rebuild in InDesign/Canva/Adobe Express using this same architecture and design system.
