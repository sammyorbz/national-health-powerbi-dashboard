# 📊 National Health Power BI Dashboard  
## Build Process & Methodology

This document outlines the step-by-step process used to design, model, and build an interactive **National Health Dashboard** using Power BI. The project follows best practices commonly used in real-world business intelligence and analytics workflows.

---

## 1. Project Objective

The goal of this project was to build a **data-challenge–style healthcare dashboard** that delivers actionable insights on:

- Patient demographics and admissions
- Hospital capacity and operational performance
- Treatment outcomes by medical condition
- Healthcare billing and cost trends

The dashboard is fully interactive, allowing users to explore data by **year, month, hospital, and medical condition**.

---

## 2. Project Assets & Environment

The project was developed using a pre-structured setup, similar to enterprise BI scenarios, including:

- A healthcare dataset (fact and dimension tables)
- A Power BI template file (`.pbix`)
- A custom PowerPoint background for layout design
- Pre-written DAX measures provided with the template

The focus of the project was on **data integration, modeling, visualization, and interactivity**, rather than writing measures from scratch.

---

## 3. Data Connection & Parameter Configuration

Upon opening the Power BI file, data source errors occurred due to unresolved file paths.

### Steps Taken
- Opened **Power Query** via *Transform Data*
- Updated the **Data Folder parameter** to reference the local dataset directory
- Ensured the folder path ended with a trailing slash (`/`)
- Refreshed all queries to reload the datasets successfully

This parameter-based setup ensures the report is **portable and reusable** across different machines.

---

## 4. Data Preparation (Power Query)

Light transformations were applied to prepare the data for analysis:

- Validation of column data types
- Review of existing transformations
- Creation of calculated columns, including:
  - **Length of Stay** (difference between admission and discharge dates)
  - **Length of Stay Buckets**:
    - Short stay (1–3 days)
    - Moderate stay (4–7 days)
    - Long stay (8–14 days)

These steps support meaningful operational and efficiency analysis.

---

## 5. Data Modeling

A clean and efficient data model was implemented:

### Model Structure
- **Fact Table:** Health Data
- **Dimension Tables:**
  - Calendar (date intelligence and time filtering)
  - Medical Condition (condition metadata, descriptions, images)

The fact table sits at the center of the model with one-to-many relationships to each dimension.

A dedicated **Measures table** was also created to centrally store and organize all DAX calculations and KPIs.

---

## 6. Key Performance Indicators (KPIs)

The following healthcare KPIs were implemented using card visuals:

- Total admitted patients (distinct count)
- Room / bedspace availability
- Average billing amount
- Number of doctors
- Average length of stay
- Average patient age

Consistent formatting was applied across KPIs to improve readability and visual alignment.

---

## 7. Year-over-Year (YoY) Analysis

Year-over-year logic was implemented to compare current values against the previous year.

### Key Features
- Dynamically detects the selected year
- Calculates prior-year values automatically
- Handles edge cases gracefully:
  - No year selected
  - Missing previous-year data

The output includes:
- Percentage change
- Directional indicators (increase / decrease)
- User-friendly messages instead of blank values

This improves clarity for both technical and non-technical users.

---

## 8. Patient Demographics Analysis

Patient demographics were analyzed across multiple dimensions:

- Age group
- Gender
- Medical condition
- Blood group

### Bookmark-Based Navigation
Bookmarks were used instead of field parameters to:
- Switch between demographic views
- Preserve slicer selections
- Prevent unintended filter resets

A bookmark navigator enables seamless switching between views while maintaining filter context.

---

## 9. Condition-Specific Insights

For each selected medical condition:
- Condition images update dynamically
- Condition descriptions are displayed contextually
- Test results are analyzed as:
  - Normal
  - Inconclusive
  - Abnormal

Both **counts and percentages** are displayed to provide balanced insight into treatment outcomes.

---

## 10. Hospital Performance Analysis

Hospital-level analysis was implemented using:

- A **matrix visual** comparing hospitals against medical conditions
- Conditional formatting to highlight high-volume combinations

A supporting column chart summarizes total admissions by condition, enhancing quick visual comparison.

---

## 11. Key Trends Analysis

A **field parameter** was created to dynamically switch trend analysis between:

- Admitted patients
- Average length of stay
- Average billing amount

A line chart visualizes monthly trends by admission type, supported by:
- Dynamic titles
- Clean formatting
- Controlled slicer interactions

---

## 12. Treatment & Cost Analysis

The final page focuses on financial and treatment insights, including:

- Total billing by admission type
- Length of stay distribution
- Billing analysis by:
  - Hospital
  - Insurance provider (via parameter switch)

Dynamic titles update automatically based on the selected medical condition, improving interpretability.

Additional matrix visuals highlight:
- Medical condition vs medication usage
- Treatment patterns across facilities

---

## 13. Interactivity & Navigation

To enhance usability:
- Slicer interactions were carefully managed using *Edit Interactions*
- Bookmark and page navigators were used for seamless navigation
- Consistent styling was applied across pages for a professional look

---

## 14. Final Outcome

The completed dashboard enables stakeholders to:

- Monitor patient trends and demographics
- Evaluate hospital and operational performance
- Identify cost drivers and inefficiencies
- Compare treatment outcomes across conditions and providers

---

## 15. Notes & Future Improvements

- Integrate predictive analytics for admissions and costs
- Add real-time or streaming data sources
- Expand coverage to additional hospitals and conditions

---

## 16. Disclaimer

This project was built for **learning and portfolio purposes** using a guided dataset and template.  
All implementation, customization, modeling decisions, and documentation reflect independent analytical understanding.

---

📌 **Author:**  
*Data Analyst Portfolio Project*
