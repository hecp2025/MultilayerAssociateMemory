# MultilayerAssociateMemory (MultilayerHNN)

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
