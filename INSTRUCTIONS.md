# FilAm Fashion — Cowork Project Instructions

## Brand Overview

**FilAm Fashion** (filamfashion.com) is a Filipino American custom clothing brand and editorial style magazine. The brand sits at the intersection of Filipino textile heritage and contemporary American fashion — custom-made garments, never mass-produced.

**Tagline:** Custom clothing. Filipino heritage. American soul.

---

## Brand Identity

### Tone & Voice
- Luxury editorial — sophisticated but warm and culturally proud
- Think: *Vogue* meets the spirit of the Philippines
- Never corporate, never generic
- Celebrate Filipino culture explicitly and specifically — name the textiles, the regions, the traditions
- Use poetic, evocative language for fashion descriptions

### Color Palette
| Name    | Hex       | Usage                          |
|---------|-----------|--------------------------------|
| Gold    | `#C9A96E` | Primary accent, headings       |
| Deep    | `#0D0A07` | Background                     |
| Cream   | `#F5EFE6` | Body text                      |
| Bark    | `#2A1F14` | Section backgrounds            |
| Mist    | `#D4C5B0` | Secondary text                 |
| Magenta | `#c9558a` | Magazine accent, highlights    |
| Accent  | `#E8C547` | Hover states                   |

### Typography
| Font                | Role                        |
|---------------------|-----------------------------|
| Playfair Display    | Display headings, logo      |
| Cormorant Garamond  | Body copy, editorial text   |
| Space Mono          | Labels, metadata, UI text   |

---

## Project Files

| File                              | Description                                      |
|-----------------------------------|--------------------------------------------------|
| `filipino-american-fashion.html`  | Main website — hero, AI stylist, collections, magazine, philosophy sections |
| `filam.png`                       | Magazine cover — Spring/Summer 2024 Style Icons issue |
| `INSTRUCTIONS.md`                 | This file                                        |

All new pages, articles, and assets should be saved into `C:\code\FilAmFashion\`.

---

## Filipino Textile & Cultural References

Always draw on these when generating fashion content:

**Fabrics & Textiles**
- Piña — pineapple fibre silk, the most prestigious Filipino fabric
- Hablon — handloomed Iloilo weave, geometric and earthy
- Abaca — Manila hemp, strong and natural
- Jusi — lightweight silk-like fabric used in barongs
- Pineapple silk — sheer, delicate, formal

**Garments**
- Barong Tagalog — traditional Filipino men's formal shirt, embroidered, sheer
- Baro't Saya — traditional women's two-piece (blouse + skirt)
- Terno — formal gown with signature butterfly sleeves
- Kimona — casual women's blouse

**Cultural References**
- Regions: Iloilo, Pampanga, Taguig, Cebu, Cordillera
- Patterns: Banig (woven mat), T'nalak (T'boli weave), Malong
- Occasions: Fiesta, Debut (18th birthday), Bayanihan

---

## Website Structure

The main site (`filipino-american-fashion.html`) contains these sections in order:

1. **Nav** — Logo + links (Collections, AI Stylist, Magazine, Philosophy, Custom)
2. **Hero** — Full-height landing with brand statement
3. **AI Generator** — Style concept generator (calls Anthropic API)
4. **Collections** — SS25 garment grid (5 cards)
5. **Magazine** — Featured cover spread + 4-issue grid + subscribe strip
6. **Philosophy** — Brand story + 3 pillars
7. **Footer**

### Pages Still to Build
- `custom-order.html` — Custom clothing enquiry form
- `lookbook.html` — Editorial lookbook with AI-generated style descriptions
- `magazine/ss24.html` — Full Spring/Summer 2024 issue inner pages
- `magazine/fw24.html` — Fall/Winter 2024 issue
- `about.html` — Brand story and founder page
- `contact.html` — Contact and social links

---

## AI Stylist — How It Works

The AI Generator on the site calls the Anthropic API directly from the browser. It takes:
- **Garment type** (top, dress, jacket, barong, co-ord set, accessories)
- **Occasion** (everyday, formal, wedding, festival, professional)
- **Style tag** (Barong Modern, Streetwear Fusion, Formal Filipiniana, etc.)

And returns a 4–6 sentence editorial concept with fabric suggestion, silhouette, and colour palette.

> ⚠️ For production (live on filamfashion.com), the API call must move to a serverless backend function (e.g. a Vercel API route) so the API key is not exposed in the browser.

---

## Common Cowork Tasks

Use these as starting prompts when opening a new task:

### Content Generation
- *"Write 3 editorial fashion articles for the SS24 magazine issue. Each should be 300–400 words, drawn from Filipino textile heritage, in the FilAm Fashion brand voice. Save each as a separate HTML file in the magazine/ subfolder."*
- *"Generate 6 product descriptions for the Collections section — one for each garment type. Use piña, hablon, or abaca references. Format as JSON so they can be loaded into the site."*

### Site Development
- *"Create a custom-order.html page matching the existing site styles. Include a form with fields for: name, email, garment type, occasion, measurements, and a free-text style notes field. Link it from the nav Custom button."*
- *"Build a lookbook.html page with a full-bleed editorial grid layout. Include 6 look slots with AI-generated style descriptions for each."*

### Magazine
- *"Create an inner magazine page (magazine/ss24.html) for the Spring/Summer 2024 Style Icons issue. Include the cover image, a lead editorial, and the 5 headline articles as full pieces."*

### Maintenance
- *"Review filipino-american-fashion.html and update the nav to include any new pages that have been created in this folder."*
- *"Check all internal links across all HTML files in this folder and fix any broken ones."*

---

## Deployment

The site will be hosted on **filamfashion.com** via **Vercel**.

When ready to deploy:
1. Push `C:\code\FilAmFashion\` to a GitHub repository
2. Connect the repo to Vercel at vercel.com
3. Point filamfashion.com DNS to Vercel's nameservers
4. Add a Vercel serverless function (`/api/generate.js`) to handle the Anthropic API calls securely

---

## Notes

- The magazine cover (`filam.png`) features two children in traditional Filipino formal wear — this is the heart of the brand's "Next Generation" identity. Treat it with pride.
- All garments referenced on the site are intended to be **custom made to order** — nothing off-the-shelf.
- The brand voice should always feel like it belongs on a glossy page, not a product listing.
