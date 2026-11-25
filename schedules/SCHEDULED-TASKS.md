# Scheduled tasks for NoN Agent OS

Create each one as a **cloud scheduled task** in Claude Code: claude.ai/code/routines, then New. Pick this repo, set the time, and paste the prompt exactly as written. Times are India time (IST). Turn on notifications so the reports reach your phone.

Every prompt is complete on its own, because each run starts fresh and knows only what is in this repo.

---

## 1. Weekly competitor scan: Monday 8:40 am

```
Follow CLAUDE.md. Run the competitor-tracker skill for NoN.
Competitors: Scrubsy (main foam competitor), plus any others named in brand-brain/03-positioning-and-voice.csv. Also check the categories NoN sells in: mandir/brass/silver cleaners, bathroom and tap cleaners, kitchen foam/degreaser, car interior foam, sneaker cleaner.
Check their public websites, Amazon/Flipkart listings and the Meta Ad Library (India) for new products, prices, offers, bundles and ad angles since the last report in reports/.
Write reports/<today>-competitor-tracker.md with a change log, a price and offer comparison against NoN's current prices (P- and O- records), and 3 positioning opportunities that respect brand-brain/05-claims-rights-policies.csv.
Draft only. Do not contact anyone.
```

## 2. Weekly ads review: Monday 9:10 am (only while Meta ads are running)

```
Follow CLAUDE.md. Run the performance-marketing skill for NoN.
Use the newest Meta export in inputs/meta-ads/ and the newest ShopDeck export in inputs/shopdeck-orders/. Say the date of each. If the newest Meta file is older than 10 days, say "no new ads data" and stop after one paragraph.
For each ad set and ad: spend, purchases, cost per purchase, add-to-carts, and the money left for ads per order at the product's price (O- records; formula in CLAUDE.md).
Apply the test rules from the latest creative-strategist report:
- pause an ad after Rs 300 spent with no add-to-cart;
- scale only when cost per purchase is at or under that kit's ad ceiling over 3+ purchases.
Write reports/<today>-performance-marketing.md with a pause / keep / scale table for Ashutosh to approve. Do not change anything in Ads Manager.
```

## 3. Weekly plan for Ashutosh: Monday 10:20 am

```
Follow CLAUDE.md. Run the operator skill for NoN.
Read every report in reports/ from the last 8 days, plus brand-brain/06-growth-learnings.csv and the open "decisions needed" lists in earlier reports.
Write reports/<today>-operator.md with:
1. the top 3 actions for this week, each with its owner, the approval needed and the agent that drafts it;
2. decisions still waiting on Ashutosh, oldest first;
3. inputs missing, and who should upload them;
4. which on-request agents should be run this week (creative-strategist, 10roas-static-ad-generator, product-page-merchandising, winning-offers-bundles, landing-pages-cro, ugc-video), with a one-line reason each.
Put the 5-line summary at the very top so it can be read on a phone.
```

## 4. Monthly SEO check: 1st of the month, 9:40 am

```
Follow CLAUDE.md. Run the seo-geo skill for two sites: getnon.in (NoN, ShopDeck store) and innovachem.in (InnovaChem B2B).
Crawl the public pages you can reach. Check:
- titles, meta descriptions, headings and duplicate pages;
- product page copy against the label facts in brand-brain/01-product-and-sku-truth.csv;
- structured data, image alt text, internal links, page speed signals;
- how each site appears in AI answers for 5 buyer questions per site.
Compare against the last seo-geo report.
Write reports/<today>-seo-geo.md with fixes ranked by impact. For getnon.in, write each fix as an exact ShopDeck field change. For innovachem.in, write it as a code or content change.
If Google Search Console data is in inputs/other/, use it; if not, list it as a missing input.
Do not change either site.
```

## 5. Monthly profit check: 2nd of the month, 9:40 am

```
Follow CLAUDE.md. Run the profit-attribution-growth skill for NoN.
Use every ShopDeck export in inputs/shopdeck-orders/ for last month and the Meta exports in inputs/meta-ads/.
Report:
- orders, revenue and average order value;
- units by SKU and kit;
- profit per order after GST, product cost (O- records), Rs 100 delivery and Rs 30 commission;
- ad spend and cost per purchase;
- which products and kits met the 20% floor.
Write reports/<today>-profit-attribution-growth.md and propose any updates to brand-brain/06-growth-learnings.csv as a pull request.
```

## 6. Monthly customer voice: 3rd of the month, 9:40 am

```
Follow CLAUDE.md. Run the customer-voice-objection skill for NoN.
Use brand-brain/02-audience-and-voc.csv and any new files in inputs/reviews-and-chats/. Remove names and phone numbers.
Find the top themes, objections and exact customer phrases by product category, and what changed since last month.
Write reports/<today>-customer-voice-objection.md and propose new A- records for brand-brain/02-audience-and-voc.csv as a pull request.
Never put reviewer names or quotes into ad copy; mark every quote "site use only" unless permission is recorded (C-015, C-025).
```

## 7. Monthly repeat-purchase check: 4th of the month, 9:40 am (once there are 3 months of orders)

```
Follow CLAUDE.md. Run the repeat-purchase-ltv skill for NoN.
Use all ShopDeck exports in inputs/shopdeck-orders/. Use anonymised customer IDs only.
Report:
- repeat rate and time to second order;
- which first products lead to repeat orders;
- refill timing by product.
Draft 3 WhatsApp or email reorder messages for Ashutosh to approve.
Write reports/<today>-repeat-purchase-ltv.md. Do not send anything.
```

---

## Agents you start by hand (when the weekly plan says so)

Open Claude Code on this repo, or a chat in the "Ecom agents for NON" Project, and type for example:

- `Follow CLAUDE.md and run the creative-strategist skill for <product/category>.`
- `Follow CLAUDE.md and run the 10roas-static-ad-generator skill on the clear concepts in the latest creative-strategist report.`
- `Follow CLAUDE.md and run the product-page-merchandising skill for <product>.`

The other on-request agents work the same way: winning-offers-bundles, landing-pages-cro, ugc-video, creator-affiliate-growth, email-sms-whatsapp-recovery and customer-care.
