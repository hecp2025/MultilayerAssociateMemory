# SuperlinearAssociativeMemory
Codebase for hardware-adaptive learning in memristor-based associative memory with a multilayer structure.

This repository accompanies the paper:

**A Hardware-Adaptive Learning Algorithm for Superlinear-Capacity Associative Memory on Memristor Crossbars**

---

## What’s inside

- **Hardware-adaptive (device-aware) training** for associative memory under device non-idealities  
  - `variation`: device-to-device variation noise level  
  - `stuck`: stuck-at-fault ratio (or related fault rate)
- **Multilayer Hopfield-style associative memory** experiments (e.g., MNIST patterns)
- Utilities and a memristor simulation module

> Main entry script: `multilayer.py`

---

## Repository structure

Typical layout:

- `multilayer.py` — main script for training / evaluation (CLI)
- `HopfiledNetwork.py` — Hopfield(-style) network implementation
- `utils.py` — helper functions
- `memristor_simulation/` — memristor/device modeling utilities

---

## Installation

```bash
git clone https://github.com/hecp2025/MultilayerAssociateMemory.git
cd MultilayerAssociateMemory

python -m venv .venv
# Windows:
#   .venv\Scripts\activate
# macOS/Linux:
source .venv/bin/activate

pip install -r requirements.txt
```

---
## Installation
## Train
```bash
python multilayer.py \
  --dimension 784 \
  --interval 1 \
  --train-eval 'train' \
  --variation '0.0' \
  --stuck '0.0' \
  --corruption 0.05 \
  --seed 1 \
  --dataset 'mnist' \
  --binary True \
  --max-pattern 64 \
  --min-pattern 1
```
---
## Evaluate
```bash
python multilayer.py \
  --dimension 784 \
  --interval 1 \
  --train-eval 'eval' \
  --variation '0.0' \
  --stuck '0.0' \
  --corruption 0.05 \
  --seed 1 \
  --dataset 'mnist' \
  --binary True \
  --max-pattern 64 \
  --min-pattern 1
```
---
## Key CLI arguments (summary)
```bash
--dimension: input dimension (MNIST flattened is 784)

--train-eval: 'train' or 'eval'

--dataset: dataset name (e.g., 'mnist')

--binary: whether to binarize patterns

--corruption: input corruption ratio / noise level for recall tests

--variation: device variation strength (0.0 = ideal)

--stuck: stuck-at-fault ratio / level (0.0 = no faults)

--max-pattern, --min-pattern: pattern count sweep range

--seed: random seed for reproducibility

--interval: logging / evaluation interval (implementation-defined)
```

## Citation

If you use this code in academic work, please cite the associated paper:

```bibtex
@article{multilayer_associate_memory,
  title   = {A Hardware-Adaptive Learning Algorithm for Superlinear-Capacity Associative Memory on Memristor Crossbars},
  author  = {Authors},
  journal = {To appear},
  year    = {2025},
}
