# Credit_score_assigner

**README.md**

# DeFi Credit Scorer

A Python-based tool to compute credit scores (0–1000) for Aave v2 wallets using transaction history and an Isolation Forest model.

## Features

* Parses raw wallet transaction JSON
* Engineers meaningful on‑chain features
* Trains an Isolation Forest for outlier-based scoring
* Outputs scores as a JSON array

## Requirements

* Python 3.8+
* pandas
* scikit‑learn
* numpy

## Installation

1. Clone the repo:

   ```bash
   git clone https://github.com/yourusername/defi-credit-scorer.git
   cd defi-credit-scorer
   ```
2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

## Usage

1. Prepare your input transaction file (JSON):

   * Example: `/content/drive/MyDrive/user-wallet-transactions.json`
2. Run the scoring script:

   ```bash
   python colab_kernel_launcher.py \
     /path/to/input.json \
     /path/to/output.json \
     --contamination 0.01 \
     --n_estimators 200
   ```
3. Check your scores in the output JSON file.

## Outputs

* A JSON file with entries:

  ```json
  [
    {"userWallet": "0xABC...", "credit_score": 735},
    {"userWallet": "0xDEF...", "credit_score": 482},
    ...
  ]
  ```

## License

MIT

