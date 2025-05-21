# bart-text-summarizer
Text Summarizer with BART (facebook/bart-large-cnn)

Perfect for:
- Summarizing articles or blog posts
- Understanding large texts quickly
- NLP beginners experimenting with transformers

🧠 Model Info
This project uses the facebook/bart-large-cnn model, which is pre-trained for summarization tasks and widely used in real-world applications.

Architecture: BART (Bidirectional and Auto-Regressive Transformers)

Max input length: 1024 tokens

Output summary: customizable (length, beam search, etc.)

📦 Installation
You can run this in Google Colab or locally with Python 3.7+.

Install dependencies:
```
pip install transformers torch
```
🧾 How to Use
Just run the script, replace the text variable with your own content, and get the summary printed in the console.

Example snippet:
from transformers import BartTokenizer, BartForConditionalGeneration

tokenizer = BartTokenizer.from_pretrained("facebook/bart-large-cnn")
model = BartForConditionalGeneration.from_pretrained("facebook/bart-large-cnn")

inputs = tokenizer([your_text], max_length=1024, return_tensors='pt', truncation=True)
summary_ids = model.generate(inputs["input_ids"], max_length=100, min_length=30, num_beams=4, length_penalty=2.0, early_stopping=True)
print(tokenizer.decode(summary_ids[0], skip_special_tokens=True))

🛠️ Customize
max_length: controls how long the summary can be

min_length: ensures the summary isn’t too short

num_beams: adjusts quality/speed trade-off in generation

length_penalty: higher = more concise
