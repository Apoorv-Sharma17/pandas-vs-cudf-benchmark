# pandas-vs-cudf-benchmark
Benchmarking NVIDIA cuDF against Pandas on ETL workloads at 1M, 5M, and 10M rows

# Pandas vs. NVIDIA cuDF — ETL Benchmark

Benchmarking CPU vs. GPU-accelerated data processing on a realistic 
ETL pipeline across 1M, 5M, and 10M rows.

## Key Results

| Dataset Size | Pandas (s) | cuDF (s) | Speedup |
|---|---|---|---|
| 1M  | 1.044 | 0.087 | 12.0x |
| 5M  | 1.492 | 0.059 | 25.3x |
| 10M | 3.032 | 0.087 | 34.9x |

**At 10M rows, NVIDIA cuDF completes the same ETL pipeline 34.9x 
faster than Pandas.**

## What's in This Repo

- `benchmark.ipynb` — Full reproducible notebook (run on Google Colab T4 GPU)
- `benchmark_results.csv` — Raw timing results
- `benchmark_results.png` — Visualization

## Run It Yourself

Open directly in Google Colab:
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1vZgAaZ-u2FawF8gxURJ6Ys-zrfdKlcJm?usp=sharing)

## The ETL Pipeline Tested
- Filter transactions above $500
- Feature engineering (high-value flag)
- Group and aggregate by category and region
- Sort by total transaction volume

## Environment
- Platform: Google Colab (NVIDIA T4 GPU)
- cuDF version: 26.02.01
- Python: 3.x

## Full Article
[Link to Towards Data Science article] — coming soon
