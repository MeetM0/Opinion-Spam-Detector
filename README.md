# Opinion-Spam-Detector
Fake reviews — whether AI-generated, incentivized, or bot-written — are a growing trust and safety problem across e-commerce and review platforms. Deceptive reviews often show identifiable patterns: generic/templated praise lacking specific product detail, sentiment that doesn't match the star rating, and unnatural repetition across reviews.

🚧 Actively in development. This README will be updated as each stage is completed.

- [x] Dataset exploration and preprocessing
- [ ] Baseline model (TF-IDF + Logistic Regression)
- [ ] Transformer fine-tuning (DistilBERT via HuggingFace)
- [ ] Evaluation (precision/recall/F1, confusion matrix)
- [ ] Feature analysis (linguistic markers of deceptive text)
- [ ] Rating-sentiment mismatch feature extension

## Planned Approach

1. **Data**: Deceptive Opinion Spam Corpus (Ott et al., Cornell) — labeled
   genuine vs. fabricated hotel reviews.
2. **Baseline**: TF-IDF features + Logistic Regression, to establish a
   simple reference point before adding model complexity.
3. **Main model**: Fine-tune DistilBERT (HuggingFace Transformers, PyTorch)
   for binary classification (genuine vs. deceptive).
4. **Evaluation**: Per-class precision/recall/F1 and confusion matrix
   analysis, not just overall accuracy, since class balance and error
   type matter more than raw accuracy for this kind of task.
5. **Feature analysis**: Examine which words/phrases the model associates
   with deceptive text, and test whether adding star-rating as an input
   feature improves detection (rating-sentiment mismatch is a known
   signal in deceptive review research).
