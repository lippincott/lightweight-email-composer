# Lightweight Email Composer

A serverless, client-side tool that creates formatted emails with dynamic Excel data. This tool runs entirely in your web browser without requiring a backend server.

## 🚀 Features

* **Zero Dependencies:** Runs directly in the browser (single HTML file).
* **Dynamic Data Entry:** Add, remove, and manage rows of data (Name, Email, Product, Quantity) via a clean UI.
* **Excel Generation:** Automatically compiles your data table into a downloadable `.xlsx` file using [SheetJS](https://sheetjs.com/).
* **Privacy Focused:** No data is sent to a server. All processing happens locally on your machine.
* **Modern UI:** Responsive design with a clean gradient aesthetic.

## 🛠️ Installation & Usage

1.  **Download:** Save the `index.html` file to your computer.
2.  **Run:** Double-click the file to open it in your default web browser (Chrome, Firefox, Safari, Edge).
3.  **Compose:**
    * Enter recipient emails (To/CC).
    * Write your subject and body text.
    * Add data rows to the table.
4.  **Generate:** Click "Generate Email with Attachment".

## ⚠️ Important: How Attachments Work

Due to strict browser security protocols, websites are **not allowed** to automatically attach files to your local email client (Outlook, Apple Mail, etc.) via the `mailto:` command.

**The Workflow:**
1.  When you click **Generate**, the tool first **downloads** the Excel file (`attachment.xlsx`) to your computer's "Downloads" folder.
2.  After a 1-second delay, it opens your default email client with the To, CC, Subject, and Body pre-filled.
3.  **Manual Step:** You must drag and drop the downloaded `attachment.xlsx` file into your open email draft.

## 💻 Tech Stack

* **HTML5 & CSS3:** For structure and styling.
* **JavaScript (Vanilla):** Logic for data handling and DOM manipulation.
* **SheetJS (xlsx):** A lightweight library loaded via CDN to generate Excel files on the fly.

## ⚙️ Customization

Since the code is contained in a single file, customization is easy:

* **Styles:** Modify the `<style>` block in the `<head>` to change colors or fonts.
* **Table Columns:** Edit the `renderTable()` and `addRow()` functions in the script to change the data fields (e.g., changing "Product" to "Service").

## 📄 License

This project is open source and available for personal or commercial use.
