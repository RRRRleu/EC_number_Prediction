# EC
Prediction of EC number
This project focuses on enzyme function prediction by leveraging both protein sequence and structure embeddings, combined with a hierarchical learning strategy that mirrors the layered nature of EC (Enzyme Commission) numbers.

We extract protein representations from large-scale pretrained models:

ProtTrans for capturing sequence semantics

ESMFold for incorporating structural context

These embeddings are fused and used to train a model under hierarchical supervision, including:

🧭 Hierarchical Contrastive Loss – aligns proteins with similar EC levels

📊 Hierarchical Ranking Loss – penalizes misclassifications based on their depth in the EC tree

To improve interpretability and performance, we introduce EC-level embedding centers, allowing predictions to be made layer-by-layer, from top-level class down to the most specific functional category.
