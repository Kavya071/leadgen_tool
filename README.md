
# 🔍 AI-Powered Lead Generation Tool

This project was developed as part of the **Caprae Capital AI Readiness Challenge** by **Kavya Bhardwaj**.  
It is a smart, automated tool to extract structured company data (leads) using a mix of **APIs**, **Regex**, and **AI models**.

---

## 🚀 What This Tool Does

Given a list of company names, it fetches:

- 🌐 Official Website (via Serper API)
- 📧 Emails (via Hunter.io and website scraping fallback)
- 👤 CEO Name (via DataForSEO SERP + Hugging Face AI QA model)
- 🔗 LinkedIn URL (via Google SERP matching)
- 💰 Revenue Estimates (regex from live SERPs + AI fallback)
- 👥 Employee Estimates (regex logic + Hugging Face fallback)
- 📁 Exports everything to a downloadable `.csv`

---

## 🧠 Technologies Used

| Data Field        | Powered By                                  |
|-------------------|----------------------------------------------|
| Website           | ✅ Serper API                                 |
| Emails            | ✅ Hunter.io API, ✅ Regex (fallback)          |
| CEO Name          | ✅ DataForSEO API + 🤖 Hugging Face AI        |
| LinkedIn Profile  | ✅ DataForSEO API                              |
| Revenue           | ✅ DataForSEO API, Regex, 🤖 Hugging Face AI   |
| Employees         | ✅ DataForSEO API, Regex, 🤖 Hugging Face AI   |

---

## 🧩 Smart Features

- ✅ Regex + AI fallback pipeline
- ✅ Fallback email scraping using `BeautifulSoup`
- ✅ Range filtering for employees (e.g., 1K–1M)
- ✅ Currency-aware parsing (USD, INR, Crore)
- ✅ Retry logic for missing data
- ✅ Fully exportable CSV

---

## 🧪 Example Output

| Company   | CEO             | Revenue     | Employees    |
|-----------|------------------|-------------|--------------|
| Apple     | Tim Cook         | $391.04B    | ~164,000     |
| Zomato    | Deepinder Goyal  | ₹12,114 Cr  | ~4,000       |
| Google    | Sundar Pichai    | $350.02B    | ~183,000     |

---

## 📦 How to Run

1. Install requirements:
```bash
!pip install transformers beautifulsoup4 requests
```

2. Paste the code into a Google Colab or local Python script

3. Run:
```python
companies = ["Apple", "Google", "Zomato"]
results = process_companies(companies)
```

4. Export CSV:
```python
import pandas as pd
pd.DataFrame(results).to_csv("lead_results.csv", index=False)
```

---

## 📹 Loom Demo

A walkthrough video is included explaining the functionality and showcasing real-time output.  
🔗 [Link to Loom](#) *(Insert your Loom URL here)*

---

## 📧 Contact

Feel free to connect:
- ✉️ bhardwajkavya099@gmail.com

---

**Built with 💡 by Kavya Bhardwaj**
