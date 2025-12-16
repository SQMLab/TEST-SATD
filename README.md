# 🧩 Replication Package: A First Look at the Self-Admitted Technical Debt (SATD) in Test Code

---

## 📖 Abstract

Self-Admitted Technical Debt (SATD) refers to comments in which developers explicitly acknowledge limitations, workarounds, or deferred improvements in code.  
While prior research has primarily focused on production code, this study presents the **first large-scale empirical investigation of SATD in test code**, introducing a taxonomy of 14 categories and evaluating both traditional detection tools and large language models (LLMs).

---

## 🧠 Research Questions


1. **RQ1:** What types of SATD appear in test code?
2. **RQ2:** Can existing SATD detection tools identify SATD in test code?
3. **RQ3:** Can open-source LLMs (e.g., Flan-T5) detect SATD in test code?
4. **RQ4:** Can proprietary LLMs (e.g., GPT, Gemini) detect SATD in test code?

---

## 🗂️ Dataset Description

### 1. Repository Metadata
- **File:** [repository.csv](./data/repository.csv)  
- **Description:** Metadata of 1,000 open-source Java repositories collected from GitHub, including repository URLs, stars, and size.

### 2. Comment Data

| Dataset                           | Description                                                   | File(s)                                                                                                                  |
|-----------------------------------|---------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| **All Extracted Comments**        | All extracted comments (merged from line, block, and Javadoc) | [comment.zip](./data/comment.zip)                                                                                        |
| **Detection Sets (Original)**     | 80/20 split preserving natural duplication                    | [train.csv](./data/duplicate_detect_train.csv), [test.csv](./data/duplicate_detect_test.csv)                             |
| **Detection Sets (Deduplicated)** | 80/20 split after duplicate removal                           | [train.csv](./data/unique_detect_train.csv), [test.csv](./data/unique_detect_test.csv)                                   |
| **Labeled SATD Comments**         | Manually classified SATD                                      | [satd comments.csv](./data/duplicate_satd_comment.csv), [deduplicated satd comments.csv](./data/unique_satd_comment.csv) |
| **Few-Shot Samples**              | Used for n-shot                                               | [n-shots.csv](./data/detect_n_shot.csv)                                                                                  |

### 3. Dataset Summary
- Total comments: **47,994**  
- Projects: **488**  
- SATD comments: **615 (1.28%)**  
- Non-English comments excluded: **943**  
- Auto-generated comments excluded: **1,063**

---
## License
This project is licensed under the **MIT License**. For more information, see the [LICENSE](./LICENSE).