# RAG-Multi-Corpus Dataset

## Overview

Retrieval-Augmented Generation (RAG) pipelines depend heavily on high‑quality, diverse reference datasets to evaluate retrieval robustness, document parsing accuracy, and end‑to‑end RAG performance. **RAG-Multi-Corpus** is a synthetic, multi-format, multi-domain dataset purpose‑built to benchmark RAG systems in realistic enterprise environments.

This dataset includes five fictional enterprise organizations spanning distinct industry verticals—automotive, cloud services, academia, technology, and banking. Each organization's data is available in multiple document formats, making this dataset ideal for testing parsers, chunking strategies, embeddings, retrievers, and full RAG pipelines.

## Key Features

* **Multi‑domain coverage** across telecom, aviation, banking, automotive, academia, and enterprise technology
* **Five fictional enterprise organizations** with realistic documentation
* **Multi‑format documents**, including:

  * PDF
  * HTML
  * DOCX
  * PPTX
  * Markdown (MD)
* **Curated Q&A set** for evaluating retrieval quality and RAG answer accuracy
* **Designed for benchmarking** document parsing, chunking, RAG retrieval, answer correctness, hallucination detection, and grounding quality

## Dataset Composition

The dataset contains documents from five enterprises. Each folder includes mixed-format files representing typical enterprise documentation such as internal guides, policies, technical sheets, product descriptions, FAQs, and reports.

| Entity / Organization     | Total Files | Formats                         | Industry                | Document Types                                                                 |
|---------------------------|-------------|----------------------------------|-------------------------|--------------------------------------------------------------------------------|
| Aventro Motors            | 51          | PDF, MD, HTML, DOCX, PPTX        | Automotive              | Vehicle specifications, service manuals, safety protocols, marketing materials, technical documentation |
| CloudWay 24               | 38          | PDF, MD, HTML, DOCX, PPTX        | Cloud & SaaS            | Service agreements, API documentation, pricing sheets, deployment guides, security policies |
| Cendara University        | 41          | PDF, MD, HTML, DOCX, PPTX        | Academia & Education    | Course catalogs, academic policies, research reports, student handbooks, administrative procedures |
| Velvera Technologies      | 39          | PDF, MD, HTML, DOCX, PPTX        | Enterprise Technology   | Product specifications, technical documentation, integration guides, release notes, support documentation |
| ZX Bank                   | 72          | PDF, MD, HTML, DOCX, PPTX        | Banking & Finance       | Account policies, compliance documentation, financial reports, service terms, regulatory guidelines |


### Query Distribution by Category

| Category     | Count | Percentage | Description                                                     |
|--------------|-------|------------|-----------------------------------------------------------------|
| Descriptive  | 138   | 17.6%      | Questions seeking factual descriptions or definitions            |
| Analytical   | 122   | 15.5%      | Questions requiring analysis, interpretation, or inference       |
| Comparative  | 139   | 17.7%      | Questions comparing entities, features, or concepts              |
| Boolean      | 108   | 13.7%      | Yes/no questions testing factual recall                          |
| Temporal     | 24    | 3.1%       | Questions involving time-based information or sequences          |
| Procedural  | 180   | 22.9%      | Questions about processes, steps, or how-to information          |
| Open-Ended  | 75    | 9.5%       | Complex questions requiring synthesis of multiple sources        |
| **Total**    | **786** | **100%**   | —                                                               |



## Benchmark Tasks

Some suggested benchmark tasks include:

1. **Document Parsing Accuracy** – Validate how effectively parsers extract content across formats.
2. **Retrieval Quality** – Use the Q&A set to test how well embedding models and retrievers surface relevant context.
3. **RAG Answer Accuracy** – Measure correctness, completeness, hallucination rate, and rule adherence.
4. **Cross‑format Consistency** – Compare performance across identical content represented in different file types.
5. **Enterprise‑scale RAG Simulation** – Build production‑like RAG systems with multi-domain, multi-format corpora.



## Contributors

| Name             | GitHub Profile                                      | LinkedIn Profile |
|------------------|-----------------------------------------------------|------------------|
| Uday Allu        | [@udayallu](https://github.com/udayallu)             | [LinkedIn](https://www.linkedin.com/in/udayallu/) |
| Sonu Kedia       | [@sonukedia55](https://github.com/sonukedia55)       | [LinkedIn](https://www.linkedin.com/in/sonukedia/) |
| Tanmay Odapally  | [@todap](https://github.com/todap)                   | [LinkedIn](https://www.linkedin.com/in/tanmay-odapally-aaa3a0203/) |


## License

This dataset is provided for research and experimentation. All content is synthetic and does not represent real organizations or confidential information.

## Citation

If you use **RAG-Multi-Corpus** in your research or product evaluation, please cite:

```
@Allu2025RAGMultiCorpus
```

## Contact

For questions or collaborations, feel free to reach out.
