# Run brief: Agent 04 Creative Strategist, then Agent 05 Static Ad Generator (all categories)

Written 23 Nov 2026 so a fresh chat in this Project can run both agents without the earlier conversation. Facts below are summaries; the Brand Brain CSVs are the source of truth and carry the record IDs to cite.

## What to read first

1. `agents/00-shared-operating-contract.md`: evidence states, approval rule, output contract.
2. `agents/04-creative-strategist.md`: Agent 04 package (skill, playbooks, output template, scorecard).
3. `agents/05-10roas-static-ad-generator.md`: Agent 05 package.
4. Brand Brain, all of it:
   - `brand-brain/01-product-and-sku-truth.csv`: label facts for all 31 SKUs plus Brass. Cite P-ids. Records with status draft or contradicted are not usable as ad claims.
   - `brand-brain/02-audience-and-voc.csv`: 60 Amazon/Flipkart reviews (A-007 to A-066) and the theme summary (A-067).
   - `brand-brain/03-positioning-and-voice.csv`
   - `brand-brain/04-offers-and-economics.csv`: per-SKU costs (LIST-* records), kit economics (O-006, O-010), ad ceilings (O-009).
   - `brand-brain/05-claims-rights-policies.csv`: what may and may not be claimed (C-001 to C-032).
   - `brand-brain/06-growth-learnings.csv`: past Meta result (L-002) and the pricing finding (L-004).
5. `ads/meta-campaigns-2026-10-22_2026-11-20.csv`: the only past ad data.

## Scope for this run

Cover all six product categories (from the ShopDeck Category Architecture tab), not only the two kits:

| Category | SKUs (sheet names) |
| --- | --- |
| Bathroom & Toilet Care | Toilet Cleaner, Glass & Mirror Cleaner, Mould & Mildew Remover, Drain Cleaner & Opener, Tap & Faucet Cleaner, Bathroom Cleaner |
| Kitchen & Food Care | Fruit & Vegetable Wash, Kitchen Foam Cleaner, Dishwash Liquid, Kitchen Degreaser |
| Laundry & Fabric Care | Matic Liquid Detergent, Washing Machine & Appliance Descaler, Universal Stain Remover, Ink & Stain Remover, Fabric Coat |
| Pest Control & Personal Safety | Multipurpose Repellent, Lizard Repellent, Rat & Rodent Repellent, Ant Repellent, Pepper Spray Pack of 3 |
| Auto & Gear Maintenance | Rust Remover & Converter, Car AC Vent Cleaner, Car Foam Cleaner, Silicone Spray, Helmet Cleaner, Sneaker Foam Cleaner |
| Home Surface & Specialty Care | Mandir Cleaner, Silver Cleaner & Polish, Lemongrass Floor Cleaner, Multipurpose Foam Cleaner, Glycerine Hand Wash (+ Brass Cleaner, live in Mandir Care Trio) |

Kits and bundles to advertise rather than single bottles (singles cannot fund ads at current prices, L-004): Mandir Care Trio, NoN Bathroom Shine Kit, Kitchen Care Duo, Car Care Duo, Sneaker Care Kit / Twin Pack, Insect-Free Home Pack of 4, Green Switch Trio, Laundry & Machine Care Duo, and the 2-packs on getnon.in.

## Decisions and constraints already made

- Approver for ads, pages, discounts and refunds: Ashutosh (C-017). Agents draft only; nothing is published or spent.
- Ad budget: about Rs 10,000/month, only while ads convert. The first test plan was Rs 4,200 over 14 days, 2 ad sets at Rs 150/day, broad audience 25-55, Sales objective optimised for purchases, with UTMs.
- Margin floor 20% after product cost, GST (18% inside price), Rs 100 delivery and Rs 30 commission per order (O-001).
- Current prices do not fund ads: Mandir Trio at Rs 699 leaves -Rs 5 for ads, Bathroom Shine Kit at Rs 499 leaves -Rs 135. At Rs 849 they leave about Rs 97 and Rs 102. The repricing is proposed and NOT yet approved. Every concept must state the price it assumes and the ad ceiling at that price (formula: price/1.18 x 0.8 - cost - 130).
- Past Meta ads: AI-generated video to a lookalike audience, Rs 8,244 spend, 1 purchase (L-002). Do not repeat as is.
- Earlier creative strategy for the two kits (separate artifact): concepts M1 after-Diwali reel, M3 one-box static, B1 tap reel, B2 three-marks static; reserves M2, B3. Stop rule: pause after Rs 330 spent with no add-to-cart. Scale rule must now be at or below the kit's ad ceiling (about Rs 95 at Rs 849).
- Main foam competitor: Scrubsy. NoN's edge: mandir and metal care, ingredient honesty on the label.

## Claim guardrails for every category

- No "natural / plant-based / chemical-free / non-toxic" for the whole range (C-005, C-027). Mould Remover is chlorine based, Drain Cleaner is caustic, Rust Remover uses mineral acids, Ink Remover is a flammable solvent.
- No kids-safe or pet-safe claims (C-006); no gentle-on-skin claims (C-004).
- Repellents: no efficacy claims in ads until the CIB&RC question is answered (C-009, C-010). Concepts may be drafted but must be marked blocked for spend.
- Pepper Spray: check Meta ad policy before any ad (C-030).
- Fabric Coat: label ingredients are placeholder text; do not advertise (C-028).
- Lemongrass Floor Cleaner: no disinfectant claim (C-008).
- Reviews: may be shown on the site as "Reviews from Amazon and Flipkart"; never quote reviewers or use names in ads without written permission (C-015, C-025). Review themes may inspire angles.
- Bathroom Cleaner and Tap cleaner: "Not for marble or natural stone" (C-032).
- Brass idol before/after photo exists (C-024); reshoot needed in the same spot. Owner is reshooting product photos.
- Labels carry template MRP Rs 999, batch ASCF208 and phone XXXXX (C-021); do not show labels close-up in ads until fixed.

## Expected outputs

1. Agent 04: a concept matrix by category (2-3 distinct concepts per category, each with evidence IDs, awareness stage, hypothesis, disconfirming signal, assumed price and ad ceiling, and a blocked/clear status), an angle and hook map, production briefs (static vs reel), creative experiment cards, a learning register, and a test priority order across categories given the Rs 10,000/month budget.
2. Agent 05: for the concepts Agent 04 marks as clear and static, a static ad copy pack (hook, primary text, headline, CTA), a composition brief, image-generation prompts with forbidden changes, export names and sizes (1080x1350 and 1080x1920), and an asset and claim checklist.
3. Save both as Docs, and write a short summary to `claude/creative-run-YYYY-MM-DD.md` in the Project. Status of everything: draft, awaiting Ashutosh's approval.
