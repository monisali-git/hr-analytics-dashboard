# 📊 HR Analytics Dashboard — People Intelligence

A fully interactive, client-side HR Analytics Dashboard built with vanilla HTML, CSS, and JavaScript. This tool allows HR professionals and managers to upload their workforce data (Excel/CSV) and instantly generate actionable insights without needing any backend server or database.

## 🚀 Key Features

* **Zero Server Footprint:** 100% client-side data processing. Your sensitive HR data never leaves your browser.
* **Dynamic Excel/CSV Upload:** Instantly parse and visualize workforce data using `SheetJS`.
* **Interactive Data Visualization:** Beautiful, responsive charts powered by `Chart.js` (Demographics, Attrition, Job Satisfaction, Overtime impact, etc.).
* **Advanced KPIs:** Automatically calculates Headcount, Attrition Rate, Active Employees, Average Age, and Average Monthly Pay.
* **Department Filtering:** Instantly filter all dashboard metrics by specific departments (e.g., R&D, Sales, HR).
* **Export Options:** 
  * **Export to PDF:** Generates a high-quality, multi-page PDF report of the entire dashboard using `html2canvas` and `jsPDF`.
  * **Export to Excel:** Download the detailed workforce data back into a clean `.xlsx` file.

## 🛠️ Technologies Used

* **HTML5 / CSS3 / Vanilla JS** - Core structure, styling, and logic.
* **[Chart.js](https://www.chartjs.org/)** - For rendering dynamic doughnut, bar, and line charts.
* **[SheetJS (xlsx)](https://sheetjs.com/)** - For reading user-uploaded Excel/CSV files and exporting data.
* **[html2canvas](https://html2canvas.hertzen.com/) & [jsPDF](https://parall.ax/products/jspdf)** - For capturing the dashboard and exporting it as a downloadable PDF.

## 📥 How to Use

1. Clone or download this repository.
2. Open the main HTML file (`index.html`) directly in any modern web browser.
3. Click on the **"⬆ Upload Data"** button at the top right.
4. Select your HR dataset (must be `.xlsx`, `.xls`, or `.csv`).
5. The dashboard will instantly populate. Use the top navigation to filter by departments or click **"📄 Export PDF"** to save your report!

## 📊 Required Data Structure

For the dashboard to accurately map your data, your uploaded Excel/CSV file should contain columns with the following names (case-insensitive):

| Expected Column Name | Description |
| :--- | :--- |
| `Age` | Employee's age (e.g., 30) |
| `Attrition` / `Status` | Employee exit status (`Yes`, `No`, `1`, `0`) |
| `Department` / `Dept` | e.g., Research & Development, Sales, HR |
| `JobRole` / `Role` | e.g., Sales Executive, Laboratory Technician |
| `Gender` / `Sex` | `Male`, `Female` |
| `MonthlyIncome` / `Salary`| Employee's monthly pay (Numeric) |
| `JobSatisfaction` | Rating from 1 (Low) to 4 (High) |
| `Overtime` / `OT` | `Yes` or `No` |
| `BusinessTravel` | e.g., Travel_Rarely, Travel_Frequently |
| `EducationField` | e.g., Life Sciences, Medical, Marketing |
| `WorkLifeBalance` | Rating from 1 (Poor) to 4 (Excellent) |

*Note: The script includes a smart column-matcher, so exact naming isn't strictly necessary as long as the keyword (e.g., "pay" or "salary") is present in the header.*

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).
