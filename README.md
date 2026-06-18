# NLP-spam-detection-Research
Comparative study of statistical models (Naive Bayes) and Transformer architectures (BERT) for SMS spam classification, including error analysis on adversarial phishing attempts.

# SMS Spam Classification: Comparative Research Analysis

## 1. Research Objective
To evaluate and compare the effectiveness of statistical machine learning versus Transformer-based deep learning in detecting SMS spam, with a specific focus on identifying model limitations in handling context-heavy "social engineering" attacks.

## 2. Methodology
* **Data Preprocessing:** Handled class imbalance (86% Ham, 14% Spam) using standard evaluation metrics instead of simple accuracy to ensure unbiased model performance.
* **Baseline Model:** Implemented `Multinomial Naive Bayes` using a Scikit-Learn pipeline. This served as our performance benchmark for keyword-based filtering.
* **Advanced Model:** Deployed `BERT-tiny` via Hugging Face Transformers to leverage contextual semantic understanding.

## 3. Key Findings & Error Analysis
* **Performance:** The baseline Naive Bayes achieved 98% accuracy, proving highly effective for standard keyword-based spam.
* **The "Context" Challenge:** During "Out-of-Distribution" testing, I observed that even the Transformer model struggled with "Social Engineering" spam (e.g., fraudulent transactional notifications). This indicates that modern models are prone to bias when faced with sophisticated phishing attempts that mimic legitimate communication.

## 4. Evaluation Metrics
| Metric | Result |
| :--- | :--- |
| **Accuracy** | 98% |
| **Precision** | 0.96 |
| **Recall** | 0.92 |
| **F1-Score** | 0.94 |

## 5. Tools & Technologies
* **Language:** Python
* **Libraries:** `Scikit-Learn`, `Pandas`, `Hugging Face Transformers`, `PyTorch`
* **Environment:** Google Colab

## 6. Future Scope
The next phase of this research involves:
* Expanding the dataset with domain-specific phishing examples.
* Fine-tuning the Transformer model to better recognize context-heavy adversarial patterns.
