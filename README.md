# 📈 Binomial Option Pricing Calculator

This project is a simple, self-contained Python script that calculates the fair value of an option using the **Binomial Pricing Method**. It supports **American**, **European**, and **Bermudan** options, and requires **no external libraries**, making it easy to use and portable across Python environments.

---

## 📚 Background

An **option** is a financial derivative that gives the holder the right (but not the obligation) to buy or sell an asset at a pre-agreed price (strike price) within a specified time frame.

### Types of Options:
- **Call Option**: Gives the right to **buy** the asset.
- **Put Option**: Gives the right to **sell** the asset.

### Option Styles:
- **European**: Can only be exercised at maturity.
- **American**: Can be exercised at any time before or at maturity.
- **Bermudan**: Can be exercised on specific pre-determined dates.

### Binomial Pricing Method:
The binomial model constructs a tree of possible price paths that the underlying asset can take. At each node, the value of the option is calculated using a backward induction method considering the risk-free discount rate and early exercise opportunities (for American/Bermudan options).

---

## 🧮 Features

- Works with **pure Python 3**, no external packages required.
- Supports all major option types and styles.
- Visualizes the **stock price tree**.
- Customizable parameters.
- Prints final option value and internal calculations (optional).

---

## 🧾 Model Assumptions

- No dividends are paid during the life of the option.
- Risk-free rate is constant.
- The underlying asset follows a binomial up/down movement model.

---

## 🔧 Parameters

### Required Inputs:

| Variable        | Symbol | Description                                         |
|----------------|--------|-----------------------------------------------------|
| Stock Price     | `s`    | Current price of the underlying asset              |
| Exercise Price  | `x`    | Strike price of the option                         |
| Time to Maturity| `t`    | Time until option expires (in years)               |
| Risk-Free Rate  | `r`    | Annualized risk-free interest rate (decimal)       |
| Branches/Steps  | `b`    | Number of time steps in the binomial tree          |
| Volatility      | `v`    | Annualized volatility of the asset (decimal)       |

### Optional Inputs:

| Variable              | Symbol | Description                                               |
|----------------------|--------|-----------------------------------------------------------|
| Option Nationality    | `nat`  | `'A'` for American (default), `'B'` for Bermudan, `'E'` for European |
| Option Type           | `typ`  | `'C'` for Call (default), `'P'` for Put                  |
| Print Results         | `prnt` | `True` to print tree and values (default), `False` to suppress |
| Exercisable Periods   | `exP`  | List of nodes (steps) where Bermudan option can be exercised |

---
