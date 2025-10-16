## 🧠 KoBART를 이용한 일기 요약 모델  

이 프로젝트는 KoBART(Korean BART)를 활용하여 한국어 일기 데이터를 2 ~ 3문장으로 요약하는 자연어 생성 모델입니다.  
KoBART를 파인 튜닝하여 일상의 감정 흐름을 유지하면서도 핵심 내용을 간결하게 전달하도록 설계되었습니다.
<br/>
<br/>

### 📚 데이터 출처

- [AI Hub - 요약문 및 레포트 생성 데이터](https://aihub.or.kr/aihubdata/data/view.do?dataSetSn=582)
- 다양한 도메인(일상, 행정, 교육, 뉴스 등)의 문서와 요약문으로 구성된 한국어 병렬 데이터셋
- 원문(`text`)과 요약문(`summary`)을 추출 후, **일기체 데이터 중심으로 재구성**
- 최종 학습 데이터: `2~3sent.zip` (train), `2~3sent_validation.zip` (validation)
- 요약문 길이는 2~3문장으로 제한하여 자연스러운 서술형 요약에 적합하게 조정
<br/>
<br/>

## ⚙️ 모델 구조

| 항목 | 내용 |
|------|------|
| **기반 모델** | [KoBART (SKT-AI/kobart)](https://github.com/SKT-AI/KoBART) |
| **Task** | Text Summarization (Seq2Seq Fine-tuning) |
| **Framework** | PyTorch Lightning + Transformers |
| **Optimizer** | AdamW |
| **Scheduler** | Linear Warmup |
| **Loss Function** | Cross Entropy Loss |
<br/>
<br/>

## 📦 레포지터리 구조

```
📦 DIARY_MOOD_Summary-main/
│
├── README.md                                  # 프로젝트 설명
│
├── 📁 model/
│   └── [캡스톤디자인]KoBART를_이용한_일기_요약_모델_.ipynb   # 학습 및 테스트 노트북
│
└── 📁 summary_raw_data/
    ├── 2~3sent.zip                            # 학습 데이터 (AI Hub 요약문 및 레포트 생성 기반)
    └── 2~3sent_validation.zip                 # 검증 데이터
```
<br/>
<br/>



