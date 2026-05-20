# Manual Review Cases — Ambiguous Retention Decisions

**10 customer IDs where the segment assignment is not straightforward and the retention decision requires judgment.**

---

## Case 1 — CUST00001
**Segment:** At Risk  
**Key Stats:** Recency=107 days | Frequency=6 orders | Monetary=₹2,955 | Tickets=2 | Avg Sentiment=+0.14 | Return Rate=16.7% | Sessions=1 | Last Visit=20 days ago | Churn=1

**Why it's ambiguous:** CUST00001 has 6 orders and ₹2,955 in lifetime spend — this is historically a solid customer. Their sentiment is slightly positive and return rate is moderate. However, their recency of 107 days combined with the dataset confirming they churned makes this a tricky case. Their last visit was only 20 days ago, meaning there is still digital engagement despite purchase inactivity.

**Decision:** Treat as "At Risk with rescue potential." The gap between digital engagement (still visiting) and purchase inactivity suggests a consideration barrier — possibly price, product-market fit drift, or a competitor trial. Recommended action: personalised email referencing their most purchased category with a time-limited free-shipping offer. Do not open with a discount — sentiment is neutral-positive, so brand perception is intact.

---

## Case 2 — CUST00042
**Segment:** High-Value but Unhappy  
**Key Stats:** Recency=87 days | Frequency=9 orders | Monetary=₹7,523 | Tickets=6 | Avg Sentiment=–0.46 | Return Rate=22.2% | Sessions=3 | Last Visit=14 days ago | Churn=0

**Why it's ambiguous:** This customer is the model's counter-example — they have negative sentiment, 6 support tickets, a 22% return rate, and still did NOT churn. They are clearly a high-value buyer despite being consistently dissatisfied. Assigning them "High-Value but Unhappy" is correct, but the retention action is nuanced: they don't need to be rescued — they need their experience improved.

**Decision:** Do not send a win-back campaign; they are not lost. Instead, assign to a VIP support queue immediately. Proactively audit their 6 tickets — identify the recurring issue type. If it's product quality (damaged_item, product_reaction), escalate to the product team. If it's logistics (late_delivery, wrong_item), escalate to fulfilment. A proactive service call ("We noticed a few issues with your recent orders — we'd like to make it right") can convert a retained-but-unhappy customer into a brand advocate.

---

## Case 3 — CUST00057
**Segment:** At Risk  
**Key Stats:** Recency=136 days | Frequency=2 orders | Monetary=₹2,510 | Tickets=0 | Avg Sentiment=0.0 | Sessions=7 | Last Visit=29 days ago | Churn=1

**Why it's ambiguous:** Zero tickets and a strong 7 sessions in the last 30 days — this customer is actively browsing but not buying. Their 2 orders were high-value (₹1,255 per order on average), and they have raised no complaints. The silence is confusing — no dissatisfaction signal, yet they churned.

**Decision:** This is a price/consideration customer. They are in a comparison or evaluation phase. Recommended action: retargeting on the channel they were acquired from (check acquisition_channel in customers.csv) with a "Here's what's new" product launch message. A cart-abandonment flow may also apply — check if abandoned_carts_30d > 0. Do not discount — there is no complaint to overcome; the barrier is likely consideration, not dissatisfaction.

---

## Case 4 — CUST00068
**Segment:** At Risk  
**Key Stats:** Recency=346 days | Frequency=3 orders | Monetary=₹2,123 | Tickets=1 | Avg Sentiment=–1.0 | Return Rate=33.3% | Sessions=5 | Last Visit=60 days ago | Churn=1

**Why it's ambiguous:** 346 days since last order — this customer is closer to Dormant than At Risk. But they have 3 orders, ₹2,123 in spend, and are still browsing (5 sessions, though last visit was 60 days ago). Their single ticket had a sentiment of –1.0 (maximally negative). 

**Decision:** Borderline Dormant/At Risk. The negative ticket is the critical clue — something went very wrong once, and they never returned. This requires a service-recovery framing: "We know your last experience wasn't great. We've made some changes." A single targeted email acknowledging the issue category (without revealing PII of the ticket) with a free-return-guarantee on next order could re-open the relationship. Budget cap: ₹40 maximum. If no response in 14 days, move to suppress list.

---

## Case 5 — CUST00025
**Segment:** High-Value but Unhappy  
**Key Stats:** Recency=165 days | Frequency=7 orders | Monetary=₹4,868 | Tickets=3 | Avg Sentiment=–0.23 | Return Rate=0.0% | Sessions=11 | Last Visit=29 days ago | Churn=1

**Why it's ambiguous:** 7 orders and nearly ₹5,000 spend — clearly an engaged historical buyer. Zero return rate means they kept every product. Yet they have 3 tickets with negative sentiment and haven't ordered in 165 days, and they ultimately churned. The high sessions (11) with no purchase in 165 days is paradoxical.

**Decision:** The combination of high browsing, no returns, and negative support tickets points to a service trust breakdown rather than product dissatisfaction. They like the products — they're still looking. But something in the support interaction soured the relationship enough to stop buying. Recommended action: white-glove CX outreach, acknowledge the previous ticket history, offer a dedicated support contact for future orders. A premium product bundle (no discount, but a curated gift-with-purchase) is the right gesture here.

---

