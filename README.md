
# PDF Chapterizer - 智慧 PDF 章節分割工具

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

**PDF Chapterizer** 是一個完全在瀏覽器端運行的網頁工具，它利用 Google Gemini AI 的強大能力，智慧分析 PDF 檔案的目錄 (Table of Contents)，並讓您能夠輕鬆地將長篇 PDF 分割成獨立的章節檔案進行下載。

[English Version](#english-version)

---

## 🚀 解決的痛點 (The Pain Point It Solves)

你是否也曾遇到過這種情況？

當你想將一本厚重的電子書、學術論文或研究報告上傳到像 **Google NotebookLM** 這樣的 AI 筆記與研究工具時，卻被單一來源 **50 萬字的限制**擋在門外？手動分割 PDF 不僅耗時，而且容易出錯，尤其是當你需要頻繁處理大量文件時。

**PDF Chapterizer 就是為了解決這個痛點而生。**

它能透過 AI 自動識別章節結構，讓你將大型文件拆分成更小、更易於管理的章節部分。這樣一來，你就可以將每個章節作為一個獨立的來源上傳到 NotebookLM，完美繞過上傳限制，讓 AI 更專注、更深入地分析每個章節的內容。

## ✨ 主要功能 (Features)

*   **🧠 智慧目錄分析**: 使用 Google Gemini AI 自動從 PDF 前 20 頁的文字中識別章節標題與起始頁碼。
*   **💻 純瀏覽器端運行**: 您的 PDF 檔案和 API Key **不會上傳到任何第三方伺服器**。所有處理過程（文字擷取、PDF 分割）都在您的本機瀏覽器中完成，確保您的資料隱私與安全。
*   **✂️ 一鍵分割與下載**: 分析完成後，清晰列出所有章節及其頁碼範圍。您可以單獨下載任何一個您感興趣的章節。
*   **📦 批量下載**: 提供「全部下載」功能，一鍵產生並下載所有分割後的章節檔案。
*   **🔑 API Key 記憶**: 可選擇將您的 Gemini API Key 安全地儲存在瀏覽器的 `localStorage` 中，方便下次使用，無需重複輸入。

## 📖 如何使用 (How to Use)

1.  **取得 Gemini API Key**: 前往 [Google AI Studio](https://aistudio.google.com/prompts/new_chat) 點擊 "Get API key" 來免費取得您的金鑰。
2.  **貼上 API Key**: 將複製的金鑰貼到工具的輸入框中。
3.  **(可選) 記住金鑰**: 勾選「記住我的 API Key」選項，金鑰將被儲存在您的瀏覽器中。
4.  **選擇 PDF 檔案**: 點擊按鈕選擇您要處理的 PDF 檔案。
5.  **開始分析**: 點擊「1. 分析目錄」按鈕，工具將開始讀取檔案並呼叫 Gemini AI。
6.  **下載章節**: 分析結果將會顯示在下方。您可以點擊每個章節旁的「下載」按鈕，或點擊「全部下載」來一次取得所有檔案。

## 🛠️ 技術棧 (Tech Stack)

*   **前端**: HTML, CSS, JavaScript (ES6+)
*   **AI 模型**: Google Gemini API (gemini-1.5-flash)
*   **PDF 處理**:
    *   [PDF.js](https://mozilla.github.io/pdf.js/) 用於讀取 PDF 內容並擷取文字。
    *   [PDF-Lib](https://pdf-lib.js.org/) 用於根據頁碼範圍建立新的 PDF 章節檔案。

## ⚠️ 安全警告 (Important Security Warning)

您的 API Key 僅儲存在您瀏覽器的 `localStorage` 中，並在發起請求時直接從您的瀏覽器發送到 Google 的 API 端點。它**絕對不會**經過我們的伺服器。儘管如此，這仍然是一種前端暴露金鑰的方式，請**不要在公共電腦或不信任的環境中使用**「記住我的 API Key」功能。此工具僅建議用於個人測試和便利性目的。

## 授權 (License)

此專案採用 [MIT License](LICENSE) 授權。

---
---

# English Version

## PDF Chapterizer - Smart PDF Chapter Splitter

**PDF Chapterizer** is a web-based tool that runs entirely in your browser. It leverages the power of Google Gemini AI to intelligently analyze a PDF's Table of Contents (TOC) and allows you to easily split a long PDF into individual chapter files for download.

## 🚀 The Pain Point It Solves

Have you ever faced this frustrating scenario?

You try to upload a lengthy e-book, a dense research paper, or an academic thesis to an AI-powered study tool like **Google NotebookLM**, only to be blocked by its **500,000-word limit per source**. Manually splitting a PDF is not only time-consuming but also prone to errors, especially when you need to process multiple documents.

**PDF Chapterizer is designed specifically to solve this problem.**

By automatically identifying the chapter structure using AI, it allows you to break down large documents into smaller, more manageable parts. You can then upload each chapter as a separate source to NotebookLM, effectively bypassing the size limitations and enabling the AI to perform a more focused and in-depth analysis on each section.

## ✨ Features

*   **🧠 Smart TOC Analysis**: Utilizes Google Gemini AI to automatically identify chapter titles and their starting page numbers from the text of the first 20 pages of a PDF.
*   **💻 Client-Side Only**: Your PDF files and API key are **never uploaded to any third-party server**. All processing (text extraction, PDF splitting) happens locally in your browser, ensuring data privacy and security.
*   **✂️ One-Click Chapter Splitting**: After analysis, it provides a clean list of all chapters with their page ranges. You can download any chapter individually.
*   **📦 Batch Download**: A "Download All" button is available to generate and download all split chapter files with a single click.
*   **🔑 API Key Persistence**: You can choose to securely store your Gemini API key in your browser's `localStorage` for convenience, so you don't have to enter it every time.

## 📖 How to Use

1.  **Get a Gemini API Key**: Visit [Google AI Studio](https://aistudio.google.com/prompts/new_chat) and click "Get API key" to obtain your free key.
2.  **Paste the API Key**: Paste the copied key into the input field on the tool.
3.  **(Optional) Remember Key**: Check the "Remember my API Key" box to save the key in your browser.
4.  **Select a PDF File**: Click the button to choose the PDF file you want to process.
5.  **Start Analysis**: Click the "1. Analyze Directory" button. The tool will start reading the file and calling the Gemini AI.
6.  **Download Chapters**: The analysis results will be displayed below. You can either click "Download" next to each chapter or use the "Download All" button to get all files at once.

## 🛠️ Tech Stack

*   **Frontend**: HTML, CSS, JavaScript (ES6+)
*   **AI Model**: Google Gemini API (gemini-1.5-flash)
*   **PDF Processing**:
    *   [PDF.js](https://mozilla.github.io/pdf.js/) for reading PDF content and extracting text.
    *   [PDF-Lib](https://pdf-lib.js.org/) for creating new PDF chapter files based on page ranges.

## ⚠️ Important Security Warning

Your API key is stored locally in your browser's `localStorage` and is sent directly from your browser to the Google API endpoint. It is **never** uploaded to or processed by our server. However, this is still a form of client-side key exposure. Please **do not use the "Remember my API Key" feature on public computers or in untrusted environments**. This tool is recommended for personal testing and convenience purposes only.

## License

This project is licensed under the [MIT License](LICENSE).
