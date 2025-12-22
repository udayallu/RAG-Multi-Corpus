
# Retreival Benchmark Tool

A comprehensive evaluation tool for testing search and retrieval performance across multiple knowledge bases using cosine similarity and various information retrieval metrics.

## Features

- ✅ **Multi-source embedding loading**: Loads and concatenates embeddings from multiple JSON files
- ✅ **Query evaluation**: Evaluates queries from CSV files with supporting facts
- ✅ **Cosine similarity search**: Finds top-k most similar documents using cosine similarity
- ✅ **Relevance detection**: Automatically marks results as relevant using LLM evaluator on supporting facts
- ✅ **Comprehensive metrics**: Calculates Recall@k, Precision@k, MRR, NDCG at k and k/2
- ✅ **Aggregated analysis**: Groups results by Query Type and Enterprise Name
- ✅ **Caching**: Caches supporting fact embeddings for efficient reuse
- ✅ **Multiple output formats**: Saves detailed results as JSON and aggregated metrics as CSV

## Requirements

```bash
pip install numpy transformers torch
```

## Input Files

### 1. Embedding Model (BAAI/bge-m3)
Expected format:
```json
[
  {
    "text": "Document content...",
    "file_name": "filename.md",
    "embedding": [0.123, -0.456, ...]
  }
]
```

### 2. Queries File (CSV)
Expected format:
```csv
Enterprise Name,Query Type,Query,Supporting Facts
ZX Bank,Descriptive,"What awards did ZX Bank win?","[{""filename"": ""awards.md"", ""text"": ""Award description...""}]"
```

## Configuration

Edit the `main()` function in `search_bench.py` to configure:

```python
# Embedding files to load
parsed_data_files in /parsed-chunks & /parsed-chunks-less-tokens

# Query file
queries_file = 'Dataset categories - queries.csv'

# Output file prefix
output_prefix = 'benchmark_agentic_chunks_aggregated.json' or 'benchmark_agentic_chunks_less_tokens_aggregated.json'

# Number of results to retrieve
k = 6 and 3

```


## Output Files

### 1. Detailed Results (JSON)
`search_benchmark_detailed_results.json`:
```json
{
  "results": [
    {
      "enterprise_name": "ZX Bank",
      "query_type": "Descriptive",
      "query": "What awards...",
      "recall_at_k": 0.75,
      "precision_at_k": 0.30,
      "mrr": 0.333,
      "ndcg_at_k": 0.85,
      "search_results": [...]
    }
  ],
  "aggregations": {
    "overall": {...},
    "query_type:Descriptive": {...},
    "enterprise:ZX Bank": {...}
  }
}
```

### 2. Aggregated Results (CSV)
`search_benchmark_aggregated_results.csv`:
```csv
Category,Name,Count,Avg Recall@k,Avg Recall@k/2,Avg Precision@k,Avg Precision@k/2,Avg MRR,Avg NDCG@k,Avg NDCG@k/2
overall,overall,100,0.7500,0.6800,0.3500,0.4200,0.5500,0.8200,0.7800
query_type,Descriptive,25,0.8000,0.7200,0.4000,0.4800,0.6000,0.8500,0.8100
enterprise,ZX Bank,20,0.7800,0.7000,0.3800,0.4500,0.5800,0.8400,0.8000
```

### 3. Supporting Facts Cache

## Metrics Explained

- **Recall@k**: Proportion of relevant documents found in top-k results
- **Precision@k**: Proportion of top-k results that are relevant
- **MRR (Mean Reciprocal Rank)**: Reciprocal of the rank of the first relevant result
- **NDCG (Normalized Discounted Cumulative Gain)**: Measures ranking quality with position-based discounting


### Performance
For large datasets:
- Consider processing queries in batches
- Use GPU if available for embeddings generation
- Adjust caching strategy for very large supporting fact sets

## Notes

- Agentic chunking from raw md using gpt-4.1
- The script used the BGE-M3 embedding model with 1024 vector size. and gpt-4.1 for LLM (chunking & relevancy evaluation).
- Supporting facts are matched with results for relevancy using LLM gpt 4.1.

## License

This benchmark is part of udayallu/RAG-Multi-Corpus .

