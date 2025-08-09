# XAI-Survey - Replication

Repository for replicating the ANCHOR evaluation results of the paper "Benchmarking and Survey of Explanation Methods for Black Box Models".

## Setup

### 1. Clone the repository:
```sh
git clone https://github.com/DLemming/hsfd-data-mining
cd hsfd-data-mining
```

### 2. Install dependencies:
We use [uv](https://docs.astral.sh/uv/getting-started/installation/) for dependency management (faster than pip). To install all dependencies and activate venv, run:

```sh
uv sync
source .venv/bin/activate
```

Unlike the original paper, this will automatically install the correct versions of python and all dependencies. 

## Usage

Make sure you're in the project's root directory. The jupyter notebook `repro_german_anchor.ipynb` contains all the code that was used in the attempt to reproduce the original paper's results. Inside the notebook, active the `.venv` initialized by `uv`, and run experiments as you like!
