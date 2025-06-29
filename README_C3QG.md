
# 🧠 C3QG: Context-Controlled, Explainable, and Efficient Question Generation

This repository implements **C3QG**, a transformer-based question generation system built on top of FLAN-T5 with explainable and controllable output. It is designed for applications in **education**, **assessment**, and **AI transparency**.

Developed by [Phung Thao Vi](mailto:phungvi08123@gmail.com), [Satyam Mishra](mailto:satyam.entrprnr@gmail.com), [Vishwanath Bijalwan](mailto:vishwanath.bijalwan@gmail.com), and [Duc Tan Tran](mailto:tan.tranduc@phenikaa-uni.edu.vn).

---

## 🚀 Features

- ✅ **Instruction-tuned FLAN-T5** for natural and context-aware question generation
- ✅ **Context-controlled prompting** (works with single/multi-paragraph inputs)
- ✅ **Difficulty adjustment & beam sampling**
- ✅ **Token-level explainability** via **SHAP**
- ✅ **Multi-metric evaluation**: ROUGE, METEOR, BERTScore, CrossEntropy
- ✅ **Expert validation** and educational alignment (e.g., Bloom's Taxonomy)

---

## 📂 Repository Structure

```
.
├── Final_C3QG.ipynb               # Main notebook (full implementation and results)
├── Final_Complete_of_Question_Gen.ipynb  # Optional cleaner version of QG pipeline
├── README.md                      # You're here!
```

---

## 🛠️ Installation

To run the notebook in Google Colab:

1. Open `Final_C3QG.ipynb` in Colab
2. Ensure you are using a GPU Runtime (`Runtime > Change runtime type > GPU`)
3. Run all cells

If running locally:

```bash
pip install transformers datasets shap evaluate nltk
```

---

## 📚 Dataset

The system is trained and evaluated using:

- **SQuAD v2.0** (via HuggingFace Datasets)
- Augmented with: Wikipedia passages + Back-translation + Synonym replacement

---

## 📈 Evaluation Metrics

| Metric      | Purpose                        |
|-------------|--------------------------------|
| ROUGE       | Lexical overlap                |
| METEOR      | Paraphrastic fluency           |
| BERTScore   | Semantic similarity (F1)       |
| CrossEntropy| Training signal                |
| SHAP        | Token-level model attribution  |

---

## 💡 Sample Usage

```python
context = "Renewable energy is becoming a critical part of global sustainability efforts."
generate_question(context, num_questions=3)
```

Returns:
- "What role does renewable energy play in sustainability?"
- "Why are countries investing in renewable energy?"
- "How does renewable energy help fight climate change?"

---

## 📊 Results

- +4.2% improvement in BERTScore F1 over T5/BART baselines
- +3.8% better METEOR fluency
- SHAP visualizations reveal interpretable token contributions
- Adaptive difficulty shows alignment with educational needs

---

## 📌 Limitations

- Current version is trained on general-purpose text, not domain-specific
- Performance in zero-resource or cross-lingual settings is untested
- SHAP visualizations are slower on longer contexts

---

## 📄 Citation

If you use this work, please cite:

> Phung Thao Vi, Satyam Mishra, Vishwanath Bijalwan, Duc Tan Tran.  
> *C3QG: Context-Controlled, Explainable, and Efficient Question Generation with Transformers*. (2025)

---

## 🤝 Acknowledgements

Special thanks to Vision Mentors Vietnam and SR University for infrastructure support.

---

## 📬 Contact

For collaborations or questions, feel free to reach out via email:
- [phungvi08123@gmail.com](mailto:phungvi08123@gmail.com)
- [satyam.entrprnr@gmail.com](mailto:satyam.entrprnr@gmail.com)
