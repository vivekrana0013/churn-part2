# Customer Churn Intelligence Capstone

A comprehensive D2C customer churn analysis and retention strategy project, featuring RFM segmentation with behavioral signals and actionable business insights.

## 📁 Project Structure

```
churn/
├── data/                          # Raw data files
│   ├── customers.csv              # Customer master data
│   ├── orders.csv                 # Transaction history
│   ├── support_tickets.csv        # Customer support interactions
│   ├── web_events_snapshot.csv    # Website activity
│   ├── churn_labels.csv           # Target variable (churned/retained)
│   ├── intervention_history.csv   # Past intervention data
│   ├── rfm_modeling_snapshot.csv  # RFM scoring snapshot
│   └── README.md                  # Data documentation
│
└── part2/                         # RFM Segmentation & Retention Strategy
    ├── rfm_segmentation.ipynb     # Full segmentation analysis notebook
    ├── segments.csv               # Customer segment assignments
    ├── retention_strategy.md      # Per-segment retention actions & budget
    ├── manual_review_cases.md     # Decision rationale for edge cases
    ├── requirements.txt           # Python dependencies
    └── README.md                  # Part 2 documentation
```

## 🎯 Project Overview

This project implements a **customer retention strategy** using RFM (Recency, Frequency, Monetary) segmentation combined with behavioral signals:

- **RFM Analysis**: Segment customers by purchase patterns
- **Behavioral Enrichment**: Integrate support interactions, web engagement, and churn risk
- **Retention Strategy**: Targeted interventions with budget prioritization
- **Manual Review**: Decision documentation for ambiguous cases

## 🚀 Quick Start

### Prerequisites
- Python 3.7+
- Jupyter Notebook

### Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/vivekrana0013/churn-part2.git
   cd churn-part2
   ```

2. **Install dependencies**
   ```bash
   cd part2
   pip install -r requirements.txt
   ```

3. **Run the analysis**
   ```bash
   jupyter notebook part2/rfm_segmentation.ipynb
   ```

## 📊 Key Outputs

- **segments.csv**: Customer-to-segment mapping with RFM scores and behavioral signals
- **retention_strategy.md**: Actionable interventions per segment with budget allocation
- **manual_review_cases.md**: Documentation of edge cases and decision rationale

## 📝 Documentation

- [Part 2 README](part2/README.md) — Detailed segmentation methodology
- [Retention Strategy](part2/retention_strategy.md) — Intervention tactics & budget plan
- [Manual Review Cases](part2/manual_review_cases.md) — Edge case decisions with reasoning

## 📦 Dependencies

See [part2/requirements.txt](part2/requirements.txt) for full dependency list.

Main packages:
- `pandas` — Data manipulation
- `scikit-learn` — RFM scoring
- `jupyter` — Interactive notebook environment

## 🔗 Repository

- **GitHub**: [vivekrana0013/churn-part2](https://github.com/vivekrana0013/churn-part2)

---

**Last Updated**: May 20, 2026
