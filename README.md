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

### 1. Aventro Motors

* **Total Files:** 51
* **Formats:** PDF, MD, HTML, DOCX, PPTX
* **Industry:** Automotive
<img src="https://raw.githubusercontent.com/udayallu/RAG-Multi-Corpus/main/metadata/Aventro%20Motors.jpg" width="120"/>

### 2. CloudWay 24

* **Total Files:** 38
* **Formats:** PDF, MD, HTML, DOCX, PPTX
* **Industry:** Cloud & SaaS
<img src="https://github.com/udayallu/RAG-Multi-Corpus/blob/main/metadata/Cloudway%2024.jpg" width="120"/>

### 3. Cendara University

* **Total Files:** 41
* **Formats:** PDF, MD, HTML, DOCX, PPTX
* **Industry:** Academia & Education
<img src="https://github.com/udayallu/RAG-Multi-Corpus/blob/main/metadata/Cendara%20University.jpg" width="120"/>

### 4. Velvera Technologies

* **Total Files:** 39
* **Formats:** PDF, MD, HTML, DOCX, PPTX
* **Industry:** Enterprise Technology
<img src="https://github.com/udayallu/RAG-Multi-Corpus/blob/main/metadata/Velvera%20Technologies.jpg" width="120"/>

### 5. ZX Bank

* **Total Files:** 72
* **Formats:** PDF, MD, HTML, DOCX, PPTX
* **Industry:** Banking & Finance
<img src="https://github.com/udayallu/RAG-Multi-Corpus/blob/main/metadata/zx%20bank.jpg" width="120"/>

## Benchmark Tasks

Some suggested benchmark tasks include:

1. **Document Parsing Accuracy** – Validate how effectively parsers extract content across formats.
2. **Retrieval Quality** – Use the Q&A set to test how well embedding models and retrievers surface relevant context.
3. **RAG Answer Accuracy** – Measure correctness, completeness, hallucination rate, and rule adherence.
4. **Cross‑format Consistency** – Compare performance across identical content represented in different file types.
5. **Enterprise‑scale RAG Simulation** – Build production‑like RAG systems with multi-domain, multi-format corpora.

## Folder Structure

```
RAG-Multi-Corpus/
 ├── Aventro Motors/
 ├── CloudWay 24/
 ├── Cendara University/
 ├── Velvera Technologies/
 ├── ZX Bank/
 ├── metadata/
 └── qa_dataset.json
```

## Contributors

| Name        | GitHub Profile |
|-------------|----------------|
| Uday Allu   | [@udayallu](https://github.com/udayallu) |
| Sonu Kedia   | [@sonukedia55](https://github.com/sonukedia55) |
| Tanmay Odapally  | [@todap](https://github.com/todap) |


## License

This dataset is provided for research and experimentation. All content is synthetic and does not represent real organizations or confidential information.

## Citation

If you use **RAG-Multi-Corpus** in your research or product evaluation, please cite:

```
@Allu2025RAGMultiCorpus
```

## Contact

For questions or collaborations, feel free to reach out.
