# Arbitrage

Cross-exchange crypto arbitrage toolkit (BitoPro ↔ Binance / OKX), with a Tk GUI and reusable exchange modules.

This repository is the canonical home after consolidation.  
The legacy mirror repository (`Arbitrage-b07109035`) should be treated as historical.

## What is included

- `test.py`: Tkinter GUI workflow + websocket market streams
- `bito_binance.py`: BitoPro/Binance arbitrage execution logic
- `bito_okx.py`: BitoPro/OKX arbitrage execution logic
- `run_gui.py`: clean entrypoint to launch the app

## Quick start

1. Install dependencies:

```bash
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install -r requirements.txt
```

2. (Recommended) start in dry-run mode:

```bash
cp .env.example .env
export ARBITRAGE_DRY_RUN=1
python run_gui.py
```

Dry-run mode keeps the full signal/decision flow but does **not** submit real orders.

## Environment variables

- `ARBITRAGE_DRY_RUN`: `1` enables simulated order fills

## Risk note

This project touches real trading APIs. Always test in dry-run/small-size mode first.

