# bart-text-summarizer
Text Summarizer with BART (facebook/bart-large-cnn)

# 🧠 Text Summarization with BART

This is a simple Python-based text summarization tool using the `facebook/bart-large-cnn` model from HuggingFace Transformers. It takes any long piece of English text and returns a concise summary.

## 🚀 Features

- Built using PyTorch and HuggingFace Transformers
- Accepts user input via terminal or notebook
- Returns short, readable summaries from long texts
- Perfect for news articles, essays, or long-form writing

## 📦 Requirements

- Python 3.7+
- torch
- transformers

You can install the dependencies with:

```bash
pip install torch transformers
```
🛠️ How to Run
1. Clone the repository or copy the script.
2. Run the Python file in your terminal, VS Code, or Jupyter environment:
```bash
python summarize.py
```
3. You'll be prompted to enter the text you'd like to summarize.
4. After a few seconds, the script will return a summary.

🌐 Deployment Options
✅ Local execution (CLI or Jupyter)

🖥️ Optional: can be extended to use Streamlit or Gradio for a web UI

☁️ Can be deployed to your own server or as a GitHub-hosted project

📌 Notes
This model has a max input token limit (1024). Long texts will be truncated.

Summarization is extractive + abstractive based on beam search for better coherence.
