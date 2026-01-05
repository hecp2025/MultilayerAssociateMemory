# MultilayerAssociateMemory (MultilayerHNN)

Codebase for **hardware-adaptive learning** in **memristor-based associative memory** with a **multilayer** structure. :contentReference[oaicite:1]{index=1}

This repository accompanies the paper:

> **A Hardware-Adaptive Learning Algorithm for Superlinear-Capacity Associative Memory on Memristor Crossbars** :contentReference[oaicite:2]{index=2}

---

## What’s inside

- **Adaptive (hardware-aware) training** for associative memory under device non-idealities  
  - `stuck`: stuck-at-fault ratio (or related fault rate)
- **Multilayer Hopfield-style associative memory** experiments (e.g., MNIST patterns)
- Utilities and a memristor simulation module

> Note: The main entry used in the provided commands is `multilayer.py`. :contentReference[oaicite:3]{index=3}

---

## Repository structure

Typical layout:

- `multilayer.py` — main script for training / evaluation (CLI)
- `HopfiledNetwork.py` — Hopfield(-style) network implementation :contentReference[oaicite:4]{index=4}
- `utils.py` — helper functions :contentReference[oaicite:5]{index=5}
- `memristor_simulation/` — memristor/device modeling utilities :contentReference[oaicite:6]{index=6}

---

## Installation

```bash
git clone https://github.com/hecp2025/MultilayerAssociateMemory.git
cd MultilayerAssociateMemory
python -m venv .venv
# Windows: .venv\Scripts\activate
source .venv/bin/activate
