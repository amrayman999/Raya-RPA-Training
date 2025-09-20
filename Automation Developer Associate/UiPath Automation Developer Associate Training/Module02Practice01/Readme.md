# 🎉 **ExcellReportsConsolidation** 🎉


![Automation Recording](https://github.com/amrayman999/Raya-RPA-Training/blob/master/Automation%20Developer%20Associate/UiPath%20Automation%20Developer%20Associate%20Training/Task01/AutomationRecording.gif)

---

## 📊 **Automated Daily Sales Reports Consolidation with UiPath**

Welcome to the **ExcellReportsConsolidation** project!  
This UiPath automation streamlines the process of consolidating daily sales reports from multiple Excel files into a single, visually appealing summary workbook, complete with pivot tables and charts.

---

## 🚀 **Project Overview**

- **Purpose:**  
  Automatically collects daily sales reports from the `DailyReports` folder, merges them into a master Excel file, and generates insightful visualizations.

- **Main Workflow:**  
  See [`Main.xaml`](ExcellReportsConsolidation/Main.xaml)

- **Learning Journey:**  
  > 🏅 *This project was created as part of my UiPath Automation Developer Associate training certificate. It demonstrates practical skills in automating business processes using UiPath.*

---

## 🛠️ **How It Works**

1. **Clean Start:**  
   Deletes any existing sales results file for today to avoid duplication.

2. **Create Master File:**  
   - Generates a new Excel file in `SalesResults` named `SalesResults-YYYY-MM-DD.xlsx`.
   - Adds headers:  
     - `Item`
     - `Unit Price ($)`
     - `Items Sold`
     - `Total Income`
   - Formats header row with bold, colored background for clarity.

3. **Merge Daily Reports:**  
   - Iterates through all Excel files in `DailyReports`.
   - Ensures each file's sheet is named `Sheet1` (renames if necessary).
   - Appends each report's data to the master file.

4. **Enhance Presentation:**  
   - Autofits all columns and rows for a professional look.
   - Creates a **Pivot Table** in `Sheet2` summarizing sales by item and total income.
   - Inserts a **Pie Chart** visualizing the sales distribution.

---

## ✨ **Visual Effects**

- **Colorful Headers:**  
  Headers are highlighted in Cornflower Blue with bold text for easy reading.

- **Pivot Table & Chart:**  
  Automatically generated for instant insights.

- **Log Messages:**  
  Informative logs for sheet name corrections and process status.

---

## 📁 **Folder Structure**

```
ExcellReportsConsolidation/
│
├─ DailyReports/         # Source Excel files (one per store/day)
├─ SalesResults/         # Consolidated output files
├─ Main.xaml             # Main automation workflow
├─ project.json          # Project configuration
└─ ...                   # Supporting folders and files
```

---

## 🧩 **Dependencies**

- UiPath.Excel.Activities
- UiPath.Mail.Activities
- UiPath.System.Activities
- UiPath.Testing.Activities
- UiPath.UIAutomation.Activities

See [`project.json`](ExcellReportsConsolidation/project.json) for details.

---

## 🏁 **How to Run**

1. Place daily sales Excel files in the `DailyReports` folder.
2. Run the automation using UiPath Studio or Robot.
3. Find the consolidated report in the `SalesResults` folder.

---

## 📈 **Result Example**

![Excel Pivot Table & Pie Chart](https://img.icons8.com/color/96/000000/ms-excel.png)

---

## 💡 **Why Use This Automation?**

- **Saves Time:** No manual copy-pasting or formatting.
- **Error-Free:** Ensures consistent sheet names and structure.
- **Instant Insights:** Pivot tables and charts generated automatically.

---

> **Made with UiPath for efficient business