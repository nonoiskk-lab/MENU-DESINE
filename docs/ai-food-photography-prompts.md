# AI Food Photography Task Brief — LovBites Café & Kitchen

Full, ready-to-use task for an image-generation AI assistant (ChatGPT Image, Gemini,
Midjourney, Flux, Ideogram, Leonardo, etc.) to produce **photorealistic dish photography that
does not read as AI-generated**. Covers the 17 photo slots already laid out in
`menu/index.html` / `docs/menu-architecture.md`.

> Real photography of the actual dishes is always the better option. Use this only when real
> photos aren't available yet — and swap them out for real shots the moment they exist.

---

## 1. How to use this brief

1. Check **Section 4 (Image Specification Table)** for exactly which slot each image goes into,
   what shape/resolution it must be, and how it will be cropped — so the image is generated
   already fitted to the design instead of being squeezed or cropped badly afterwards.
2. Give the AI assistant **Section 2 (Master Style Template) + Section 3 (Avoid-AI-Look
   Checklist)** once, as standing instructions for the whole job.
3. Then feed it **one prompt at a time from Section 5** (one image per prompt — don't batch
   multiple dishes in one image), always including that dish's aspect ratio from Section 4.
4. Generate **3–4 variations per dish**, pick the one with the least "AI sheen" (see checklist),
   and if possible run it through a light photo-editing pass (see Section 6) before using it.
5. Save each output using the exact filename from Section 4 and hand the files back — they'll
   be dropped straight into the matching slot in `menu/index.html`.

---

## 2. Master Style Template (paste before every dish prompt)

```
Professional restaurant food photography for an Indian café menu.
Camera: shot as if on a DSLR, 50mm lens, f/2.8, natural window light from one side,
soft falloff shadow, shallow depth of field with background gently out of focus.
Composition: 45-degree angle (or top-down flat lay where noted), dish slightly off-center
with breathing room for menu text, on a simple matte stoneware or dark slate plate,
plain wooden or dark neutral tabletop background, one folded cloth napkin and plain steel
cutlery placed naturally to the side.
Lighting and color: realistic, slightly warm, true-to-life color — not oversaturated,
not neon, not overly glossy. Visible natural steam only for dishes served hot.
Portion size: a real single-serving restaurant portion, not oversized or stacked for effect.
No text, no watermark, no logo, no hands, no cartoon or illustration style —
must look like an unedited photograph taken in a real restaurant kitchen, with natural
small imperfections (uneven sauce drizzle, slightly irregular garnish, a few real crumbs).
```

## 3. Avoid-AI-Look Checklist (apply to every prompt / reject renders that show these)

Reject or re-prompt if the image shows any of:

- **Waxy / airbrushed sheen** on food surfaces (real sauces and oils are uneven, not glossy
  all over)
- **Unnatural symmetry** — identical garnish pieces spaced perfectly, mirrored sauce swirls
- **Melted, warped or physically-impossible garnish** (herbs fused into the sauce, floating
  seeds, garnish that ignores gravity)
- **Illogical shadows or reflections** — shadows pointing different directions, cutlery with no
  shadow, reflections that don't match the light source
- **Oversaturated / neon colors** — Indian gravies and fried food are warm but not glowing
- **Distorted plate/bowl edges** — ovals that aren't true ellipses, rims that warp
- **Repeated identical texture patterns** (a telltale AI tiling artifact) in rice, curry, or
  breading
- **Extra or fused utensils/objects**, or a hand with wrong finger count if a hand appears —
  default to **no hands in frame** to avoid this entirely
- **Unnaturally perfect bokeh circles** in the background
- **Illegible warped "text"-like marks** anywhere in the frame (napkin prints, packaging)

Add explicitly to prompts as a closing line:
```
Avoid: glossy/waxy texture, perfect symmetry, warped or floating garnish, mismatched shadows,
oversaturated colors, distorted plate edges, repeated texture tiling, extra utensils, any
hands, fake-looking bokeh, illegible text marks. Must look like a real unedited photograph,
not an AI render.
```

---

## 4. Image Specification Table — which slot needs what image

