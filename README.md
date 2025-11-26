# 🚀 Data Cleaning & Analysis: Married Individuals Average Children Count

## 📊 Project Overview

This Power BI project, **"Data Cleaning - Married Average Children Count,"** is focused on the critical steps of **data cleaning** and subsequent **analysis** to determine the **Average Number of Children** for individuals specifically identified as **Married**.

This analysis serves as a foundational step to ensure data quality and provide a reliable, clean baseline metric essential for downstream reporting, advanced analytics, and broader business intelligence initiatives.

---

## ✨ Key Objectives

* **Implement & Document:** Clearly document and implement robust data cleaning and transformation steps applied to the raw source data.
* **Accurate Calculation:** Precisely calculate the average number of children (**Kidhome** + **Teenhome**) for the **'Married'** segment of customers.
* **Visualize Impact:** Visualize the final clean metric and illustrate the impact of the data cleaning process.

---

## ⚙️ Technical Details

* **Power BI File:** `Data Cleaning - Married Average Children Count.pbix`
* **Data Source:** [CSV File located] at (/Power-BI-Data-Cleaning-Married-Average-Children-Count
/marketing_customer_data_uncleaned.csv)
* **Tools Used:** **Power BI Desktop**, **Power Query (M Language)**, and **DAX**.

---

## 🔍 Data Cleaning & Transformation (Power Query)

The following sequence of critical data cleaning and transformation steps was executed in **Power Query** (M language) to prepare the data:

| Step | Action Performed | Purpose |
| :--- | :--- | :--- |
| **Initial Cleanup** | Replace `"NA"` with `""` across all columns. Transpose table to easily remove entirely blank rows. | Handles inconsistent missing value representation and removes unneeded rows. |
| **Header & Duplicates** | Promote Headers. Remove duplicate rows based on **'Column1'** (assumed to be the unique identifier). | Ensures correct column naming and data uniqueness. |
| **Data Standardisation** | Replace the suffix `" kid(s)"` with `""` in the **Kidhome** column. | Prepares the column for numerical type conversion. |
| **Type Conversion** | Transform column types (e.g., **ID** to Integer, **Income** to Currency, **Dt\_Customer** to Date). | Enforces data integrity and enables proper mathematical operations. |
| **Final Polish** | Sort the resulting table by **ID** in ascending order. | Organizes the final clean data table. |

---

## 💡 Key Measure & Visualization (DAX & Report View)

While a formal DAX measure could be created, the **Average Children Count for Married Individuals** was primarily derived and validated within the **Report View** using Power BI's built-in summarization capabilities.

1.  **Total Children (Sum):**
    * A visual (e.g., a Bar/Column Chart) was created.
    * **Kidhome** (or a combined measure of Kidhome + Teenhome) was added to the X-axis (Summarized as **Sum**).
    * **Marital\_Status** was added to the Y-axis.
    * *Result:* This initial view shows the **Total Number of Children** for each marital status group.
2.  **Average Children (Average):**
    * A duplicate visual was created.
    * The summarization within the Y-axis was changed from **Sum** to **Average**.
    * *Result:* This final view provides the **Average Number of Children** for each marital status, giving the final desired metric for the 'Married' group.

---

## 🛠️ How to Use

1.  **Download:** Clone this repository to your local machine.
2.  **Open:** Open the `Data Cleaning - Married Average Children Count.pbix` file using **Power BI Desktop**.
3.  **Explore:** Navigate through the report pages to view the cleaned data and the final average children count visualization.
4.  **Refresh (if necessary):** If the data source is not embedded or the local path has changed, you may need to update the source path:
    * Go to **File** > **Options and settings** > **Data source settings**.
    * Select the source and choose **Change Source...** to update the file path to its new local location.
