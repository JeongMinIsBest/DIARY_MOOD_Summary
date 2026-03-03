# 🧠 Diary Summarization Model Using KoBART
This project presents a Korean diary summarization model built on **KoBART (Korean BART)**.  
The model is fine-tuned to generate concise **2–3 sentence summaries** of diary entries while preserving the original emotional flow and key daily events.
  
By leveraging KoBART’s strong generative capabilities, the model aims to produce summaries that remain faithful to the writer’s sentiment while delivering the core content in a compact and natural narrative form.
<br/>
<br/>

## 📚 Data Source
- **AI Hub – Summary and Report Generation Dataset**  
  https://aihub.or.kr/aihubdata/data/view.do?dataSetSn=582
- A large-scale Korean parallel dataset consisting of documents and human-written summaries across diverse domains, including daily life, administration, education, and news
- Raw document–summary pairs were extracted and **reconstructed with a focus on diary-style texts**
- Final training datasets:
  - `2~3sent.zip` (training set)
  - `2~3sent_validation.zip` (validation set)
- Summary length was constrained to **2–3 sentences** to encourage natural, narrative-style abstractive summarization
<br/>
<br/>

## ⚙️ Model Architecture
| Component | Description |
|---------|------------|
| **Base Model** | KoBART (`SKT-AI/kobart`) |
| **Task** | Text Summarization (Seq2Seq Fine-tuning) |
| **Framework** | PyTorch Lightning + Hugging Face Transformers |
| **Optimizer** | AdamW |
| **Scheduler** | Linear Warmup |
| **Loss Function** | Cross-Entropy Loss |
<br/>
<br/>

## 📦 Repository Structure
```
📦 DIARY_MOOD_Summary-main/
│
├── README.md
│   └── Project overview and documentation
│
├── 📁 model/
│   └── [Capstone Design] Diary Summarization Model using KoBART.ipynb
│       # Training and evaluation notebook
│
└── 📁 summary_raw_data/
    ├── 2~3sent.zip
    │   └── Training data (derived from AI Hub summary & report generation dataset)
    └── 2~3sent_validation.zip
        └── Validation data
```
<br/>
<br/>

*This project explores how pretrained sequence-to-sequence models can be adapted for emotionally coherent summarization in personal narrative texts.*
<br/>
<br/>
