# Selenium Bulk Downloader (Excel Reports)

A small automation script that uses **Selenium WebDriver (Chrome)** to open a list of report URLs and trigger downloads of multiple **`.xlsx`** files.

This was created to reduce manual effort when repeatedly downloading the same set of operational spreadsheets.

> **Note:** The sample code in this repo should not include real internal URLs. Replace them with your own endpoints or keep them as placeholders.

---

## ✅ What it does

- Launches **Chrome** via Selenium
- Iterates over a list of `.xlsx` report URLs
- Opens each URL (which triggers the browser download)
- Waits briefly between downloads (`time.sleep(2)`)
- Closes the browser at the end

---

## 🧰 Tech stack

- Python 3.x
- Selenium
- ChromeDriver / Google Chrome

---

## 📁 Suggested project structure

```
selenium-bulk-downloader/
├─ download_reports.py
├─ requirements.txt
└─ README.md
```

---

## ⚙️ Setup

### 1) Install dependencies
```bash
pip install selenium
```

(Optional) create a `requirements.txt`:
```txt
selenium
```

### 2) Install Chrome + ChromeDriver
- Make sure **Google Chrome** is installed
- Ensure the **ChromeDriver** version matches your Chrome version
- Put `chromedriver` on your PATH, or provide its location in code

---

## ▶️ How to run

1. Update the script:
   - Replace the placeholder URLs with your own list
   - Adjust the sleep time if downloads are slow
2. Run:
```bash
python download_reports.py
```

---

## 🔧 Configuration ideas (recommended improvements)

To make the script more robust and “portfolio-friendly”, consider:

- Store URLs in a list and loop (instead of repeating `driver.get()` many times)
- Use **explicit waits** (WebDriverWait) instead of fixed `sleep`
- Set a custom download directory via Chrome options
- Add logging and basic error handling (retry on transient failures)
- Parameterize inputs (e.g., read report codes from a config file)

---

## 🔐 Security / Privacy

If this repo is public:
- **Do not commit internal URLs**
- **Do not commit exported files**
- Prefer `config.example.json` for placeholders and keep real config in `.gitignore`

---

## 📄 License

MIT License.
