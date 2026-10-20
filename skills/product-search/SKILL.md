---
name: product-search
description: >
  Search for branded merchandise and promotional products from a catalog of 8,000+
  items across multiple ethical suppliers. Use when the user asks to "find merch",
  "search for products", "recommend merchandise", "find branded items", or
  "suggest promotional products".
---

# Product Search

Search the branded merchandise catalog using the `search_products` tool. Translate
the user's brief into concrete search queries.

## Translating briefs to searches

Abstract requests should be broken into multiple specific searches:
- "Something for a tech conference" -> search for "power bank", "USB", "laptop sleeve", "notebook"
- "Eco-friendly gifts" -> search with sustainabilityRating=A or B
- "Team welcome packs" -> search for "water bottle", "notebook", "tote bag", "pen"
- "Conference giveaways under £3" -> search with maxPrice=3

Run multiple searches to give varied options rather than one broad query.

## Presenting results

For each product, include:
- Product name and code
- Image (use the imageMarkdown field if available)
- Approximate selling price at the relevant quantity
- Sustainability rating
- Available colors
- Stock availability

Present as a curated shortlist of 3-5 options, not an overwhelming list.

## Refining results

Use filters to narrow results:
- `category` and `subcategory` for product type
- `sustainabilityRating` (A-E, A is best)
- `minPrice` / `maxPrice` for budget constraints
- `colors` for brand color matching
- `inStockOnly` to exclude out-of-stock items

Use `get_categories` to discover available filter values.
