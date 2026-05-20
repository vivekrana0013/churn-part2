# Retention Strategy — D2C Churn Capstone Part 2

**Snapshot Date:** 2025-09-30  
**Total Customers Segmented:** 2,400  
**Segmentation Method:** RFM scoring (1–5 quintile ranks) + support tickets + return rate + web activity + discount usage  

---

## Segment Overview

| Segment | Count | Churn Rate | Avg Recency | Avg Monetary (INR) | Priority |
|---|---|---|---|---|---|
| Champions | 344 | 10.5% | 21 days | ₹4,916 | Protect |
| Loyal Customers | 421 | 24.0% | 45 days | ₹3,354 | Retain |
| New Customers | 213 | 22.5% | 24 days | ₹793 | Onboard |
| Needs Nurturing | 451 | 40.1% | 51 days | ₹1,116 | Re-engage |
| Discount Sensitive | 88 | 58.0% | 83 days | ₹596 | Monetise |
| High-Value but Unhappy | 198 | 73.7% | 154 days | ₹4,456 | Rescue |
| At Risk | 623 | 81.5% | 167 days | ₹2,202 | Urgently Retain |
| Dormant | 62 | 90.3% | 219 days | ₹505 | Win-back or Accept |

---

## Segmentation Logic

### RFM Scoring
Each customer is scored 1–5 on three dimensions using quintile ranking:
- **R (Recency):** 5 = ordered most recently; 1 = longest inactive
- **F (Frequency):** 5 = most orders in 180d; 1 = fewest
- **M (Monetary):** 5 = highest spend in 180d; 1 = lowest

### Additional Signals Layered In
1. **Support tickets** — ticket count, negative sentiment rate, reopened tickets
2. **Return rate** — proportion of orders returned in 180d
3. **Discount dependency** — average discount % across orders
4. **Web/app activity** — sessions in last 30d, last visit days ago
5. **Campaign engagement** — campaign clicks, email opens

---

## Segment Definitions & Retention Actions

---

### 1. Champions (344 customers | 10.5% churn)
**Behaviour:** R≥4, F≥4, M≥4. Ordered recently, frequently, and at high value. Low return rate, positive sentiment, regularly engaged on app.  
**Risk:** Low. These customers are the brand's most loyal advocates.  
**Retention Action:**
- Enrol in exclusive "Brand Ambassador" programme or top loyalty tier
- Early access to new product launches
- Personal thank-you communications (not mass email blasts)
- Referral programme — incentivise them to bring in customers like themselves
- Do NOT send discount offers — this cheapens their relationship with the brand

**Expected Business Value:** Protecting this segment from churning is worth more per customer than winning back dormant ones. Every churned Champion represents ~₹4,916 in lost recurring revenue.

---

### 2. Loyal Customers (421 customers | 24.0% churn)
**Behaviour:** R≥3, F≥3, RFM Total ≥10. Consistent buyers but not at the very top tier. Moderate spend, good sentiment.  
**Risk:** Low-medium. Their churn rate is 24%, meaning roughly 1 in 4 will lapse without attention.  
**Retention Action:**
- Loyalty tier upgrade prompts (e.g., "You're 2 orders away from Gold status")
- Personalised product recommendations based on purchase history
- Anniversary or milestone rewards (e.g., "1 year with us" offer)
- Subscription or bundle offer at modest discount (max 10–15%)

**Expected Business Value:** With ₹3,354 average monetary value and 421 customers, even saving 10% of at-risk churners in this segment saves ~₹141K in revenue.

---

### 3. New Customers (213 customers | 22.5% churn)
**Behaviour:** F≤1, recency ≤60 days. Still in the early lifecycle. Have purchased once, recently.  
**Risk:** Medium. The first 60–90 days are critical for LTV development.  
**Retention Action:**
- Week-1 welcome series: product education + how-to content
- Day-30 follow-up: "How was your first purchase?" personalised email
- Day-60 loyalty nudge: "Join our loyalty programme — free for first-timers"
- Category cross-sell: if first order was Skin Care, introduce Hair Care next
- Offer a second-purchase incentive (free shipping, not a deep discount)

**Expected Business Value:** Converting a new customer into a recurring buyer increases LTV from ₹793 (single order) to potentially ₹2,000+ over 6 months.

---

### 4. Needs Nurturing (451 customers | 40.1% churn)
**Behaviour:** Mid-tier RFM scores. Buy occasionally, not deeply engaged. Sessions are moderate, last visit ~51 days. Not in loyalty programme typically.  
**Risk:** Medium-high. 40% churn rate is above average. The largest single segment.  
**Retention Action:**
- Re-engagement email series with personalised content (not generic blasts)
- Loyalty programme onboarding — many of these customers are not enrolled
- Cart abandonment reminder nudges (average abandoned_carts > 0)
- Product education: show value beyond price to reduce discount dependency
- Behavioural triggers: if 21+ days since last visit, trigger a check-in

