# Holiday Catalog 2026

A holiday wish list styled after an early-'80s department store Christmas catalog. Static HTML, no build step.

## Adding an item
1. Drop a photo in `img/` (WebP or JPG, ~1000px on the long side).
2. Edit the `<script type="application/json" id="catalog">` block in `index.html` and add an entry to `items`:

```json
{
  "id": "unique-slug", "section": "rpg", "catno": "27 B 4406",
  "title": "Item name", "maker": "Brand",
  "url": "https://shop.example/item",
  "img": "img/photo.webp", "fit": "cover",
  "caption": "Small italic caption on the photo",
  "price": 24.99, "currency": "USD", "unit": "",
  "blurb": "Catalog copy.",
  "info": "<b>Size:</b> details line",
  "shipwt": "Shpg. wt. 1 lb.",
  "note": "Optional red handwritten-style aside"
}
```

Optional fields: `was` (regular price, adds the green sale ribbon), `priceTo` + `fromLabel` (price ranges), `anyAmount` (gift cards), `approx`, `cta` (button text). `fit: "cover"` fills the panel with a scene photo; leave it off for cutouts/covers.

Sections live in the same block (`name`, `headline`, `style`: `light` | `caps` | `band`, `photo` backdrop color).
