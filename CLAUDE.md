# NoN Agent OS: rules for every Claude run in this repo

This repo runs the Ecom Agent OS v4 growth agents for **NoN (Nature or Nothing)**, sold on getnon.in, a ShopDeck store. It also covers SEO for **innovachem.in**. Both belong to InnovaChem Systems LLP. Owner and only approver: **Ashutosh**.

## Read before any task

1. This file.
2. `shared/02-SHARED-OPERATING-CONTRACT.md` and the other files in `shared/`: evidence states, approval and handoff rules.
3. The whole Brand Brain in `brand-brain/`:
   - `00-source-register.csv`: where each fact came from (SRC-*)
   - `01-product-and-sku-truth.csv`: label facts, sizes, prices and costs for all 31 SKUs plus the Brass Cleaner (P-*)
   - `02-audience-and-voc.csv`: segments and 60 Amazon/Flipkart reviews (A-*)
   - `03-positioning-and-voice.csv`: positioning and voice (V-*)
   - `04-offers-and-economics.csv`: margin floor, costs, kit economics, ad ceilings (O-*)
   - `05-claims-rights-policies.csv`: what may and may not be said (C-*)
   - `06-growth-learnings.csv`: past tests and decisions (L-*)
4. The newest file in `reports/` for the same agent, so each run builds on the last one.
5. The skill for the agent you are running, in `.claude/skills/<agent>/SKILL.md`. Paths inside a skill (inputs/, references/, outputs/, review/) are relative to that skill's folder.

## Hard rules

- **Draft only.** Never publish, send, spend, change ShopDeck, Meta Ads Manager, WhatsApp or any account, or contact anyone. Every external action needs Ashutosh's explicit approval at the time of the action (C-017).
- **No invented facts.** Every factual statement cites a Brand Brain record ID (P-, A-, V-, O-, C-, L-) or a file in `inputs/` with its date. Missing data is written as `missing`, not guessed.
- **Claim guardrails** (full list in `05-claims-rights-policies.csv`):
  - No "natural", "plant-based", "chemical-free" or "non-toxic" claims for the whole range (C-005, C-027).
  - No kids-safe or pet-safe claims (C-006), and no gentle-on-skin claims (C-004).
  - Repellent efficacy claims are blocked until the CIB&RC question is answered (C-009, C-010).
  - Fabric Coat is not to be advertised (C-028).
  - No Pepper Spray ads (C-030).
  - No disinfectant claim for the Floor Cleaner (C-008).
  - Reviewer names and quotes are not to be used in ads without written permission (C-015, C-025).
- **Economics:**
  - Prices include 18% GST.
  - The 20% margin floor is checked after product cost, Rs 100 delivery and Rs 30 commission per order (O-001).
  - Money left for ads per order = price / 1.18 x 0.8 - cost - 130.
  - Never propose a price above the printed or listed MRP (C-026).
- **Privacy:** order and chat exports may contain customer names and phone numbers. Never copy personal details into reports. Work with counts and anonymised quotes only.

## Where output goes

- Each run writes one report: `reports/YYYY-MM-DD-<agent-name>.md`. Use the agent's `outputs/output-template.md` sections, and start with a 5-line summary for Ashutosh.
- Proposed Brand Brain changes go in the report under "Proposed Brand Brain updates", plus a pull request on a branch named `claude/<agent>-YYYY-MM-DD`. Never commit straight to `main`. Ashutosh merges what he approves.
- End every report with three items: decisions needed from Ashutosh, missing inputs, and next run date.

## Where inputs come from

Ashutosh (or Priyanka) drops exports into `inputs/` and commits them:
- `inputs/shopdeck-orders/`: weekly ShopDeck order export, with names and phones removed
- `inputs/meta-ads/`: weekly Meta Ads Manager export, ad level, with spend, impressions, clicks, landing page views, add to cart, checkout and purchases
- `inputs/reviews-and-chats/`: reviews and WhatsApp chats, anonymised
- `inputs/other/`: anything else, named with its date

Always use the newest file and state its date in the report. If the needed input is older than 10 days, say so and run on what exists.
