# FabAlcohol site specification and use cases

## Product objective

FabAlcohol is positioned as a curated gateway to Taiwanese whisky and spirits for customers in Vietnam, initially focused on Ho Chi Minh City. The website is both a brand introduction and a compact product catalogue. It should feel like a finished premium retail presence even when a product requires a direct quotation.

## Primary audiences

1. Individual buyers discovering Taiwanese whisky.
2. Buyers choosing a bottle for a dinner, celebration, or gift.
3. Enthusiasts looking for a specific Taiwanese bottle.
4. Companies requesting gifts, group orders, or partnership discussions.

## Main use cases

### Discover the brand

A visitor lands on the hero, understands the Taiwan-to-Vietnam positioning, and sees FabAlcohol's promise: thoughtful curation, transparency, approachable advice, and direct contact through Zalo.

### Understand why Taiwan matters

The Taiwan section explains the effect of warm-climate maturation, the broader local spirits culture, and the principle of selecting by experience rather than volume.

### Browse the catalogue

The catalogue gives Kavalan Classic and Kavalan Distillery Select No. 1 the strongest visual treatment while allowing more products to be added later. Additional bottles remain in the same collection rather than being framed as a speculative future range.

### Evaluate a bottle quickly

Each catalogue entry shows:

- Name, origin, volume, and ABV.
- Concise flavour direction and use occasion.
- Suggested drinking style or pairing.
- A price or `Liên hệ báo giá` when no final retail price is published.

### Read the full bottle story

The product-story modal expands each bottle into four chapters:

1. History and origin.
2. Production method.
3. Why the flavours develop.
4. When and how to drink it.

The modal also links to the producer information used as an editorial source.

### Request personal advice

Visitors can ask for a recommendation based on taste, occasion, drinking style, or budget. Zalo is the primary conversion channel; the site has no checkout or contact form.

### Request gifting or partnership support

FabAlcohol presents corporate gifting, group orders, and partnerships as available services. The site does not describe them as a future roadmap.

### Switch language

Vietnamese is the default. The VI/EN control changes interface copy without loading another page. Product names and technical specifications stay consistent.

## Information architecture

1. Sticky navigation.
2. Hero and primary Zalo CTA.
3. Why Taiwan.
4. Product collection.
5. Why FabAlcohol.
6. About FabAlcohol.
7. Personal and business services.
8. FAQ accordion.
9. Zalo contact panel.
10. Responsible-drinking footer.

## Visual system

- Direction: premium, editorial, dark Taiwanese identity.
- Core colours: charcoal black, warm ivory, oxidised red, muted gold.
- Display typography: DM Serif Display and Noto Serif.
- Body typography: Be Vietnam Pro.
- Product priority: large bottle photography, generous spacing, minimal catalogue density.
- Mobile behaviour: stacked content, collapsible navigation, single-column product stories.

## Interaction inventory

- Sticky header with anchor navigation.
- Responsive mobile menu.
- Vietnamese/English switcher using `data-vi` and `data-en` attributes.
- FAQ accordion.
- Product-story modal with Escape and close-button support.
- Scroll reveal animation.
- Zalo topic shortcuts; these require the official Zalo destination to be supplied.

## Content and data model

To add a product, create a catalogue card with a unique `data-product` key, then add the matching entry to the `storyProducts` object in `index.html`. Each story entry contains:

- `name`
- `index`
- `image`
- `specs`
- `source` label and URL
- Vietnamese and English `deck`, `history`, `craft`, `flavour`, and `serve`

Use `data-vi` and `data-en` on visible elements that must change language. Never invent a price or availability state; use `Liên hệ báo giá` until confirmed.

## Current constraints

- No ecommerce checkout.
- No customer form.
- No age gate.
- No inventory counts.
- No testimonials.
- No final logistics promise unless it has been operationally confirmed.
- Footer includes compact 18+ and responsible-drinking notices.

## Acceptance checklist for a rebuild

- Opens without an internet connection.
- Every local image loads.
- Local fonts load from `assets/fonts`.
- No horizontal overflow at common desktop and mobile widths.
- VI and EN both update all visible interface copy.
- FAQ items open and close.
- Every product button opens the correct story.
- Escape and the close button dismiss the modal.
- Navigation anchors reach the correct sections.
- The official Zalo link is tested before launch.
- Product prices, availability, and delivery language are reviewed before launch.

