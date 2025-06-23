# Literature Review: Neural Passage Ranking, Parameter-Efficient Fine-Tuning, and Embedding Space Analysis

## 1. Neural Passage Ranking

**Dual-Encoder vs Cross-Encoder Architectures**
- **Dual-encoders**: Separate encoders for queries and documents with efficient similarity computation (Dong et al., 2022)
- **Cross-encoders**: Joint processing of query-document pairs for nuanced relevance modeling (Lu et al., 2025; Karpukhin et al., 2020)
- **ColBERT**: Late interaction architecture balancing efficiency and effectiveness (Khattab & Zaharia, 2020)

**Key Benchmarks**
- MS MARCO dataset drives advances with models like DPR, ColBERT, and BERT-based rankers
- Recent work shows cross-encoders can rediscover semantic variants of BM25 (Lu et al., 2025)

## 2. Parameter-Efficient Fine-Tuning

**LoRA (Low-Rank Adaptation)**
- Reduces trainable parameters while maintaining performance (Hu et al., 2022)
- Targets query/value projection matrices (~3.9% of total parameters)
- **Challenge**: Limited evaluation on already domain-adapted models

**Retrieval-Specific Issues**
- IR models often start with extensive domain-specific pre-training
- Creates different optimization dynamics compared to general NLP tasks

## 3. Embedding Space Analysis

**Geometric Understanding**
- Critical for retrieval performance (Reimers & Gurevych, 2019)
- Sentence-BERT: Siamese networks for semantic sentence embeddings

**Visualization Techniques**
- **UMAP**: Preserves local and global structure for embedding analysis (McInnes et al., 2018)
- **t-SNE**: Reveals clustering patterns through local structure preservation (van der Maaten & Hinton, 2008)

**Diagnostic Value**
- Reveals degradation patterns beyond traditional metrics
- Essential for understanding fine-tuning effects on pre-optimized models

## 4. Key Insights

**Research Gaps**
- Parameter-efficient methods need evaluation on saturated benchmarks
- Traditional fine-tuning assumptions may not hold for heavily pre-trained models
- Need for hybrid approaches combining statistical (BM25) and neural methods (Robertson & Zaragoza, 2009)

## References

Dong, Z., Niu, S., Chen, J., Yang, Y., & Xie, P. (2022). Exploring dual encoder architectures for question answering. In *Proceedings of the 2022 Conference on Empirical Methods in Natural Language Processing (EMNLP)* (pp. 9520-9530).

Hu, E. J., Shen, Y., Wallis, P., Allen-Zhu, Z., Li, Y., Wang, S., Wang, L., & Chen, W. (2022). LoRA: Low-rank adaptation of large language models. In *Proceedings of the 10th International Conference on Learning Representations (ICLR)*.

Karpukhin, V., Oguz, B., Min, S., Lewis, P., Wu, L., Edunov, S., Chen, D., & Yih, W. (2020). Dense passage retrieval for open-domain question answering. In *Proceedings of the 2020 Conference on Empirical Methods in Natural Language Processing (EMNLP)* (pp. 6769-6781).

Khattab, O., & Zaharia, M. (2020). ColBERT: Efficient and effective passage search via contextualized late interaction over BERT. In *Proceedings of the 43rd International ACM SIGIR Conference on Research and Development in Information Retrieval* (pp. 39-48).

Lu, M., Chen, C., & Eickhoff, C. (2025). Cross-encoder rediscovers a semantic variant of BM25. *arXiv preprint arXiv:2502.04645*.

McInnes, L., Healy, J., & Melville, J. (2018). UMAP: Uniform manifold approximation and projection for dimension reduction. *arXiv preprint arXiv:1802.03426*.

Reimers, N., & Gurevych, I. (2019). Sentence-BERT: Sentence embeddings using Siamese BERT-networks. In *Proceedings of the 2019 Conference on Empirical Methods in Natural Language Processing and 9th International Joint Conference on Natural Language Processing (EMNLP-IJCNLP)* (pp. 3982-3992).

Robertson, S., & Zaragoza, H. (2009). The probabilistic relevance framework: BM25 and beyond. *Foundations and Trends in Information Retrieval*, 3(4), 333-389.

van der Maaten, L., & Hinton, G. (2008). Visualizing data using t-SNE. *Journal of Machine Learning Research*, 9(86), 2579-2605.
