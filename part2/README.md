# Part 2 — RFM Segmentation & Retention Strategy

## D2C Customer Churn Intelligence Capstone

This repository contains RFM-based customer segmentation, enriched with behavioural signals, and a detailed retention strategy with budget prioritisation.

---

## Repository Structure

```
part2/
├── rfm_segmentation.ipynb     # Full segmentation notebook
├── segments.csv               # Customer segment assignments with all signals
├── retention_strategy.md      # Per-segment retention actions + budget plan
├── manual_review_cases.md     # 10 ambiguous customer decisions with reasoning
├── requirements.txt
└── README.md
```

---

## Dataset Setup

Place the dataset CSVs in a `data/` folder one level above this repo:

```
data/
├── customers.csv
├── orders.csv
├── support_tickets.csv
├── web_events_snapshot.csv
├── churn_labels.csv
└── intervention_history.csv
```

Change `DATA_DIR` in Cell 2 of the notebook if your path differs.

---

## Setup & Run

```bash
python3 -m venv venv && source venv/bin/activate
pip install -r requirements.txt
jupyter notebook rfm_segmentation.ipynb
```

---

## Segmentation Approach

### RFM Scores (Quintile 1–5)
| Score | Dimension | 5 = Best |
|---|---|---|
| R | Recency (days since last order) | Most recent |
| F | Frequency (orders in 180d) | Most orders |
| M | Monetary (INR spend in 180d) | Highest spend |

### Additional Signals
1. **Support tickets** — count, negative sentiment rate, reopened tickets
2. **Return rate** — proportion of orders returned
3. **Discount usage** — average discount % across orders
4. **Web activity** — sessions, last visit days ago, campaign clicks

---

## Segments (8 segments across 2,400 customers)

| Segment | Count | Churn Rate | Avg Recency | Avg Monetary |
|---|---|---|---|---|
| Champions | 344 | 10.5% | 21 days | ₹4,916 |
| Loyal Customers | 421 | 24.0% | 45 days | ₹3,354 |
| New Customers | 213 | 22.5% | 24 days | ₹793 |
| Needs Nurturing | 451 | 40.1% | 51 days | ₹1,116 |
| Discount Sensitive | 88 | 58.0% | 83 days | ₹596 |
| High-Value but Unhappy | 198 | 73.7% | 154 days | ₹4,456 |
| At Risk | 623 | 81.5% | 167 days | ₹2,202 |
| Dormant | 62 | 90.3% | 219 days | ₹505 |

---

## Key Outputs

| File | Description |
|---|---|
| `segments.csv` | customer_id, segment_name, RFM scores, support/web signals |
| `retention_strategy.md` | Per-segment behaviour, retention action, budget breakdown |
| `manual_review_cases.md` | 10 customer IDs with ambiguous decisions and reasoning |

---

## Budget Summary (₹50,000 campaign budget)

| Priority | Segment | Budget |
|---|---|---|
| 1 | At Risk | ₹18,000 |
| 2 | High-Value but Unhappy | ₹12,000 |
| 3 | Loyal Customers | ₹7,000 |
| 4 | New Customers | ₹6,000 |
| 5 | Needs Nurturing | ₹5,000 |
| 6 | Champions | ₹1,500 |
| 7 | Discount Sensitive | ₹500 |
| 8 | Dormant | Automated only |
