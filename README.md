# AICUP-2023-Fact-Extraction-and-Verification-for-Disinformation

<p>本競賽提供一個事實資料庫及陳述句 (claim)，參賽者需建立自動化的事實檢索與查核系統，以驗證陳述句的真偽。<br />
如果陳述句能夠「支持」或「反對」事實，系統也必須透過檢索資料庫中的文章來提供證據句。
</p>

* TEAM_3517 
* Private leaderboard：0.680223 / (Rank 6 / 301)
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
### 執行流程
* combine.ipynb
   * 合併第一＆第二批資料
* TFIDF_doc5.ipynb & TFIDF_doc1.ipynb
* stage1&2.ipynb
* 5 個 stege3 .ipynb 檔
* Private.ipynb
* Ensemble.ipynb
