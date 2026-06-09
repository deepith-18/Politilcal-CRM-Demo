# 🏛️ Political CRM Suite v2.0 - Executive Dashboard

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![SheetJS](https://img.shields.io/badge/SheetJS-00A65F?style=for-the-badge&logo=microsoftexcel&logoColor=white)

A premium, frontend-only **Executive CRM Dashboard** designed specifically for political campaigns, constituency management, and mobilization strategies. Built with pure HTML, CSS, and Vanilla JavaScript, this tool provides real-time data visualization, dynamic constituent tracking, and a built-in interactive tele-calling simulator.

---

## ✨ Key Features

*   📊 **Executive Analytics Dashboard:** Custom 3D SVG bar charts, Voter Support gauges, and district-level metrics.
*   👥 **Advanced Contacts Database:** 3D interactive tilt cards, list/grid view toggles, and multi-parameter filtering (by District, Constituency, Role, and Sentiment).
*   📥 **Excel Spreadsheet Importer:** Drag-and-drop `.xlsx` / `.xls` support via **SheetJS** to instantly populate the database with campaign data.
*   📞 **Integrated Dialer Simulator:** Built-in calling interface with a live timer, outcome disposition logging, and sentiment tracking.
*   📋 **Constituent Profile Inspector:** Individual dossier views featuring persistent action-task checklists and chronological interaction timelines.
*   📱 **Responsive Premium UI:** Glassmorphism effects, 3D shadows, and a mobile-first bottom navigation bar for seamless tablet and smartphone use.
*   🛡️ **Offline Sandbox Mode:** Falls back to an integrated static database of 50 sample contacts if no Excel file is provided, ensuring zero downtime.

---

## 🚀 Getting Started

Because this application relies entirely on frontend technologies, there is no need for a complex backend setup or a local server for the base functionality.

### 1. Simple Run (Browser)
1. Clone or download this repository.
2. Double-click the `index.html` file to open it in any modern web browser.
3. The app will automatically initialize the **Offline Sandbox Data**.

### 2. Full Experience (Local Server)
To test the dynamic `.xlsx` auto-fetch functionality, you must run it through a local web server (to avoid CORS/File protocol restrictions).
*   **VS Code:** Install the `Live Server` extension and click "Go Live".
*   **Python:** Run `python -m http.server 8000` in the directory.
*   **Node.js:** Run `npx serve` in the directory.

---

## 📂 Excel Importer Schema

The CRM features an **Excel Importer Tab** that allows campaign managers to drag and drop constituent lists. For the CRM to parse your data correctly, ensure your spreadsheet has the following headers:

| ID | Name | Mobile | District | Constituency | Profession | Category | Address |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | Ramesh Gowda | 9054478620 | Mysuru | Vijayapura | Engineer | Volunteer | Ward 43 |

*Supported Role Categories:* `Volunteer`, `Donor`, `Influencer`, `VIP Contact`, `Booth Leader`, `Party Worker`.

> **Note:** The application attempts to auto-fetch a file named `Political_CRM_Demo_50_Records.xlsx` on initial load. You can download the template directly from the "Excel Importer" tab in the app.

---

## 🛠️ Built With

*   **HTML5** - Semantic markup
*   **CSS3** - Custom CSS variables, Grid/Flexbox layouts, 3D CSS transforms, and Keyframe animations.
*   **Vanilla JavaScript (ES6+)** - State management, DOM manipulation, and dynamic SVG rendering without heavy frameworks like React or Vue.
*   **[SheetJS (xlsx)](https://sheetjs.com/)** - Client-side Excel parsing.
*   **Google Fonts** - *Outfit* and *Plus Jakarta Sans* for premium typography.

---

## 💻 Technical Highlights

*   **Custom SVG Charting Engine:** Bar charts and gauge arcs are generated mathematically via JS and drawn using raw `<svg>` nodes—eliminating the need for heavy charting libraries like Chart.js.
*   **CSS 3D Tilt Cards:** Employs math-driven CSS custom properties (`--rx`, `--ry`) linked to mousemove events to create an Apple-like 3D hover effect on constituent cards.
*   **In-Memory State Management:** Handles CRUD operations (tasks, timeline logs, sentiment updates) entirely in-memory for lightning-fast UI updates.

---

## 📜 License

This project is open-source and available under the **MIT License**. Feel free to copy, modify, and use it for your own campaigns or professional portfolios.
