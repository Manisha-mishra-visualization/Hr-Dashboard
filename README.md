# HR PMS & Attrition Dashboard

A Power BI dashboard for tracking employee performance management and attrition metrics across departments, job roles, and demographics.

overview_dashboard.png

## Overview

This dashboard provides HR teams and leadership with a consolidated view of workforce health — from headcount and attrition to job satisfaction and compensation patterns — to support data-driven retention strategies.

## Key Metrics

| Metric | Value |
|---|---|
| Overall Employees | 1,470 |
| Active Employees | 1,233 |
| Attrition (count) | 237 |
| Attrition Rate | 16.12% |
| Average Age | 37 |
| Average Salary Band | 15 |

## Dashboard Sections

- **Employee by Department** — headcount split by gender across Research & Development, Sales, and Human Resources.
- **Employees Performance Rating** — distribution of performance ratings (3 vs 4) across the workforce.
- **Work Life Balance by Job Role & Gender** — female/male breakdown and totals across job roles (Healthcare Representative, Human Resources, Laboratory Technician, Manager, Manufacturing Director, Research Director, Research Scientist).
- **Employee – Job Satisfaction** — proportion of employees reporting High, Medium, Low, and Average satisfaction.
- **Employee Marital Status** — split across Married, Single, and Divorced employees.
- **Monthly Income by Job Level and Gender** — compensation comparison across job levels, by gender.

## Filters

- **Department** — filter all visuals by department.
- **Age** — filter all visuals by employee age.

## Tech Stack

- **Power BI Desktop** — dashboard authoring
- **Power Query (M)** — data transformation
- **DAX** — calculated measures (see [docs/dax_measures.md](docs/dax_measures.md))

## Data

The dataset structure closely follows the commonly used IBM HR Analytics Employee Attrition dataset (department, job role, marital status, job satisfaction, work-life balance, performance rating, monthly income, etc.).

> **Note:** No real employee data is included in this repository. Place your own dataset in `data/raw/` before opening the `.pbix` file, or point Power BI to your own data source. See [docs/data_dictionary.md](docs/data_dictionary.md) for expected columns.

## Repository Structure

```
HR-PMS-Attrition-Dashboard/
├── data/
│   ├── raw/            # original/source dataset (not committed if sensitive)
│   └── processed/      # cleaned data used by the model
├── pbix/
│   └── HR_PMS_Attrition_Dashboard.pbix
├── docs/
│   ├── screenshots/    # dashboard images for this README
│   ├── data_dictionary.md
│   └── dax_measures.md
├── reports/
│   └── HR_PMS_Attrition_Dashboard.pdf   # optional exported PDF view
├── .gitignore
├── .gitattributes
└── README.md
```

## Getting Started

1. Clone this repository.
   ```bash
   git clone https://github.com/<your-username>/HR-PMS-Attrition-Dashboard.git
   ```
2. Add your dataset to `data/raw/`.
3. Open `pbix/HR_PMS_Attrition_Dashboard.pbix` in **Power BI Desktop**.
4. Update the data source path/connection if needed (Home → Transform Data → Data Source Settings).
5. Refresh the data and explore.



## Data Privacy

If your `.pbix` file is connected to real employee data, **do not commit that data** to a public repository. Use anonymized/synthetic data, or keep the repo private.
