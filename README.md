# 🦈 Mini-Project: Shark Attacks Analysis

**Scenario:**

We run a surf shop that offers surf lessons, rentals, and safety training. We wanted to maximize revenue while ensuring customer safety. Shark attack data helped us decide where and when to operate safely.

---

## Step 1 — Define Hypotheses

From the business case, we created simple hypotheses to guide the analysis:

- **Location & Risk:** Sharks attack more often in some areas (e.g., regions or countries) → helped decide where to operate safely.
- **Activity Risk:** Certain water activities (surfing, swimming) are riskier → helped plan lessons and rentals.
- **Time & Seasonality:** Shark attacks are more common in certain months → helped schedule lessons safely.
- **Demographics:** Age and gender influence attack likelihood → helped tailor safety training.

---

## Day 1 — Data Tasks

- Loaded the dataset into Pandas.
- Inspected columns and types using `df.info()`, `df.head()`, `df.describe(include='all')`.
- Checked for missing values with `df.isnull().sum()`.
- Checked for duplicates with `df.duplicated().sum()`.
- Documented initial issues and created a short table of potential fixes:

| Column   | Issue                | Action Taken                      |
| -------- | -------------------- | --------------------------------- |
| Age      | Missing values       | Filled with median                |
| Activity | Inconsistent strings | Standardized using `.str.lower()` |
| Date     | Stored as string     | Planned conversion to datetime    |

---

## Day 2 — Data Cleaning

- Standardized column names → lowercase, underscores
- Cleaned categorical values → gender, state, activity
- Removed duplicates → kept first occurrence
- Handled missing values → filled median for numeric, mode for categorical
- Applied numeric formatting (e.g., `customer_lifetime_value`, `number_of_open_complaints`)
- Created optional new columns → `age_group`

---

## Day 3 — Aggregation & Analysis

**Tasks Completed:**

- Grouped and aggregated data to answer hypotheses:
  - Identified which states were most dangerous
  - Determined which activities were most risky
  - Found which age groups were most affected
- Created pivot tables for combinations (e.g., state × activity)
- Filtered for key outcomes (fatal vs non-fatal attacks)
- Drew preliminary conclusions from aggregated tables

---

## Day 4 — Insights

**Findings:**

- **Top locations:** Identified states with most attacks → informed safe areas for lessons
- **High-risk activities:** Found most dangerous water sports → informed safety training
- **Age patterns:** Determined most affected age groups → targeted safety campaigns
- **Fatality analysis:** Calculated proportion of fatal vs non-fatal attacks → planned emergency response
- **Combined view:** Produced heatmap of State × Activity → supported operational decisions for the surf shop
