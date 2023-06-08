# AICUP-2023-Fact-Extraction-and-Verification-for-Disinformation

* TEAM_3517 
* Private leaderboard：0.680223 / Rank 6
* Environment: Colab Pro
    * GPU: NVIDIA A100-SXM4-40GB
 * [Download checkpoints](https://drive.google.com/file/d/12m8aVyHx8xZNr6A6dSZQXQDj_Q8-xVfW/view?usp=sharing)

## Install Package
```bash
pip install -r requirements.txt
```

## Folder Structure

```
│── data                           # 放置資料（包含各階段產生的資料）
│   ├── public_train_1.jsonl       # 第一批釋出資料
│   ├── public_train_2.jsonl       # 第二批釋出資料
│   ├── public_train_new.jsonl     # 合併第一＆第二批後的資料
│   ├── dict.txt.big               # jieba dict
│   └── wiki-pages 
├── preprocess                     
│   └── combine.ipynb              # 用於合併第一＆第二批資料
├── TF-IDF                         # Part 1 TF-IDF
│   ├── TFIDF_doc5.ipynb
│   ├── TFIDF_doc1.ipynb
│   └── tfidf_utils.py  
├── stage1&2.ipynb   
├── stege3_1(hfl_chinese-roberta-wwm-ext-large).ipynb  
├── stege3_2(bert-base-chinese).ipynb  
├── stege3_3(hfl_chinese-bert-wwm-ext).ipynb   
├── stege3_4(hfl_chinese-macbert-large).ipynb             
├── stege3_5(hfl_chinese-lert-large).ipynb
├── Private.ipynb                   # 處理 private 資料
├── Ensemble.ipynb
├── checkpoints                     # 存放模型
│   ├── sent_retrieval
│   └── claim_verification
├── dataset.py
├── utils.py
├── requirements.txt
├── fig
│   ├── Data_format.png
│   └── Evaluation.png
└── ...
```
### 執行流程(順序)
1. combine.ipynb (合併第一＆第二批資料)
2. TFIDF_doc5.ipynb & TFIDF_doc1.ipynb
3. stage1&2.ipynb
4. 5 個 stege3 .ipynb 檔
5. Private.ipynb
6. Ensemble.ipynb
