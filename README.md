# Advanced BESS Multi-Market Co-Optimization (Day-Ahead + FCR)

An enterprise-grade quantitative optimization framework designed for Battery Energy Storage Systems (BESS) co-optimizing energy arbitrage in the European EPEX Spot market alongside Frequency Containment Reserve (FCR) capacity commitments in Germany.

The model solves complex Mixed-Integer Linear Programming (MILP) formulations to maximize total asset revenue while respecting simultaneous power headroom constraints, dynamic grid limits, and state-of-the-art battery degradation costs.

---

### Visualization

The optimization engine jointly manages energy discharge/charge schedules alongside dedicated FCR reserve capacity allocation across 24-hour horizons:

<p align="center">
  <img src="bess_co_optimization_dark.gif" width="100%" alt="Multi-Market Co-Optimization Animation">
</p>

---

### Key Features
* **Multi-Market Revenue Stacking:** Simultaneously captures value from energy arbitrage (Day-Ahead) and capacity payments (FCR).
* **Joint Power Headroom Constraints:** Automatically ensures that inverter capacity is safely shared between energy dispatch and frequency regulation reserves ($P_{dispatch} + R_{fcr} \le P_{max}$).
* **Degradation-Aware Modeling:** Factoring in throughput wear-and-tear costs alongside binary mutual-exclusivity logic.
* **Dynamic Grid Injection Limits:** Adapts dispatch schedules to handle local distribution and transmission congestion limits.

---

### Project Structure
```text
bess-multi-market-optimizer/
│
├── notebooks/
│   └── co_optimization_demo.ipynb
├── bess_co_optimization_dark.gif
├── README.md
└── requirements.txt