Every photo slot in `menu/index.html` is a **fixed 16:9 landscape box** (this is true for both
the single-photo and the two-photo rows — the two-photo rows are just two 16:9 boxes side by
side, not two different shapes). Layout math from the actual CSS: A4 page = 210mm wide with
16mm margins → 178mm usable width.

| Slot | Page | Menu Section | Dish (Price) | Filename | Slot type | Printed size on page | Min. generate resolution |
|---|---|---|---|---|---|---|---|
| 1 | 3 – Breakfast | Healthy Breakfast | Paneer Stuffed Chilla (₹189) | `healthy-breakfast-hero.jpg` | Half-width (2-up) | 84mm × 47mm | 2000×1125px |
| 2 | 3 – Breakfast | Protein Breakfast | Egg & Chicken Protein Breakfast (₹249) | `protein-breakfast-hero.jpg` | Half-width (2-up) | 84mm × 47mm | 2000×1125px |
| 3 | 4 – Desi Breakfast & Eggs | Desi Favourites | Classic Chole Bhature (₹159) | `desi-favourites-hero.jpg` | Full-width (1-up) | 178mm × 100mm | 3000×1688px |
| 4 | 5 – Protein Lab | Protein Power Bowls | Paneer Power Bowl ⭐ (₹249) | `protein-bowl-paneer.jpg` | Half-width (2-up) | 84mm × 47mm | 2000×1125px |
| 5 | 5 – Protein Lab | Protein Power Bowls | Grilled Chicken Power Bowl ⭐ (₹299) | `protein-bowl-chicken.jpg` | Half-width (2-up) | 84mm × 47mm | 2000×1125px |
| 6 | 6 – Shakes/Smoothies/Drinks | Protein Shakes | Cold Coffee Whey Shake ⭐ (₹269) | `cold-coffee-whey-shake.jpg` | Full-width (1-up) | 178mm × 100mm | 3000×1688px |
| 7 | 7 – Soups & Veg Starters | Soup (Veg) | Veg Manchow Soup (₹149) | `veg-manchow-soup.jpg` | Half-width (2-up) | 84mm × 47mm | 2000×1125px |
| 8 | 7 – Soups & Veg Starters | Veg Starters | Paneer Tikka - 8 Pc ⭐ (₹269) | `paneer-tikka-hero.jpg` | Half-width (2-up) | 84mm × 47mm | 2000×1125px |
| 9 | 8 – Non-Veg Starters & Crispy Chicken | Non-Veg Starters | Chicken Lollipop (₹299) | `chicken-lollipop.jpg` | Half-width (2-up) | 84mm × 47mm | 2000×1125px |
| 10 | 8 – Non-Veg Starters & Crispy Chicken | Crispy Chicken | Korean Crispy Chicken ⭐ (₹299) | `korean-crispy-chicken.jpg` | Half-width (2-up) | 84mm × 47mm | 2000×1125px |
| 11 | 9 – Indo-Chinese | Indo-Chinese | Chicken Hakka Noodles (₹229) | `chicken-hakka-noodles.jpg` | Full-width (1-up) | 178mm × 100mm | 3000×1688px |
| 12 | 10 – Kebab & Tandoor | Kebab & Tandoor | Chicken Tikka - 8 Pc ⭐ (₹329) | `chicken-tikka-hero.jpg` | Half-width (2-up) | 84mm × 47mm | 2000×1125px |
| 13 | 10 – Kebab & Tandoor | Kebab & Tandoor | Tandoori Chicken - Full (₹699) | `tandoori-chicken-full.jpg` | Half-width (2-up) | 84mm × 47mm | 2000×1125px |
| 14 | 11 – Sizzlers & Veg Main Course | Sizzlers | Smoky Chicken Sizzler (₹499) | `smoky-chicken-sizzler.jpg` | Full-width (1-up) | 178mm × 100mm | 3000×1688px |
| 15 | 12 – Non-Veg Main Course | Non-Veg Main Course | Butter Chicken ⭐ (₹329) | `butter-chicken.jpg` | Half-width (2-up) | 84mm × 47mm | 2000×1125px |
| 16 | 12 – Non-Veg Main Course | Non-Veg Main Course | Slow-Cooked Mutton Curry ⭐ (₹429) | `mutton-curry.jpg` | Half-width (2-up) | 84mm × 47mm | 2000×1125px |
| 17 | 14 – Rice & Biryani | Rice & Biryani | Chicken Dum Biryani Signature ⭐ (₹329) | `chicken-dum-biryani.jpg` | Full-width (1-up) | 178mm × 100mm | 3000×1688px |