**Expected Business Value:** At 451 customers and a ₹1,116 average spend, reducing this segment's churn rate from 40% to 25% would retain approximately 68 customers and ~₹76K in revenue per cycle.

---

### 5. Discount Sensitive (88 customers | 58.0% churn)
**Behaviour:** Average discount ≥45%, moderate-low RFM. Have only bought during promotions. Recency averages 83 days.  
**Risk:** High. These customers have been trained to wait for deals and will lapse without one.  
**Retention Action:**
- Avoid deepening the discount habit — no further flat discounts
- Offer value-adds instead: free gift with purchase, loyalty points double-up
- Educate on product quality and efficacy to build non-price loyalty
- Test "buy 2, get free shipping" bundles — maintains engagement without eroding margin
- If no response to 2 value-based offers, exit this segment from active campaign spend

**Expected Business Value:** High caution. Over-investing in this segment risks training more customers to be discount-dependent. ROI threshold should be strictly enforced.

---

### 6. High-Value but Unhappy (198 customers | 73.7% churn)
**Behaviour:** M≥4 (avg monetary ₹4,456) but high ticket count (avg 3+), negative sentiment, or high return rate. These are big spenders who have had bad experiences.  
**Risk:** Very high. They have the money to come back — they just don't want to after bad interactions.  
**Retention Action:**
- **Immediate priority:** Personal outreach from a senior CX representative, not a bot
- Acknowledge specific past issues (damaged items, wrong items, refund delays)
- Offer a service recovery gift — not a discount, a genuine gesture (premium sample set, priority shipping on next order)
- Escalate unresolved support tickets within 24 hours
- Assign a named account manager or VIP support queue for this segment

**Expected Business Value:** This segment is the highest ROI rescue target. Each recovered customer represents ~₹4,456 in monetary value. Even a 20% save rate across 198 customers generates ~₹177K in recovered revenue.

---

### 7. At Risk (623 customers | 81.5% churn)
**Behaviour:** R≤2, some purchase history (F≥2 or M≥2). Have bought before but are going quiet. Avg recency 167 days. Largest segment at 623 customers.  
**Risk:** Critical. Over 80% churn rate — these customers are already disengaging.  
**Retention Action:**
- Time-sensitive win-back offer: "We miss you — here's free shipping + 15% off your next order (valid 14 days)"
- Highlight new launches or improvements relevant to their preferred category
- SMS/push notification if they have consented — break through email fatigue
- If no response in 30 days, move to Dormant and reduce campaign frequency

**Expected Business Value:** This is the largest at-risk pool. Saving even 15% of this group (93 customers × ₹2,202 avg) recovers ~₹205K. This should receive the largest absolute budget allocation among at-risk segments.

---

### 8. Dormant (62 customers | 90.3% churn)
**Behaviour:** Recency >150 days (avg 219 days), very low web engagement. Most haven't visited the site in 2+ months.  
**Risk:** Near-terminal. 90% churn rate indicates brand disengagement.  
**Retention Action:**
- Low-cost win-back attempt: single "We're still here" email with a strong product reason to return
- If no response within 30 days, suppress from all campaigns to reduce wasted spend
- Analyse exit reasons before attempting rescue — many may be lost to competitor or category exit

**Expected Business Value:** Low ROI. Budget cap of ₹40/customer maximum. Do not over-invest.

---

## Campaign Budget Prioritisation

**Assumed total budget per cycle:** ₹50,000

| Priority | Segment | Customers | Recommended Budget | Cost/Customer | Rationale |
|---|---|---|---|---|---|
| 1 | At Risk | 623 | ₹18,000 | ₹29 | Largest salvageable pool with meaningful monetary value |
| 2 | High-Value but Unhappy | 198 | ₹12,000 | ₹61 | Highest revenue-per-rescue; personal outreach justified |
| 3 | Loyal Customers | 421 | ₹7,000 | ₹17 | Protect recurring revenue; low cost to maintain |
| 4 | New Customers | 213 | ₹6,000 | ₹28 | Early lifecycle investment pays off over 6–12 months |
| 5 | Needs Nurturing | 451 | ₹5,000 | ₹11 | Large segment, low cost per touch via email automation |
| 6 | Champions | 344 | ₹1,500 | ₹4 | Minimal cost — recognition events, not discounts |
| 7 | Discount Sensitive | 88 | ₹500 | ₹6 | Test value-add approach; monitor ROI strictly |
| 8 | Dormant | 62 | ₹0* | — | Suppress; marginal ROI does not justify active spend |

*Dormant customers can receive a single automated email at near-zero marginal cost but should not receive paid campaign spend.

**Why At Risk gets the largest budget:** 623 customers × 81.5% churn × avg ₹2,202 monetary = approximately ₹1.1M in revenue at risk. Even a 15% save rate with a ₹18,000 investment produces a revenue-to-cost ratio of ~12x.

**Why High-Value but Unhappy gets priority over Loyal:** Their monetary value is ₹4,456 vs ₹3,354 and their churn rate is 3x higher. The rescue effort is harder but the revenue stakes justify the premium cost-per-customer.
