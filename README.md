## 📈 High-Low Ratio Strategy Bot (Python Edition)

An algorithmic trading bot that analyzes the frequency of **higher highs** and **lower lows** to assess market momentum, combined with **moving average crossovers** for signal confirmation.

Built in Python for flexibility, speed, and transparency — this strategy is ideal for trend detection across multiple forex or crypto symbols.

---

### 🔍 Strategy Breakdown

This strategy analyzes market behavior using two signals:

- **High-Low Ratio**: The percentage of candles where the current high > previous high or the current low < previous low.
- **MA Crossovers**: Tracks short- and long-period moving averages of this ratio to trigger buy/sell signals.

> Customizable for any asset class — forex, crypto, indices — using APIs like `ccxt` or custom data feeds.

---

### 🧩 Technology Stack

| Component        | Role                                  |
|------------------|---------------------------------------|
| **Python 3.10+** | Core programming language              |
| **NumPy / pandas** | Data manipulation & calculations     |
| **Matplotlib / Plotly** | Optional visualizations         |
| **Backtrader / Custom Logic** | Strategy engine or framework |

---

### 💡 Sample Code Snippet

```python
def compute_high_low_ratio(highs, lows):
    new_highs = np.sum(highs[1:] > highs[:-1])
    new_lows  = np.sum(lows[1:] < lows[:-1])
    total = new_highs + new_lows
    ratio = (new_highs / total) * 100 if total > 0 else 50
    return ratio
```

---

### ⚠️ Disclosure & Licensing

This repo shares **concepts and key logic components**, while full execution and trading integration are **kept private** to protect IP.

- Shared under the **MIT License**
- Execution logic available for demo or discussion on request

> 📬 Get in touch: [mailto:your.email@example.com](mailto:judeekene@gmail.com)

---
