# 📊 Smart Excel Combiner & Report Builder

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Platform](https://img.shields.io/badge/platform-Browser-orange.svg)
![Privacy](https://img.shields.io/badge/privacy-100%25%20Local-green.svg)

A powerful, single-file tool to merge Excel files, analyze data, and generate custom reports directly in your browser.

Unlike standard mergers, this tool allows you to **select specific rows** from multiple files, **reorder them**, and export a curated **Word (.docx)** or **Excel (.xlsx)** document.

## ✨ Key Features

### 🧠 Smart Data Merging
* **Header Mapping:** Automatically aligns columns by name (e.g., "Email" maps to "Email"), even if the column order differs between files.
* **Dynamic Discovery:** If a file contains a new column not present in previous files, it is automatically added to the master table.

### 🔍 Interactive Data View
* **Sortable Columns:** Click any table header to sort data A-Z or Z-A.
* **Persistent Selection:** The "Memory" feature ensures your checkmarks remain saved even while you sort and filter the table.
* **Bulk Actions:** "Select All" and "Deselect All" controls for rapid processing.

### 📝 Drag-and-Drop Report Builder
* **Staging Area:** Move selected rows into a dedicated "Report" section.
* **Reorder:** Drag and drop report items to arrange them in the exact order you need.
* **Clear & Reset:** Easily remove specific items or wipe the entire report to start fresh.

### 📤 Native Exports
* **Word Export (.docx):** Generates a genuine Microsoft Word document with a formatted table (no "corrupt file" warnings).
* **Excel Export (.xlsx):** Downloads a clean spreadsheet of your report.

### 🔒 Privacy Focused
* **Client-Side Only:** No data is ever uploaded to a server. All processing happens locally in your browser's memory using JavaScript.

## 🚀 Quick Start

**No installation required.** This tool runs as a standalone HTML file.

1.  Download the `index.html` file from this repository.
2.  Open `index.html` in any modern web browser (Chrome, Edge, Firefox, Safari).
3.  **Drag & Drop** your Excel files onto the upload area.
4.  Click **Combine & View Data**.

## 🛠 Usage Guide

1.  **Upload:** Drop multiple `.xlsx` or `.xls` files.
2.  **Combine:** Click the button to merge them into a master view.
3.  **Select:** Check the boxes for the rows you want to include in your final document. You can sort columns to find data easier—your selections will be saved!
4.  **Add to Report:** Click "Add Selected to Report" to move them to the bottom section.
5.  **Refine:**
    * Drag rows up/down to change the order.
    * Click `✕` to remove a single row.
    * Click `🗑️ Clear Report` to reset the report section.
6.  **Export:** Click "Export to Word" or "Export to Excel" to get your final file.

## 📦 Tech Stack

This project uses pure HTML/CSS/JS and relies on two powerful CDNs:

* **[SheetJS (xlsx)](https://sheetjs.com/):** For reading and writing Excel files.
* **[docx.js](https://docx.js.org/):** For generating valid Microsoft Word documents programmatically.

## ⚠️ Limitations

* **Header Case Sensitivity:** "Email" and "email" are treated as two different columns. Ensure your source files have consistent header capitalization.
* **Browser Memory:** Because this runs in your RAM, combining massive datasets (e.g., hundreds of thousands of rows) may cause the browser tab to slow down or crash.

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.