## Case 6 — CUST00072
**Segment:** At Risk  
**Key Stats:** Recency=90 days | Frequency=4 orders | Monetary=₹2,587 | Tickets=0 | Avg Sentiment=0.0 | Return Rate=0% | Sessions=7 | Last Visit=26 days ago | Churn=1

**Why it's ambiguous:** Near-clean customer — no tickets, no returns, 4 orders at ₹647 avg, actively browsing (7 sessions), last visited 26 days ago. Yet they churned. Nothing in the data explains why.

**Decision:** This is a "silent leaver" — they left without leaving a trace. This is the hardest case to crack. No negative signal to address. Recommended action: conduct a micro-survey ("We haven't seen you in a while — was there anything we could improve?") paired with a clean "here's what's new" message. The survey response will be more valuable than any single campaign. If they respond with a competitor mention or pricing concern, route to a specialist. If no response, suppress after 30 days.

---

## Case 7 — CUST00089
**Segment:** At Risk  
**Key Stats:** Recency=165 days | Frequency=2 orders | Monetary=₹2,825 | Tickets=0 | Return Rate=0% | Sessions=12 | Last Visit=31 days ago | Churn=1

**Why it's ambiguous:** Highest sessions count (12) among At Risk cases reviewed here, yet 165 days since their last order and confirmed churned. High browse-to-purchase gap is unusual.

**Decision:** Classic high-intent, low-conversion pattern. The customer has price sensitivity or comparison behaviour. With ₹1,412 avg order value, a "bundle and save" offer (buy 2 products at same total cost, positioned as convenience not discount) may convert. Alternatively, a loyalty tier pitch ("Join our Gold tier — free express delivery + exclusive member pricing") can create a structural incentive to purchase through this brand vs a competitor.

---

## Case 8 — CUST00020
**Segment:** High-Value but Unhappy  
**Key Stats:** Recency=368 days | Frequency=3 orders | Monetary=₹4,487 | Tickets=1 | Avg Sentiment=–0.95 | Return Rate=0% | Sessions=0 | Last Visit=60 days ago | Churn=1

**Why it's ambiguous:** 368 days since last order — this is functionally Dormant. But their monetary value (₹4,487) means a recovery attempt is worth considering. Zero sessions suggest they may have fully stopped engaging with the brand digitally.

**Decision:** Standard Dormant protocols apply — single win-back email maximum. However, given the ₹4,487 value, escalate to a phone outreach attempt if email is unopened within 7 days. The near-zero sentiment on their single ticket (–0.95) likely explains the departure. A CX manager should review that specific ticket before reaching out — the message must acknowledge the specific failure. Budget ceiling: ₹60 for this customer given the revenue upside.

---

## Case 9 — CUST00051
**Segment:** High-Value but Unhappy  
**Key Stats:** Recency=210 days | Frequency=4 orders | Monetary=₹4,444 | Tickets=2 | Avg Sentiment=–0.39 | Return Rate=0% | Avg Discount=35% | Sessions=6 | Last Visit=35 days ago | Churn=1

**Why it's ambiguous:** Four orders, ₹1,111 avg order value, 6 sessions, last visited 35 days ago — not fully disengaged. But 210 days without a purchase and 35% avg discount usage suggests this customer is both unhappy AND discount-dependent. Which problem do you solve first?

**Decision:** Address sentiment first, discount second. A satisfaction-focused outreach ("We noticed it's been a while — we'd love to hear your feedback, and we have some new products we think you'll love") with a modest value-add (free sample, not discount) is the right sequence. If they respond positively, introduce the loyalty programme as an alternative to one-off discounts. If they only engage with discount offers, flag as Discount Sensitive and adjust strategy accordingly.

---

## Case 10 — CUST00066
**Segment:** High-Value but Unhappy  
**Key Stats:** Recency=320 days | Frequency=5 orders | Monetary=₹4,598 | Tickets=1 | Avg Sentiment=–1.0 | Return Rate=0% | Sessions=11 | Last Visit=60 days ago | Churn=1

**Why it's ambiguous:** 5 orders and ₹4,598 spend — strong historical value. Still showing 11 sessions, but hasn't purchased in 320 days and visited 60 days ago. Single ticket with –1.0 sentiment is a red flag that aligns with the departure timing.

**Decision:** The –1.0 sentiment single ticket is almost certainly the inflection point. This customer had a serious negative experience and voted with their feet. However, 11 sessions suggest the brand still interests them. They are "interested but blocked." The intervention must be personal and empathetic: acknowledge the bad experience, show what has changed operationally, and offer a risk-free trial (easy return, dedicated support). Do not open with a discount — the relationship breakdown is emotional, not financial. Budget: up to ₹75 given ₹4,598 historical value.

---

## Summary of Manual Review Themes

| Theme | Cases | Implication |
|---|---|---|
| Still browsing, not buying | CUST00057, CUST00072, CUST00089, CUST00066 | Consideration gap — value messaging, not discount |
| Negative sentiment exit | CUST00068, CUST00020, CUST00010, CUST00066 | Service recovery before any commercial offer |
| Retained despite complaints | CUST00042 | Improve experience, don't risk disrupting loyalty |
| High value, silent leaver | CUST00072, CUST00089 | Survey-first, then personalised re-engagement |
| Discount-dependent + unhappy | CUST00051 | Sentiment fix first, then wean off discounts |
