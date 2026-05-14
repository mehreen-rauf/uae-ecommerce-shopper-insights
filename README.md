# UAE E-Commerce Buyer Psychology
## Amazon.ae Review Analysis — Apple iPad 11-inch (A16) vs Honor Pad 9

---

## Project Summary

This project analyses 191 customer reviews scraped from Amazon.ae to 
investigate how buyers of two top-selling tablets — the Apple iPad 
11-inch (A16 Chip) and Honor Pad 9, differ in their buying psychology, 
price perception, and complaint behaviour.

The core finding: Apple and Honor buyers use identical platforms and 
mention price at identical rates — but mean completely different things. 
And when things go wrong, their failure modes map directly back to what 
each buyer originally trusted.

---

## Key Findings

**1. Two completely different buying mindsets**
Apple buyers choose the product, then justify the price.
Honor buyers choose the price, then justify the product.

**2. Price language differs by brand**
Apple reviews frame price as validation — "top-notch product, 
competitive price."
Honor reviews frame price as the core reason — "worth every penny, 
nothing comes close at this price."

**3. Blame maps to trust**
Among Apple's negative reviews (classified): 50% blamed the 
platform/seller, 44% blamed the product.
Among Honor's negative reviews (classified): 71% blamed the product, 
14% blamed the platform.

**4. Star ratings do not always reflect satisfaction**
13 one-star reviews were scored Neutral by VADER — buyers expressed 
real dissatisfaction in calm, factual language that text sentiment 
alone could not detect. This highlights a key limitation of automated 
sentiment analysis.

---

## Methodology

| Step | Detail |
|------|--------|
| Data collection | Octoparse web scraping from Amazon.ae product pages |
| Products | Apple iPad 11-inch (A16 Chip) · Honor Pad 9 |
| Reviews | 191 after cleaning (Apple: 92 · Honor Pad 9: 99) |
| Translation | Arabic reviews translated to English via Octoparse |
| Cleaning | Python — removed nulls, emoji-only rows, standardised columns |
| Sentiment | VADER enhanced with Hu & Liu Opinion Lexicon + 32 custom tech words |
| Final label | Combined VADER score + star rating for more accurate classification |
| Blame analysis | Keyword classification into Platform/Seller vs Product/Brand |

---

## Tools & Libraries

- Python (Google Colab)
- Pandas — data cleaning and analysis
- VADER (vaderSentiment) — sentiment scoring
- Hu & Liu Opinion Lexicon — domain-specific lexicon enhancement
- NLTK — stopword removal and frequency analysis
- Matplotlib / Seaborn — visualisation
- Octoparse — web scraping

---

## Files in this Repository

| File | Description |
|------|-------------|
| `tablet_python_code.ipynb` | Full analysis notebook with comments |
| `Ecommerce_cleaned.xlsx` | Cleaned dataset used for analysis |

---

## Limitations

- Single platform (Amazon.ae only) — Noon.com was excluded due to 
  scraping constraints
- Small sample size (191 reviews) — findings are directional, 
  not statistically generalisable
- Translation quality — Arabic reviews translated automatically, 
  minor nuance may be lost
- VADER limitations — calm factual complaints scored as Neutral 
  despite clear dissatisfaction (documented in notebook)
- Self-selected reviews — Amazon.ae reviewers may not represent 
  all UAE tablet buyers

---

## Author

Mehreen Rauf
MSc Business Analytics — University of Wollongong in Dubai
Consumer Insights | Data Analytics | UAE Market Research

[LinkedIn](https://www.linkedin.com/in/mehreen-rauf/)
