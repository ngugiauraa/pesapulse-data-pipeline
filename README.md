# Day 1: API Customer Directory Pipeline

An internal automated pipeline designed for **Pesa Pulse** to safely download, normalize, validate, and chart customer directory datasets received via partner endpoints before executing regional marketing distributions.

## 🚀 Execution Guide

### 1. Installation Requirements
Ensure your workspace includes a Python 3.10+ execution framework and install the required library components:
```bash
pip install -r requirements.txt
```

### 2. Run the Engine
Execute the core script pipeline directly through your local shell environment:
```bash
python analysis.py
```
Upon execution, the terminal layer will establish synchronous telemetry hooks with the API, log schema profiles, execute validation sanity checks, and write tidy document assets into the local `output/` directory.

---

## 🛠️ Implementation Architecture

The framework splits responsibilities cleanly across specific processing layers:

* **Data Ingestion & Integrity Protection (Tasks 1 & 2):** Connects to the REST endpoint utilizing `requests` with a strict `timeout=10` threshold safety tripwire. Schema objects are structurally analyzed using an automated recursive object tree-walk loop to log data patterns cleanly.
* **Normalization & Key-Tie Sorting (Tasks 3, 4 & 5):** Deep nested variables (like coordinate coordinates) are isolated and transformed into native decimal floating-point data arrays. Primary indexing columns are updated to match strict template headers (`customer_id`). Aggregation operations execute using a tuple weight-factor string sort layout (`key=lambda item: (-item, item)`) to arrange equal-count items in a clean, alphabetical secondary arrangement automatically.
* **Pandas Assertion Cross-Checks & Exports (Tasks 6, 7 & 8):** Flat record sequences are loaded into a `pandas.DataFrame`. The script forces an alphabetical key-standardization check across target dictionaries before validating pure Python aggregation structures against Pandas `.value_counts()` calculations. Safe tabular assets map data parameters to `customer_count` rows before writing to index-free, machine-readable CSV files.

---

## 🔍 Data Discoveries & Strategy Insights

* **Perfect Audience Fragmentation:** Our market contains **10 total active records scattered uniformly across 10 separate unique cities**. Because regional population concentration is non-existent, marketing dollars should avoid localized physical ad campaigns (like billboards) and favor wider programmatic online distribution funnels.
* **Top-Level Domain Suffix Penetration:** Sorting the target customer mailing extensions isolates **.biz** as the leading Top-Level Domain extension (representing 40% of overall user volume across 4 profiles), pointing to a distinctly business-centric user base.
* **Visual Value Contrast Analysis:** Generating a traditional city bar chart outputs a completely flat line where every property equals a count of 1, rendering it useless for growth planners. Utilizing the `.png` breakdown for top-level email domains groups users into structural segments that teams can target right away.

---

## 📋 Underlying System Assumptions

* **Fallback Structural Metrics:** Missing geospatial values can default to generic coordinate boundaries of `0.0` without invalidating adjacent profile record arrays.
* **Domain Extraction Scope:** In compliance with template specifications, the field variable tracking `email_domain` targets the isolated terminal top-level domain suffix string element (e.g., parsing `biz` out of a user email).
* **Availability Thresholds:** Pipeline tasks assume the upstream server maintains structural schema tree configurations, with native exception handlers intercepting temporary connection timeouts gracefully.
