# 📚 Amazon Kindle Bestseller Data Extraction & Structuring Pipeline

A fully automated data pipeline built using **n8n** to scrape, process, and structure Amazon Kindle bestseller data (Paranormal Romance category), and export it into structured datasets for analysis.

---

## 🚀 Overview

This project extracts bestseller book data from Amazon, enriches it with detailed metadata, cleans and normalizes the information, and stores it in:

- 📄 CSV file
- 📊 Google Sheets dataset

It is designed for **data analysis, machine learning pipelines, and research use cases**.

---

## ⚙️ Workflow Architecture

The pipeline consists of the following stages:

### 1. Scraping Bestseller Page
- Fetches the Amazon bestseller listing page
- Extracts:
  - Rank
  - Title
  - Author
  - Rating
  - Reviews
  - Price
  - Product URL

---

### 2. Data Preprocessing
- Removes duplicate URLs
- Splits book entries into individual items
- Applies rate limiting to avoid blocking

---

### 3. Detailed Page Scraping
- Visits each book’s page
- Extracts:
  - Description
  - Publisher
  - Publication Date
  - Structured metadata (JSON-LD)

---

### 4. Data Enrichment
- Parses metadata scripts
- Extracts:
  - Clean descriptions
  - Publisher details
  - Accurate publication dates

---

### 5. Data Cleaning & Normalization
- Converts ratings → numeric format
- Extracts review counts
- Cleans price values
- Standardizes dates (ISO format)
- Fixes relative URLs → absolute URLs

---

### 6. Final Structuring
Structured dataset includes:

| Field | Description |
|------|------------|
| Rank | Bestseller ranking |
| Title | Book title |
| Author | Author name |
| Rating | Numeric rating |
| Reviews | Number of reviews |
| Price | Book price |
| URL | Product link |
| Description | Book summary |
| Publisher | Publisher name |
| Publication_Date | Release date |

---

### 7. Data Export
- 📄 CSV File (`amazon_bestsellers.csv`)
- 📊 Google Sheets integration

---

## 🛠️ Tech Stack

- **n8n** → Workflow automation
- **HTTP Requests** → Web scraping
- **HTML Parsing** → Data extraction
- **JavaScript (Code Nodes)** → Data transformation
- **Google Sheets API** → Data storage

---

## 📂 Workflow File

The complete workflow configuration is available here:  
👉 :contentReference[oaicite:0]{index=0}

---

## 🧠 Key Features

- 🔄 End-to-end automation
- 🧹 Data cleaning & normalization
- 📊 Structured dataset generation
- ⚡ Rate-limited scraping (safe execution)
- 🔗 Metadata enrichment using JSON-LD
- ☁️ Cloud export (Google Sheets)

---

## ⚠️ Disclaimer

- This project is for **educational and research purposes only**
- Ensure compliance with Amazon’s **Terms of Service**
- Avoid aggressive scraping (rate limiting is implemented)

---

## 📈 Future Improvements

- Add proxy rotation for large-scale scraping
- Integrate database (PostgreSQL / MongoDB)
- Build dashboard (Next.js / Streamlit)
- Add ML model for bestseller prediction
- Automate daily/weekly scheduled runs

---

## 🤝 Contributing

Contributions are welcome!  
Feel free to fork, improve, and submit a PR.

---

## 📬 Contact

If you have any questions or ideas, feel free to reach out!

---

⭐ If you found this useful, consider giving it a star!
