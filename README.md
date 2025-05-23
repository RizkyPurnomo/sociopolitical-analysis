# Sentiment and Emotion Analysis on Indonesian Sociopolitical Issues

Sentiment and Emotion Analysis on Indonesian Sociopolitical Issues is an NLP-powered project that explores how Indonesians react to key sociopolitical events through their online conversations—primarily on X (formerly Twitter). The project covers multiple case studies such as the IHSG stock market crash, the #TolakUUTNI movement, and the Danantara discourse.

Using a combination of pre-trained models (Hugging Face) and large language models (LLMs), the project performs sentiment and emotion labeling, temporal analysis, and topic modeling. Visualizations and custom model training are included to deliver a deeper understanding of public opinion in real time.
 
So far, I’ve written three Medium articles based on these projects:
- Danantara: [Kata Netizen soal Danantara](https://medium.com/@data.rizkydwi/kata-netizen-soal-danantara-51130a472137)
- IHSG's Crash: [Decoding IHSG’s 18th March 2025 Drop using Sentiment, Emotion, and Keyword Analysis \(with Code!\)](https://medium.com/@data.rizkydwi/decoding-ihsgs-18th-march-2025-crash-using-sentiment-emotion-and-keyword-analysis-with-code-3b2f8779b60b)
- #TolakUUTNI: [Fine-Tuning BERT for Sentiment and Emotion Analysis for Indonesian Sociopolitical Issues](https://medium.com/@data.rizkydwi/fine-tuning-bert-for-sentiment-and-emotion-analysis-for-indonesian-sociopolitical-issues-7963bc6a7343)

This repository includes the IHSG and #TolakUUTNI projects. The Danantara notebook isn’t included because it’s a bit too chaotic to share (for now!) lol.

---

## Reports
<p align="center">
  <img src="reports\danantara_llm_emotion.png" width="50%" />
  <img src="reports\danantara_llm_sentiment.png" width="50%" />
</p>
<p align="center">
  <img src="reports\danantara_wordcloud_anger" width="33%" />
  <img src="reports\danantara_wordcloud_fear.png" width="33%" />
  <img src="reports\danantara_wordcloud_trust.png" width="33%" />
</p>
<p align="center">
  <img src="reports\danantara_wordcloud_positive" width="33%" />
  <img src="reports\danantara_wordcloud_neutral.png" width="33%" />
  <img src="reports\danantara_wordcloud_negative.png" width="33%" />
</p>
<p align="center">
  <img src="reports\ihsg_llm_emotion_otime1" width="33%" />
  <img src="reports\ihsg_llm_sentiment_otime3.png" width="33%" />
</p>
<p align="center">
  <img src="reports\ihsg_llm_sentiment" width="33%" />
  <img src="reports\ihsg_llm_emotion.png" width="33%" />
</p>


Step-by-step explanations of the analysis are written in the articles, you can take a quick look, but here is the essential steps:
- Mine the data — Most of it came from X (formerly Twitter).
- Clean and transform — X data can be... quite messy.
- Label the data — Using both Hugging Face models and API-based LLMs (like DeepSeek).
- Analyze and visualize — Sentiment, emotion, time-based trends, and more.
- Model topics and extract keywords — To understand deeper public discourse.
- (Optional) Fine-tune a model — Trained a BERT model specifically for Indonesian sociopolitical sentiment & emotion classification.

## Libraries used
- `pandas` for data manipulation and I/O.
- `transformers`, for labeling and training models.
- `groq` to call LLMs via API (used DeepSeek).
- `re` for data cleaning and keyword extraction.
- `plotly` and `Kaleido` for interactive and exportable visualizations (I’m a big `plotly` fan!).
- `datasets` to load and prepare the data before training 
- `evaluate` for model evaluation metrics.
- `wandb` for experiment tracking and result logging.
- `huggingface_hub` to push fine-tuned models to the Hugging Face Model Hub.