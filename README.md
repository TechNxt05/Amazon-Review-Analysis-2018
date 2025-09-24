# Amazon Electronics Reviews — Dataset-level Analysis

This project analyzes the **Amazon Reviews (2018) — Electronics** dataset  
([original source](https://nijianmo.github.io/amazon/index.html)).  

We explore ratings, review helpfulness, sentiment, and topics at the **dataset level**.  
Outputs include pros/cons sentences, topic models, and semantic search index.  
Large raw data and models are stored locally in `data/` (not committed to Git).

---

## 📂 Repository Structure

amazon-reviews-analysis/
├─ notebooks/
│ └─ Amazon_Reviews_Analysis_2018.ipynb # main Colab notebook
├─ data/ # raw data (large CSVs, FAISS index, models) — not pushed
│ └─ electronics_small.csv # (example; keep in Drive, not GitHub)
├─ outputs/ # small results safe to commit
│ ├─ top_positive_sentences.csv
│ ├─ top_negative_sentences.csv
│ ├─ lsa_topics.json
│ ├─ dataset_summary.json
│ ├─ monthly_review_counts.csv
│ └─ monthly_avg_rating.csv
├─ README.md
├─ LICENSE
└─ .gitignore


---

## 🚀 Quickstart (Google Colab)

1. Open `notebooks/amazon_reviews_colab.ipynb` in [Google Colab](https://colab.research.google.com/).
2. Mount Google Drive:
   ```python
   from google.colab import drive
   drive.mount('/content/drive')
   DATA_PATH = "/content/drive/My Drive/Amazon-Analysis/electronics_small.csv"


Run cells sequentially:

EDA: ratings distribution, helpful votes, time trends

Review-level features: lengths, helpfulness correlation

Sentence-level pros/cons extraction (VADER-based)

Topic modeling (TF-IDF + LSA)

Semantic search demo (embeddings + FAISS)

Outputs (CSV/JSON) are saved under outputs/.

📊 Features Implemented

Exploratory Data Analysis (EDA): ratings, votes, time trends

Sentiment analysis: VADER polarity vs. ratings

Sentence-level pros/cons extraction (top positive & negative sentences)

Topic discovery with TF-IDF + Latent Semantic Analysis (LSA)

Semantic search demo (Sentence-BERT + FAISS)

📦 Data & Models

Not in GitHub (large files):

electronics_small.csv (3M reviews)

reviews_index.faiss (semantic search index)

tfidf_30000.joblib, lgb_helpful_model.pkl (model artifacts)

👉 Keep these in data/ locally or in Google Drive.
To recreate them, run the notebook’s relevant cells.

🛠️ How to Run Locally

Clone this repo and install requirements:

git clone https://github.com/YOUR_USERNAME/amazon-reviews-analysis.git
cd amazon-reviews-analysis
pip install -r requirements.txt


Recommended minimal requirements.txt:

pandas
numpy
matplotlib
seaborn
plotly
scikit-learn
vaderSentiment
sentence-transformers
faiss-cpu
tqdm

📤 Push to GitHub (step-by-step)
# initialize repo (first time only)
git init
git add .
git commit -m "Initial commit: Amazon reviews analysis"

# connect to GitHub repo
git branch -M main
git remote add origin git@github.com:YOUR_USERNAME/amazon-reviews-analysis.git   # SSH
# or: git remote add origin https://github.com/YOUR_USERNAME/amazon-reviews-analysis.git   # HTTPS

# push
git push -u origin main


⚠️ Do not push raw CSVs, FAISS indexes, or model binaries — they’re too large.
Keep them in data/ (ignored by .gitignore) or store in Drive/S3.

📄 License

MIT License

🙌 Acknowledgements

Dataset: Amazon Review Data (2018)

Paper: Justifying recommendations using distantly-labeled reviews and fined-grained aspects
Jianmo Ni, Jiacheng Li, Julian McAuley (EMNLP, 2019)


---

✨ Copy this into your `README.md` file and you’re good to go.  

Do you also want me to give you a **ready `requirements.txt`** content (so you can copy–paste that too)?
