# 🧠 AI Meeting Notes Summarizer (Malt Technical Interview Project)

This project simulates an internal productivity tool, using LLMs to summarize semi-structured meeting notes.

## 🔧 What It Does
- Parses messy meeting notes
- Extracts project name, speaker, deadline, and actions using regex
- Feeds clean input to a real HuggingFace summarization model
- Returns clean summaries for internal tools (like Malty AI)

## 💻 Tech Used
- Python 3.10
- pandas, re
- HuggingFace Transformers (`pipeline`)
- Model: `sshleifer/distilbart-cnn-12-6`

## 🛠 How to Run
```bash
pip install -r requirements.txt
jupyter notebook notebook.ipynb
