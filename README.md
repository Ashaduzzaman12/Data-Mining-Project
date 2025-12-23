# iOS App Reviews Scraper & Sentiment Analysis

This project scrapes **iOS App Store reviews** for popular applications and performs **sentiment analysis** (Positive / Negative / Neutral) using **VADER Sentiment Analysis**. The results are aggregated per app and exported to a CSV file for further analysis.

The project is implemented as a **Jupyter Notebook** and is compatible with **Google Colab**.

---

## 📌 Features

* Scrapes recent App Store reviews using Apple’s public RSS feed
* Supports multiple iOS apps at once
* Performs sentiment analysis using `vaderSentiment`
* Aggregates sentiment counts overall and per app
* Exports cleaned data to a CSV file

---

## 🛠️ Technologies Used

* Python 3
* requests
* pandas
* vaderSentiment
* Jupyter Notebook / Google Colab

---

## 📂 Project Structure

```
Scrapper_app_review.ipynb   # Main notebook
ios_reviews_with_sentiment.csv  # Output file (generated after running)
README.md
```

---

## ⚙️ Installation

Install the required libraries:

```bash
pip install requests pandas vaderSentiment
```

If using **Google Colab**, the notebook already includes the installation step.

---

## ▶️ How to Use

1. Open the notebook:

   ```
   Scrapper_app_review.ipynb
   ```

2. Modify the app list if needed:

   ```python
   app_list = [
       {"name": "Facebook", "ios_id": 284882215},
       {"name": "WhatsApp Messenger", "ios_id": 310633997},
       {"name": "Instagram", "ios_id": 389801252},
   ]
   ```

3. Run all cells in order.

4. The script will:

   * Fetch reviews for each app
   * Analyze sentiment
   * Display sentiment counts
   * Save results to a CSV file

---

## 📊 Output

* **Console Output**

  * Overall sentiment distribution
  * Sentiment breakdown per app

* **CSV File**

  * `ios_reviews_with_sentiment.csv`

Example columns:

| app_name | review | rating | sentiment | compound_score |
| -------- | ------ | ------ | --------- | -------------- |

---

## 📈 Sentiment Logic

Sentiment is calculated using VADER compound scores:

* **Positive**: compound ≥ 0.05
* **Negative**: compound ≤ -0.05
* **Neutral**: otherwise

---

## 🚀 Future Improvements

* Add support for Google Play Store reviews
* Add visualization (charts & graphs)
* Improve error handling and rate limiting
* Save results to a database

---

## 👤 Author

**Amanullah**

---

## 📄 License

This project is for educational and research purposes. Feel free to modify and use it.
