# Suri-Aral: AI-Powered Item Analysis Tool

Suri-Aral (a combination of Filipino words "Suri" for analyze and "Aral" for study) is a standalone, browser-based web application designed to help educators perform detailed item analysis on test results. It leverages the power of Google's Gemini AI to provide not just quantitative data but also qualitative insights and actionable recommendations, turning raw scores into a powerful tool for improving instruction.

The entire application runs from a single `index.html` file, requiring no server-side setup or installation.

<!-- Add a screenshot of the application here -->
<!-- !Suri-Aral Screenshot -->

## ✨ Features

- **All-in-One Interface:** From setup to final report, everything is handled in a single, user-friendly interface.
- **Flexible Data Entry:**
    - Automatically generates a data entry grid based on the number of students and items.
    - Supports manual entry by checking boxes for correct answers.
    - **Bulk upload** student scores using a simple CSV file format.
- **Real-Time Calculations:** The analysis table updates instantly as you enter data, calculating:
    - Total scores for each student.
    - Correct responses per item.
    - **Mean Percentage Score (MPS)** for each item.
    - **Mastery Levels** (Mastered, Least Mastered, Not Mastered) based on MPS.
- **Context-Aware AI Analysis:**
    - Upload the test question paper as a **PDF**. The tool extracts the questions to provide context to the AI.
    - Integrates with the **Gemini API** to generate a detailed summary, identifying learning patterns and providing actionable recommendations for the teacher.
- **Session Management:**
    - **Save** your entire session (exam details, student answers, and AI summary) to a JSON file.
    - **Load** a previous session from a JSON file to continue your work.
- **Professional Reporting:**
    - Generates a clean, printable report including exam details, the item analysis table, and the AI-generated summary.
    - A dedicated "Print Report" button formats the output perfectly.
- **Modern & Secure:**
    - Built with Tailwind CSS for a clean, responsive design.
    - Features a subtle, animated 3D background.
    - Your Gemini API key is stored only in your browser's local storage and is never sent to any server besides Google's.

## 🚀 How to Use

1.  **Open the `index.html` file** in a modern web browser like Chrome, Firefox, or Edge.
2.  **Section 1: Examination Details**
    - Fill in the details about the exam (school, subject, etc.).
    - Enter the "Total Number of Items" and "Number of Test Takers".
    - Click **Generate Data Entry Grid**.
3.  **Section 2: Data Entry**
    - **Manual Entry:** Check the box for each item a student answered correctly. Student names can be edited by clicking on them.
    - **CSV Upload:** Alternatively, prepare a `.csv` file. The first column must be the student's name, followed by columns for each item (use `1` for correct, `0` for incorrect). Click **Process CSV** to populate the grid automatically.
4.  **Section 3: Analysis & AI**
    - **Upload Questions (Recommended):** Click "Choose File" under "Upload Questions for AI Analysis" and select the PDF of your test paper. This gives the AI crucial context for its analysis.
    - **Enter API Key:** Paste your Gemini API Key into the input field. (Click "How do I get one?" for instructions).
    - **Generate Analysis:** Click the **✨ Generate AI Analysis** button. The AI will analyze the mastery levels and the corresponding questions (if provided) to generate a report.
5.  **Manage & Export**
    - **Save Data:** Click `💾 Save Data` to download a `.json` file of your current session.
    - **Load Data:** Click `📂 Load Data` to upload a previously saved `.json` file.
    - **Print Report:** Click `Print Report` to open your browser's print dialog for a clean, formatted version of the analysis.

## 🛠️ Technology Stack

- **Frontend:** HTML5, CSS3, Vanilla JavaScript (ES6+)
- **Styling:** Tailwind CSS (via CDN)
- **AI Integration:** Google Gemini API
- **Libraries:**
    - PDF.js for parsing uploaded PDF question papers.
    - Vanta.js (with Three.js) for the animated 3D background.

## ⚙️ Local Setup

This project is designed for maximum simplicity. No complex setup is required.

1.  Clone or download this repository.
2.  Ensure you have an active internet connection (for the CDN-hosted libraries to load).
3.  Open the `index.html` file directly in your web browser.

That's it! The application is ready to use.

## Getting a Gemini API Key

To use the AI analysis feature, you need a free Gemini API key.

1.  Go to Google AI Studio.
2.  Click "**Create API key**".
3.  Copy the generated key.
4.  **Important:** You must also enable the "Generative Language API" for your project in the Google Cloud Console to avoid errors. The application provides a link and instructions for this step.
5.  Paste the key into the input field in the Suri-Aral application.

---

*This tool is intended to assist educators and should be used as a supplement to professional judgment.*