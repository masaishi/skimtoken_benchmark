# skimtoken Benchmark

Automated benchmark suite for [skimtoken](https://github.com/masaishi/skimtoken) - a lightweight token count estimation library.

[![PyPI](https://img.shields.io/pypi/v/skimtoken)](https://pypi.org/project/skimtoken/)
[![Crates.io](https://img.shields.io/crates/v/skimtoken)](https://crates.io/crates/skimtoken)
[![License](https://img.shields.io/github/license/masaishi/skimtoken)](https://github.com/masaishi/skimtoken/blob/main/LICENSE)

## Overview

This repository contains benchmarking tools to measure skimtoken's performance and accuracy across different estimation methods.

## Data Source

Benchmarks use the [cc100-samples](https://huggingface.co/datasets/xu-song/cc100-samples) dataset from Hugging Face, which contains the first 10,000 lines from the CC-100 dataset. This multilingual dataset includes text samples from over 100 languages, making it ideal for testing token estimation accuracy across diverse linguistic contexts.


## Usage

### Local Benchmarking

```bash
# Install dependencies
uv sync

# Run benchmark for a specific method
uv run python benchmark.py -m simple
uv run python benchmark.py -m basic
uv run python benchmark.py -m multilingual
uv run python benchmark.py -m multilingual_simple
```

### GitHub Actions

This repository includes a GitHub Action workflow for automated benchmarking:

1. Go to the [Actions tab](../../actions)
2. Select "Run Benchmark"
3. Click "Run workflow"

The workflow will:
- Install dependencies using uv
- Run benchmarks for all methods
- Update this README with the latest results
- Commit and push the changes back to the repository

## Results

Benchmark results include:
- Initialization time and memory usage
- Execution time and memory usage
- Total resource consumption
- Accuracy metrics (RMSE, error rate)
- Performance comparison with tiktoken

### Latest Benchmark Results

_Results will be automatically updated here by GitHub Actions_

## Requirements

- Python 3.9+
- [uv](https://github.com/astral-sh/uv) package manager

## License

MIT License

