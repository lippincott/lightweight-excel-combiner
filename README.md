# 📊 Lightweight Excel Combiner

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Platform](https://img.shields.io/badge/platform-Browser-orange.svg)
![Dependency](https://img.shields.io/badge/dependency-SheetJS-green.svg)

A clean, modern, and privacy-focused tool to merge multiple Excel files (`.xlsx`, `.xls`) directly in your web browser. 

Unlike standard mergers that simply stack rows, this tool utilizes **Smart Column Mapping** to align data based on header names, ensuring your data remains consistent even if column orders differ between files.

## ✨ Features

* **🔒 100% Client-Side:** No server uploads. Your data never leaves your browser, making it safe for sensitive information.
* **🧠 Smart Column Mapping:** Matches columns by header name (e.g., "Email" maps to "Email"), regardless of the column order in the source files.
* **➕ Dynamic Header Discovery:** If File B has a column that File A is missing, the tool automatically adds it to the master header list.
* **⚡ Zero Install:** Runs as a single HTML file. No Python, Node.js, or complex backend required.
* **👀 Live Preview:** See a snapshot of your combined data before downloading.

## 🚀 Quick Start

### Option 1: Run Locally
1.  Download the `index.html` file from this repository.
2.  Double-click `index.html` to open it in any modern browser (Chrome, Edge, Firefox, Safari).
3.  Drag and drop your Excel files and click **Combine**.

### Option 2: Host it
You can host this static file anywhere (GitHub Pages, Netlify, Vercel, or an internal corporate intranet). It requires no backend processing.

## 🛠 How it Works

1.  **Ingestion:** The tool uses the [SheetJS](https://sheetjs.com/) library to read uploaded binary files.
2.  **Parsing:** It converts spreadsheet rows into JSON Objects (Key-Value pairs).
3.  **Alignment:** * It scans every file to build a "Master List" of unique headers.
    * It iterates through all rows and maps data to the correct header in the Master List.
4.  **Export:** It generates a new workbook and triggers a browser download.

## ⚠️ Limitations & Best Practices

* **Exact Header Matching:** The tool is case-sensitive. `Email` and `email` will be treated as two different columns. Ensure your source files have consistent naming conventions.
* **Browser Memory:** Since this runs entirely in your browser's RAM, combining dozens of massive files (e.g., 50MB+ each) may cause the tab to crash. It is best suited for small-to-medium datasets.

## 🤝 Contributing

Contributions are welcome! If you'd like to improve the UI or add features like fuzzy-matching for headers:

1.  Fork the Project
2.  Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3.  Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4.  Push to the Branch (`git push origin feature/AmazingFeature`)
5.  Open a Pull Request

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.

---

*Built with vanilla JavaScript and [SheetJS](https://github.com/SheetJS/sheetjs).*
