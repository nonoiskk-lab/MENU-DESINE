# LovBites Café & Kitchen — Menu Design

A structured, print-ready menu system for **LovBites Café & Kitchen (Dhanbad)**, built from
`LOVBITES_RESTAURANT_MENU.xlsx` and the official LovBites logo. No item name, price, or category
was changed from the source spreadsheet.

## What's here

| Path | Purpose |
|---|---|
| `data/menu.json` | Full structured menu data (120 items, 24 categories) parsed from the Excel, with veg/non-veg/egg flags, signature-item flags, and flagged data issues. |
| `data/menu.csv` | Same data as a flat spreadsheet, for quick review or re-import into Excel/Canva. |
| `docs/menu-architecture.md` | The page-by-page menu architecture, design system (colors/type/spacing), data-issue notes, and photography priority list. |
| `menu/index.html` | The final print-ready menu — a 17-page A4 HTML/CSS booklet using the real data and logo. Open in a browser and use **Print → Save as PDF** for production output, or hand off to a designer for Canva/Adobe Express/InDesign. |
| `assets/lovbites-logo.jpg` | The official LovBites logo used throughout the menu. |

## Data issues flagged (not auto-corrected — see `docs/menu-architecture.md` for detail)

1. **Packaged Drinking Water** has a non-numeric price (`As per MRP`) in the source file.
2. Two probable duplicate entries in **Protein Power Bowls** (identical description + price
   under two different names).
3. A price inconsistency between two near-identical Rajma bowl entries.

## Photography

No AI-generated food images were used. Each menu page has marked photo slots ready for real
food photography — `docs/menu-architecture.md` lists the 13 signature/bestseller items to
prioritize for a photo shoot.

## Next steps for production print

1. Confirm final trim size (A4 assumed) and single vs. split café/fine-dine menu.
2. Resolve the flagged data issues above.
3. Shoot or source real food photography for the signature items and drop them into the photo
   slots in `menu/index.html`.
4. Add the restaurant's full address, phone number, and social handles on the back cover.
