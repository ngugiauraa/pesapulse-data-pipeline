# Pesa Pulse API Customer Analysis Pipeline

An automated data engineering and analytics pipeline designed for **Pesa Pulse** (Nairobi, Kenya) to securely download, flatten, validate, and chart structured customer directory profiles from a partner REST endpoint prior to launch campaigns.

## Execution Guide

Follow these sequential environment steps to initialize your sandbox and execute the core pipeline securely:

### 1. Clone the Repository
Clone this workspace down to your local architecture and navigate straight to the project root directory:
```bash
git clone https://github.com/ngugiauraa/pesapulse-data-pipeline
cd pesapulse-data-pipeline
```

### 2. Configure a Virtual Environment
Isolate your development dependencies from your global python layout environment using standard `venv` setups:

* **On Windows Platforms:**
  ```pwsh
  python -m venv venv
  .\venv\Scripts\activate
  ```
* Bash
  ```bash
  python3 -m venv venv
  source venv/bin/activate
  ```
*Your terminal shell prompt line will now prepend an indicator token reading `(venv)` confirming active runtime isolation.*

### 3. Install Application Dependencies
Update your isolated sandbox workspace layout with necessary framework processing tools:
```bash
pip install -r requirements.txt
```

### 4. Execute the Data Pipeline
Run the modular orchestration script directly through your active virtual terminal layer:
```bash
python analysis.py
```
Upon processing initiation, the engine establishes streaming validation linkages, dumps log metadata profiles, checks internal data dictionaries against Pandas aggregations, and writes clean assets directly to your local `output/` directory workspace.

---

## Implementation Architecture

The framework splits tracking operations across clean structural boundaries to satisfy engineering marking requirements:

* **Data Ingestion & Integrity Protection (Tasks 1 & 2):** Connects to the REST endpoint utilizing `requests` with a strict `timeout=10` threshold safety tripwire. Schema objects are structurally analyzed using an automated recursive object tree-walk loop to map nesting depth constraints cleanly.
* **Normalization & Key-Tie Sorting (Tasks 3, 4 & 5):** Deep nested variables (like coordinate values) are isolated and transformed into native decimal floating-point data arrays. Primary indexing columns are updated to match strict template headers (`customer_id`). Aggregation operations execute using a tuple weight-factor string sort layout (`key=lambda item: (-item, item)`) to arrange equal-count items in a clean, alphabetical secondary arrangement automatically.
* **Pandas Assertion Cross-Checks & Exports (Tasks 6, 7 & 8):** Flat record sequences are loaded into a `pandas.DataFrame`. The script forces an alphabetical key-standardization check across target dictionaries before validating pure Python aggregation structures against Pandas `.value_counts()` calculations. Safe tabular assets map data parameters to `customer_count` rows before writing to index-free, machine-readable CSV files.

---

## Data Discoveries & Strategy Insights

* **Perfect Audience Fragmentation:** Our market contains **10 total active records scattered uniformly across 10 separate unique cities**. Because regional population concentration is non-existent, marketing dollars should avoid localized physical ad campaigns (like billboards) and favor wider programmatic online distribution funnels.
* **Top-Level Domain Suffix Penetration:** Sorting the target customer mailing extensions isolates **.biz** as the leading Top-Level Domain extension (representing 40% of overall user volume across 4 profiles), pointing to a distinctly business-centric user base.
* **Visual Value Contrast Analysis:** Generating a traditional city bar chart outputs a completely flat line where every property equals a count of 1, rendering it useless for growth planners. Utilizing the `.png` breakdown for top-level email domains groups users into structural segments that teams can target right away.

---

## Underlying System Assumptions

* **Fallback Structural Metrics:** Missing nested location properties can fall back on coordinate defaults of `0.0` without invalidating adjacent profile record arrays.
* **Domain Extraction Scope:** In compliance with template specifications, the field variable tracking `email_domain` targets the isolated terminal top-level domain suffix string element (e.g., parsing `biz` out of a user email layout).
* **Availability Thresholds:** Pipeline tasks assume the upstream server maintains structural schema tree configurations, with native exception handlers intercepting temporary connection timeouts gracefully.

Built by [Jesse Ngugi](https://ngugi.pages.dev)