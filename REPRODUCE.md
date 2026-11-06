# Reproducing this repository

Input: the Parquet files listed below, revision `fecc2c971945cacd914c63b54ee22db9149e58c9` of the `voilaj/swiss-caselaw` dataset
(`https://huggingface.co/datasets/voilaj/swiss-caselaw/resolve/fecc2c971945cacd914c63b54ee22db9149e58c9/<file>`), plus `graph/statute_references.parquet`
from the same revision, and lexifina/switzerland-law `main` for the overlay's `law_commit`.

```
python tools/build.py sh <cache with data/ and graph/> <empty folder> --today 2026-11-06
```

Needs Python 3 and `duckdb`. Gives 1,435 decision commits and one documentation commit, hash for hash.

## SHA-256 of the input files

```
f459b0bf2dd4bb4b5ada235d7f9cffac770ebf57e80cd07ef068b9a4a3fc0e76 *sh_gerichte.parquet
4f22b8f62244b1c2eb59765141e642213f55f7cbea59bfe0956a04be0ba39402 *sh_obergericht.parquet
```
