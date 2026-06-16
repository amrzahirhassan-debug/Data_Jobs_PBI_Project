# 📊 Data Jobs Dashboard — Power BI Project
![Page_1](/Resources/Page_1.png)



> A two-page interactive Power BI report analyzing the global data jobs market in 2024, covering salary benchmarks, job distribution, role-level comparisons, and job condition breakdowns.

---

## 🎯 Project Goal

The goal of this project was to explore the data jobs landscape in 2024 and answer key questions a job seeker or hiring manager would care about:

- Which data roles have the highest volume of openings?
- How do hourly and yearly salaries compare across job titles?
- What job conditions are attached to each role (remote work, health insurance, degree requirements)?
- Where are data jobs concentrated globally?

The dashboard was designed for clarity and interactivity — allowing users to filter by job title and drill through from a high-level overview into role-specific detail.

---

## 🗂️ Project Structure

```
DJ_Dashboard.pbix       ← Power BI report file (main deliverable)
Recording.gif           ← Screen recording demo of the dashboard in action
Page_1.png              ← Screenshot: Main Overview page
Page_2.png              ← Screenshot: Drill-Through Detail page
README.md               ← This file
```

---

## 📄 Dashboard Pages

### Page 1 — Overview (Data Jobs Dashboard)
![Page_1](/Resources/Page_1.png)



The landing page gives a high-level snapshot of the entire dataset.

| Visual | Description |
|---|---|
| **KPI Cards** | Total job count (479K), salary rating (5 stars), median yearly salary ($113K), median hourly salary ($47.62) |
| **Bar Chart** | Job count by title — Data Engineer leads, followed by Data Analyst and Data Scientist |
| **Scatter Plot** | Hourly vs. yearly salary by job title — reveals which roles are high-compensation across both dimensions |
| **Line Chart** | Monthly job count trend across 2024 — shows a sharp drop from July onward |
| **Table with Spark Lines** | Summary of all job titles with job count, hourly salary, yearly salary, and a mini trend line |
| **Slicer** | Filter by job title — affects all visuals simultaneously |
| **Drill Through button** | Navigate to the detail page for the selected role |

---

### Page 2 — Drill-Through Detail (Role-Level View)
![Page_1](/Resources/Page_2.png)

Activated by right-clicking a job title or using the Drill Through button. Scoped to a single role (example shown: Data Engineer).

| Visual | Description |
|---|---|
| **Gauge — Yearly Salary** | Target salary range with current median highlighted ($126K, range: $15K–$640K) |
| **Gauge — Hourly Salary** | Hourly rate range ($59.16 median, range: $9–$221) |
| **Donut — Work From Home** | 15% of Data Engineer postings mention remote work |
| **Donut — Health Insurance** | Only 10% include health insurance mention |
| **Donut — No Degree Required** | 47% of postings do not mention a degree requirement |
| **Map** | Global job distribution (bubble map) — heavy concentration in North America and Europe |
| **Bar Chart** | Job count for the selected title |
| **Treemap** | Employment type split: Full-time (~90%) vs. Contract (~9%) |
| **Back arrow** | Returns user to Page 1 |

---

## 🔧 What Was Built

- **Two-page report** with a main overview and a drill-through detail view
- **Job title slicer** that filters all visuals on Page 1
- **Drill-through filter** scoped to job title on Page 2
- **Gauge charts** for salary range visualization with target markers
- **Donut charts** for binary job condition flags (remote, health insurance, degree)
- **Bubble map** showing global job distribution
- **Spark lines** in the summary table for mini trend context
- **Custom dark theme** — deep purple/black palette with neon magenta accents for visual identity
- **Clear all slicers button** and **tooltip/help button** on Page 1

---

## 📐 Design Decisions

- **Color palette:** Dark background (#0D0D1A range) with purple (#7B2FBE) and magenta (#FF00FF) accents — consistent across both pages for professional cohesion
- **Scatter plot** was chosen over a standard bar to show the relationship between two salary dimensions simultaneously, making salary outliers visible
- **Drill-through** was used instead of page-level filters to preserve Page 1 as a full market overview and give role-specific detail its own focused canvas
- **Gauges** on Page 2 communicate salary range context, not just a single number — which is more useful when benchmarking your own salary expectations

---

## 📊 Dataset Summary

| Attribute | Detail |
|---|---|
| **Scope** | Global data job postings, 2024 |
| **Total records** | ~479,000 job listings |
| **Job titles covered** | 10 (Data Engineer, Data Analyst, Data Scientist, Senior variants, Business Analyst, Software Engineer, ML Engineer, Cloud Engineer) |
| **Key fields** | Job title, yearly salary, hourly salary, work from home flag, health insurance flag, degree requirement flag, employment type, location |

---

## 💡 Key Insights

1. **Data Engineer** has the highest job volume (~129K postings) but sits mid-range on hourly salary ($59/hr)
2. **Software Engineer** and **Machine Learning Engineer** lead on both hourly and yearly compensation
3. **Data Analyst** is the most accessible entry point — highest volume after Data Engineer, lowest salary floor
4. Job postings dropped significantly after July 2024 — a seasonal or market contraction pattern worth monitoring
5. Remote work mentions are low across all roles (~15% for Data Engineer), suggesting most roles still expect in-person or hybrid
6. Degree requirements are becoming optional — 47% of Data Engineer postings don't mention a degree

---

## 🛠️ Tools Used

- **Power BI Desktop** — report design, DAX measures, drill-through logic, custom theme
- **Power Query** — data transformation and column standardization
- **DAX** — calculated measures for median salary, job count, salary rating

---

## 🧠 Skills Demonstrated

- Multi-page report architecture with drill-through navigation
- KPI design and gauge chart configuration
- Scatter plot for dual-metric comparison
- Geospatial visualization (bubble map)
- Conditional formatting in tables
- Slicer and filter interaction design
- Custom dark theme application in Power BI
- Data storytelling — structuring visuals to answer a specific question flow
