# CQF Quant Finance Practice

A collection of Python notebooks implementing core quantitative finance methods from CQF-style coursework, including derivatives pricing, numerical methods, interest-rate modeling, and reinforcement learning.

---

## Repository Overview

This repository contains hands-on implementations of:

- Monte Carlo option pricing
- Multi-asset derivatives pricing
- Low-discrepancy / quasi-Monte Carlo simulation
- Path-dependent option pricing
- Interest-rate derivative pricing
- Binomial tree methods
- Finite-difference PDE methods
- Reinforcement learning examples using Q-learning and Deep Q-Networks

The code is organized as Jupyter notebooks for research, experimentation, and educational review.

---

## Notebooks

### `pricing.ipynb`

Implements multiple derivatives-pricing methods across equity and interest-rate products.

#### Equity Option Pricing

The notebook includes Monte Carlo pricing for:

- European calls
- European puts
- Binary options
- Single-asset lognormal equity models
- Multi-asset basket-style payoffs
- Correlated lognormal underlyings

Implemented methods include:

- Standard Monte Carlo simulation
- Cholesky-based correlated asset simulation
- Low-discrepancy sampling using Sobol sequences
- Discounted risk-neutral payoff estimation
- Standard-error estimation

#### Path-Dependent Options

Includes Monte Carlo pricing for Asian-style options using simulated geometric Brownian motion paths.

Supported payoff types include:

- Asian calls
- Asian puts
- Asian binaries

#### Interest-Rate Derivatives

Implements interest-rate simulation and bond-option pricing components using:

- Vasicek short-rate model
- Heath-Jarrow-Morton-style forward-rate simulation
- Discount-factor construction from simulated rate paths
- Bond option payoff evaluation

#### Tree-Based Pricing

Implements Cox-Ross-Rubinstein-style binomial tree pricing for:

- European call options
- European put options
- European binary options
- American call options
- American put options
- American binary options

The American option implementation supports early exercise through backward induction.

#### Finite-Difference Pricing

Implements finite-difference methods for Black-Scholes-style PDE pricing:

- Explicit finite-difference method
- Crank-Nicolson finite-difference method
- European options
- American options with early-exercise constraints
- Call, put, and binary payoffs

The notebook also contains section placeholders for:

- Asian options through explicit finite difference
- Caps and floors
- Convertible bonds with stochastic stock and interest rates

---

### `reinforcement_learning.ipynb`

Implements reinforcement learning examples from basic tabular learning to deep reinforcement learning.

#### Deep Q-Network Maze Solver

A Keras-based DQN agent learns to navigate an 8×8 grid maze from the start state to the goal while avoiding walls.

Implemented components include:

- Grid-world environment
- One-hot state encoding
- Four-action movement space
- Neural-network Q-function approximator
- Experience replay buffer
- Target network
- Epsilon-greedy exploration
- Episode-based training loop
- Maze/path visualization

#### Tabular Q-Learning Hallway Example

A simpler object-oriented Q-learning example where an agent learns to move through a 5-cell hallway to reach a terminal goal state.

Implemented components include:

- Environment class
- Agent class
- Trainer class
- Q-table learning
- Epsilon-greedy action selection
- Episode training loop

---

## Methods Covered

### Derivatives Pricing

- Risk-neutral valuation
- Monte Carlo simulation
- Quasi-Monte Carlo simulation
- Basket option pricing
- Asian option pricing
- Binary option pricing
- Binomial tree pricing
- American early-exercise logic
- Finite-difference PDE methods
- Crank-Nicolson scheme

### Interest-Rate Modeling

- Vasicek short-rate dynamics
- Forward-rate simulation
- Bond pricing from discount factors
- Bond option valuation

### Reinforcement Learning

- Q-learning
- Deep Q-Networks
- Experience replay
- Target networks
- Epsilon-greedy exploration
- Grid-world environments

---

## Tech Stack

- Python
- NumPy
- SciPy
- TensorFlow / Keras
- Jupyter Notebook

---

## Repository Structure

```text
cqf/
│
├── pricing.ipynb                  # Derivatives pricing and numerical methods
├── reinforcement_learning.ipynb   # Q-learning and DQN examples
└── README.md
```

---

## Example Topics

This repository can be used to review or demonstrate:

- How Monte Carlo pricing works under geometric Brownian motion
- How correlated multi-asset payoffs are simulated
- How Sobol low-discrepancy sequences improve simulation design
- How binomial trees handle European and American exercise
- How finite-difference grids solve option-pricing PDEs
- How short-rate models generate discount factors
- How tabular Q-learning differs from DQN-style function approximation

---

## Notes

This repository is intended for educational and research practice.

The implementations prioritize clarity and directness over production-level optimization. Some notebook sections are exploratory or partially scaffolded for future extensions.

---

## Potential Future Improvements

- Add analytical Black-Scholes benchmarks
- Add convergence diagnostics for Monte Carlo and finite-difference methods
- Add Greeks calculation
- Add implied-volatility solvers
- Complete cap/floor pricing examples
- Complete convertible bond pricing examples
- Refactor reusable pricing functions into Python modules
- Add unit tests for pricing routines
- Add plots comparing numerical methods
- Add transaction-cost-aware reinforcement learning examples

---

## Disclaimer

This repository is for educational and research purposes only.  
It does not constitute financial advice, trading advice, or investment recommendations.