**Rules that make an image "fit" the design, not just look good:**

- **Always generate at 16:9** (e.g. 2000×1125, or 3000×1688) — never square or portrait. The
  slot crops with `object-fit: cover`, so a wrong ratio gets cropped unpredictably.
- **Keep the dish centered with even margin on all sides** — the slot may crop a few % off any
  edge depending on the final screen/print size, so don't place the dish flush against one edge.
- **Leave calm, low-detail space in the top-left or top-right corner** on full-width (1-up)
  images only — that's the area most likely to sit near the category header above it.
- Pages 13, 15 and 16 (Breads, Salads & Papad, Beverages & Add-Ons) have **no photo slots by
  design** — icon-led, text-only pages — so no images are needed for those.

## 5. Per-Dish Prompts (17 photo slots, mapped to `menu/index.html`)

Each entry = filename to save as → the dish-specific line to append after Section 2's master
template (and before Section 3's "Avoid:" line). Always add the aspect ratio / resolution from
the Section 4 table into the prompt too (e.g. "16:9 aspect ratio, 3000x1688px").

### Page 3 — Breakfast
- **`healthy-breakfast-hero.jpg`** (Healthy Breakfast, slot 1)
  *"Paneer Stuffed Chilla: two golden moong-dal chillas filled with lightly spiced paneer,
  folded and plated with a small bowl of fresh curd and a wedge of lemon, top-down flat lay."*
- **`protein-breakfast-hero.jpg`** (Protein Breakfast, slot 2)
  *"Egg & Chicken Protein Breakfast: three eggs cooked sunny-side/scrambled, sliced grilled
  chicken breast, a side of sautéed mixed vegetables, and one piece of toast, 45-degree angle."*

### Page 4 — Desi Breakfast & Eggs
- **`desi-favourites-hero.jpg`** (Classic Chole Bhature)
  *"Classic Chole Bhature: a bowl of spiced chickpea curry with a single large fluffy fried
  bhature leaning against the bowl, garnished with onion rings and a lemon wedge, 45-degree
  angle, warm morning light."*

### Page 5 — Protein Lab
- **`protein-bowl-paneer.jpg`** (Paneer Power Bowl ⭐)
  *"Paneer Power Bowl: cubed grilled paneer, steamed rice, fresh mixed salad vegetables and a
  light dressing drizzle, arranged in a wide shallow bowl, top-down flat lay."*
- **`protein-bowl-chicken.jpg`** (Grilled Chicken Power Bowl ⭐)
  *"Grilled Chicken Power Bowl: sliced grilled chicken breast, steamed rice, fresh salad
  vegetables and a light dressing drizzle, wide shallow bowl, top-down flat lay."*

### Page 6 — Shakes, Smoothies & Healthy Drinks
- **`cold-coffee-whey-shake.jpg`** (Cold Coffee Whey Shake ⭐)
  *"Cold Coffee Whey Shake: a tall glass of chilled creamy cold coffee with a thin layer of
  froth on top, condensation droplets on the glass, a straw, on a wooden counter, side-on
  angle with soft daylight."*

### Page 7 — Soups & Veg Starters
- **`veg-manchow-soup.jpg`** (Veg Manchow Soup)
  *"Veg Manchow Soup: a bowl of spiced vegetable soup with visible thin fried noodles on top and
  finely chopped spring onion garnish, gentle steam rising, top-down angle."*
- **`paneer-tikka-hero.jpg`** (Paneer Tikka - 8 Pc ⭐)
  *"Paneer Tikka: 8 skewered pieces of tandoor-charred paneer with visible light char marks,
  bell pepper and onion between pieces, served on a black skillet with mint chutney and a lemon
  wedge, 45-degree angle."*

### Page 8 — Non-Veg Starters & Crispy Chicken
- **`chicken-lollipop.jpg`** (Chicken Lollipop)
  *"Chicken Lollipop: six deep-fried chicken lollipops standing upright in a small steel cone
  stand, light red-orange coating, side dip of house sauce, 45-degree angle."*
- **`korean-crispy-chicken.jpg`** (Korean Crispy Chicken ⭐)
  *"Korean Crispy Chicken: crispy fried chicken pieces tossed in a glossy-but-not-oversaturated
  sweet-spicy Korean glaze, garnished with sesame seeds and chopped spring onion, plated on a
  dark plate, top-down angle."*

### Page 9 — Indo-Chinese
- **`chicken-hakka-noodles.jpg`** (Chicken Hakka Noodles)
  *"Chicken Hakka Noodles: wok-tossed noodles with visible shredded chicken, julienned
  vegetables, and a light char from the wok, twirled loosely on a plate, chopsticks resting to
  the side, 45-degree angle."*

### Page 10 — Kebab & Tandoor
- **`chicken-tikka-hero.jpg`** (Chicken Tikka - 8 Pc ⭐)
  *"Chicken Tikka: 8 skewered pieces of tandoor-charred boneless chicken with visible smoky char
  marks, served on a sizzling black skillet with onion rings, mint chutney and a lemon wedge,
  45-degree angle, visible steam."*
- **`tandoori-chicken-full.jpg`** (Tandoori Chicken - Full)
  *"Tandoori Chicken (Full): a whole tandoori chicken with classic red-orange marinade and char
  marks, plated on a large platter with onion rings, mint chutney, and lemon wedges, 45-degree
  angle."*

### Page 11 — Sizzlers & Veg Main Course
- **`smoky-chicken-sizzler.jpg`** (Smoky Chicken Sizzler)
  *"Smoky Chicken Sizzler: grilled chicken pieces, sautéed vegetables, rice, and fries on a
  cast-iron sizzler plate with visible rising smoke, wooden underplate, side-on angle with
  dramatic but natural lighting."*

### Page 12 — Non-Veg Main Course
- **`butter-chicken.jpg`** (Butter Chicken ⭐)
  *"Butter Chicken: tender chicken pieces in a rich orange-red creamy makhani gravy, a light
  cream swirl on top, fresh coriander leaf garnish, served in a copper-toned bowl, 45-degree
  angle."*
- **`mutton-curry.jpg`** (Slow-Cooked Mutton Curry ⭐)
  *"Slow-Cooked Mutton Curry: bone-in mutton pieces in a deep reddish-brown home-style gravy,
  whole spices visible, fresh coriander garnish, served in an earthen-toned bowl, 45-degree
  angle."*

### Page 14 — Rice & Biryani
- **`chicken-dum-biryani.jpg`** (Chicken Dum Biryani Signature ⭐)
  *"Chicken Dum Biryani: a mound of long-grain basmati rice with visible saffron streaks,
  chicken pieces peeking through, fried onions and mint leaf garnish, a small side bowl of raita
  and a boiled egg half beside it, top-down angle."*

---

## 6. Post-generation pass (recommended, keeps it from reading as AI)

- Slightly desaturate (-5 to -10%) and reduce contrast/clarity by a small amount — pure
  AI-generated images tend to be punchier than real restaurant photos.
- Add a very light film grain (3–5%) — real camera sensor noise is one of the fastest tells
  that separates a photo from a render.
- Crop/export at exactly **16:9** for every slot (both half-width and full-width — see Section 4;
  they're the same shape, only the printed size differs) to match the existing slots in
  `menu/index.html`.
- Do a final side-by-side check against the checklist in Section 3 before approving.

## 7. Delivery

Drop the finished files into `assets/food/` using the exact filenames above, and note in
your message which dishes are done — the corresponding `<div class="photo-slot">` in
`menu/index.html` will be swapped for `<img>` tags and the file committed to this branch.
