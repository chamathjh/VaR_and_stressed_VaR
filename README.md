# **Portfolio Value at Risk (VaR) & Stressed VaR Analysis**

## **Project Overview**

This project demonstrates **market risk measurement** using **Value at Risk (VaR)** and **Stressed VaR (sVaR)** for a portfolio of real financial assets. The project uses **Python**, **yfinance**, and **data visualization** to calculate and compare risk metrics with **industry-standard methods**.

Key methods include:

* **Parametric VaR (Variance-Covariance)**
* **Historical Simulation VaR**
* **Monte Carlo Simulation VaR**
* **Stressed VaR** (sVaR) during historical crisis periods

 ---

## **Technologies & Libraries**

* Python 3.x
* Pandas & NumPy (data manipulation & portfolio calculations)
* yfinance (real historical market data)
* Matplotlib & Seaborn (visualizations)
* SciPy (parametric VaR calculations)

Optional for interactive dashboards:

* ipywidgets

---

## **Project Structure**

```
VaR_Project/
│
├─ VaR_Calculation.ipynb       # Main notebook with VaR/sVaR computations
├─ data/                        # Folder for CSV downloads (optional)
├─ README.md                    # Project documentation
└─ requirements.txt             # Required Python packages
```

## **Usage**

1. **Download real historical stock data** for your portfolio using `yfinance`.
2. **Compute daily returns** for each asset.
3. **Specify portfolio weights** and **confidence level**.
4. **Calculate VaR** using:

   * Parametric (assumes normality)
   * Historical Simulation
   * Monte Carlo Simulation (correlated assets)
5. **Calculate Stressed VaR (sVaR)** using a historical stress period.
6. **Visualize portfolio loss distribution** and compare VaR metrics.

---

## **Results Interpretation**

* **Parametric VaR:** Quick estimate assuming normal returns. May **underestimate tail risk**.
* **Historical VaR:** Uses actual returns, better captures **fat tails**.
* **Monte Carlo VaR:** Simulates portfolio returns based on covariance, flexible for **complex portfolios**.
* **Stressed VaR:** Conservative estimate under extreme market conditions, **critical for regulatory capital**.

**Visualization:** Loss distribution histogram with VaR and sVaR lines highlights **tail risks**.

---

## **Extensions / Future Work**

* Include **Expected Shortfall (ES/CVaR)** for tail risk measurement
* Make an **interactive dashboard** with sliders for weights and confidence levels
* Incorporate **multi-period VaR** (weekly, monthly)
* Integrate **macro-economic stress scenarios** for sVaR
