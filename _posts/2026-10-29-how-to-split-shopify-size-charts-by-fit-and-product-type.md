---
layout: post
title: "How to Split Shopify Size Charts by Fit and Product Type"
description: "Use fit and product logic to decide when Shopify products need separate size charts, then assign each chart without creating catalog maintenance work."
date: 2026-10-29 04:31:00 +0000
categories: [tools, how-to]
tags: [shopify, size-charts, apparel, merchandising]
canonical_url: ""
image: "/assets/img/posts/2026-10-29-how-to-split-shopify-size-charts-by-fit-and-product-type/cover-9c463f6b8be3.webp"
---

A collection is not a size system. If a Shopify collection contains cropped tees, relaxed tees, fitted base layers, and heavy overshirts, one generic table turns into an expensive guess. The labels may run from XS to XL across every product, but the measurement logic has changed.

That is the moment to split the chart—not when a product is merely a new colour, and not because the catalog feels untidy. The useful rule is simpler: create a separate chart when the shopper needs different measurements, different fit guidance, or a different way to interpret the same measurements.

[Supra Size Chart](https://supra-size-chart.sktch.io/) is built for this exact catalog task. It keeps charts and measurement guides central, then places the right one on each product through Shopify rules instead of asking a merchandiser to paste a table into every description. Here is a practical way to decide the splits before your assortment gets larger.

## Start with the measurement promise

Before opening a spreadsheet, take a sample from each product family and ask one question: **would the same set of measurements let a shopper make a confident choice on both products?**

A regular unisex tee and that tee in three colours probably share a chart. A slim ribbed tee and a boxy heavyweight tee usually do not. Their chest ease, body length, intended silhouette, and the meaning of “size up” differ—even if their size labels match.

Make a short working list for each family:

- garment type: tee, shirt, trouser, jacket, dress, footwear, or accessory
- intended fit: slim, regular, relaxed, oversized, compression, or adjustable
- measurement set: for example chest and length for a tee; waist, rise, inseam, and leg opening for trousers
- measurement basis: garment flat measurements, body measurements, or both
- shopper instruction: true-to-size, choose based on a body measurement, size up for layering, and so on

The distinction between [body and garment measurements](https://supra-size-chart.sktch.io/blog/body-vs-garment-measurements) matters here. A body-based guide cannot safely inherit a garment-based table just because both show centimetres. If the promise changes, split the chart.

![Garment fit cards sorted into two product groups on a workbench](/assets/img/posts/2026-10-29-how-to-split-shopify-size-charts-by-fit-and-product-type/image-01-119b7e1c2701.webp)

## Split on fit or construction—not colour and copy

There are two bad extremes: one universal chart for everything, or a unique chart for every SKU. Both create work without giving shoppers better information.

Use one shared chart when products have the same pattern block, grading, fit intent, and useful measurement columns. Colourways, a new product title, or a photo refresh are not reasons to clone it.

Create a separate chart when one of these changes:

1. **Fit intent changes.** A relaxed fit needs different guidance from a fitted one, even when the chest measurement is similar.
2. **Construction changes.** A jacket with lining and layer allowance needs a different decision process from a single-layer tee.
3. **The measurement columns change.** Adding sleeve length or torso length is a signal that this is a new sizing job.
4. **The shopper is measuring something different.** Foot length, bra band, ring circumference, and trouser inseam should not be forced into an apparel template.
5. **A region or vendor uses a genuinely different spec.** Do not hide a different grading system behind the same chart title.

For a clean test, put two candidate products side by side. If you would explain their measurements differently in a support reply, they deserve separate charts. A [garment measurement guide](https://how-to.the-lean-ecommerce.com/2026/10/24/how-to-build-a-garment-measurement-guide-for-shopify-size-charts/) is a useful companion: it keeps the names of the measurement points consistent once the groups are decided.

## Build a small chart map before making rules

Turn that working list into a chart map. It can be a plain spreadsheet with four columns: chart name, products included, assignment signal, and exception. For example:

| Chart | Products included | Assignment signal | Exception |
| --- | --- | --- | --- |
| Core regular tee | Same pattern in all colours | Product type: T-shirt | Exclude cropped fit |
| Relaxed overshirt | Overshirts with layer allowance | Collection: Overshirts | None |
| Slim base layer | Fitted thermal tops | Tag: fit-slim | Separate body guide |

The point is not to invent clever names. It is to give each chart one defensible job. If a product has two competing rows in the map, resolve the merchandising decision first; do not let the product page become the place where ambiguity leaks out.

In Supra Size Chart, create the tables in the spreadsheet-style editor, attach a reusable labelled measurement guide where it helps, then target the group with a product, collection, product type, vendor, or tag rule. The app’s [rule-based assignment approach](https://supra-size-chart.sktch.io/blog/size-chart-assignment-rules-at-scale) means a later product added to that collection can inherit the correct chart without another description edit. Its most-specific rule wins, with a store-wide default below it.

![Physical product routing board for assigning size charts by product group](/assets/img/posts/2026-10-29-how-to-split-shopify-size-charts-by-fit-and-product-type/image-02-e717c36e5de7.webp)

## Make exceptions visible and deliberate

Exceptions are normal: a one-off collab, a petite cut, a different supplier batch, or a bundle with mixed components. The mistake is encoding them in a vague product title and hoping the next person notices.

Choose one controlled signal for exceptions—a tag such as `fit-slim`, a product-level rule, or a dedicated collection—and document it in the chart map. This keeps the catalog searchable and prevents accidental coverage by a broader collection rule. If you have many vendor spec sheets, the app can also import and export chart data as CSV or JSON, which makes a review outside the app less fragile.

Do not use the exception as a reason to multiply display patterns. Once the chart is right, choose whether it is inline, in an accordion, or behind a modal based on the product-page reading job. The tradeoffs in [this display-layout guide](https://supra-size-chart.sktch.io/blog/size-chart-display-inline-accordion-modal) are useful; on a dense apparel page, an accordion may preserve scanning space, while a measurement-heavy product may need an inline table.

## Test the assigned chart on the actual product page

A correct rule can still produce a poor shopper experience. Test one product from every chart group on desktop and mobile before you roll it across a collection. Check that:

- the right chart appears after a collection or tag change
- the size labels and measurement notes match the product’s fit promise
- the guide shows the same measurement points named in the table
- the metric/imperial toggle is useful for the audience you serve
- the chart is readable by keyboard, not only by a pointer
- the block’s placement does not bury essential fit advice below unrelated content

That keyboard check is easy to overlook. This [size-chart accessibility walkthrough](https://how-to-blog.gitlab.io/2026/10/25/how-to-make-shopify-size-charts-easier-to-navigate-with-a-keyboard/) makes a good final pass, and a [mobile-first product-details system](https://how-to.the-lean-ecommerce.com/2026/10/28/how-to-build-a-mobile-first-shopify-product-details-system/) helps keep the size decision near the information a small-screen shopper needs.

![Mobile product page size-chart quality check with garment and tape measure](/assets/img/posts/2026-10-29-how-to-split-shopify-size-charts-by-fit-and-product-type/image-03-526371539750.webp)

## Keep the system small enough to trust

The best size-chart setup is not the one with the most rules. It is the one a merchandiser can explain in a minute: this family shares this pattern and fit, so it gets this chart; this exception has a different measurement promise, so it gets another.

Start with the five or ten product families that generate the most size questions. Build a chart map, set the rules, and test the pages. Then install [Supra Size Chart from the Shopify App Store](https://apps.shopify.com/supra-size-chart) to keep the tables, reusable guides, and assignments in your own Shopify catalog. It is free, and its charts live in Shopify metaobjects with CSV and JSON export, so your sizing data stays portable.

A shopper should not have to decode your assortment to choose a size. Split charts where the fit logic changes, reuse them where it does not, and make every product page answer the same basic question clearly: what should I measure, and which size follows from it?
