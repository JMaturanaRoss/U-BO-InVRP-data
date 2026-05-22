# Computational Results

This directory contains the computational results reported in the paper. All results were obtained using Gurobi Optimizer with the AUGMECON2 method (Mavrotas & Florios, 2013) for generating Pareto optimal solutions.

## Directory Structure

```
results/
├── pareto_fronts/       # Pareto front solutions
│   ├── deterministic/   # Deterministic BO-InVRP front
│   ├── stochastic/      # Stochastic programming (SP) front
│   └── robust/          # Robust optimization (RO) fronts for varying Γ
└── tables/              # Summary tables from the paper
```

## Pareto Front Files

Each Pareto front CSV file contains the following columns:

| Column | Type | Description |
|--------|------|-------------|
| `solution_id` | int | Solution index on the Pareto front |
| `MTC` | float | Maritime transportation cost (objective 1) |
| `GTC` | float | Ground transportation cost (objective 2) |
| `vessels_used` | int | Number of vessels deployed |
| `docks_visited` | str | Semicolon-separated list of visited dock IDs |
| `routes` | str | Semicolon-separated vessel routes (sequence of node IDs) |
| `solve_time_s` | float | AUGMECON2 iteration solve time in seconds |

### Stochastic Programming Results

For SP solutions, the `MTC` and `GTC` columns report **expected values** across the scenario pool. Additional columns include:

| Column | Type | Description |
|--------|------|-------------|
| `VSS` | float | Value of the Stochastic Solution |
| `EVPI` | float | Expected Value of Perfect Information |

### Robust Optimization Results

For RO solutions, results are organized by budget parameter values. Each file is named according to the uncertainty budget pair (Γ_d, Γ_v). Additional columns include:

| Column | Type | Description |
|--------|------|-------------|
| `gamma_d` | int | Dock availability uncertainty budget |
| `gamma_v` | int | Vessel availability uncertainty budget |
| `PoR_MTC` | float | Price of Robustness for MTC |
| `PoR_GTC` | float | Price of Robustness for GTC |

## Summary Tables

The `tables/` directory contains CSV reproductions of the summary tables reported in the paper, including payoff tables, metric comparisons (VSS, EVPI, Price of Robustness), and front comparison statistics.

## Reproducibility

All Pareto fronts were generated using the AUGMECON2 epsilon-constraint method applied to the SP and RO formulations described in Section 4 of the paper. The deterministic and robust fronts were re-evaluated across the stochastic scenario pool to project all three fronts into a common expected-objective plane for comparison.

## References

- Mavrotas, G., & Florios, K. (2013). An improved version of the augmented ε-constraint method (AUGMECON2) for finding the exact Pareto set in multi-objective integer programming problems. *Applied Mathematics and Computation*, 219(18), 9652–9669. https://doi.org/10.1016/j.amc.2013.03.002
