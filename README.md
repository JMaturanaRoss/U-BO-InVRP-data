# U-BO-InVRP: Datasets and Results

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

This repository contains the datasets and computational results accompanying the paper:

> **Uncertain Bi-Objective Insular Vehicle Routing Problem: Stochastic Programming and Robust Optimization Approaches**
>
> Javier Maturana-Ross and Stefan Voß
>
> *[Journal Name]*, [Year]. DOI: [pending]

## Overview

The Uncertain Bi-Objective Insular Vehicle Routing Problem (U-BO-InVRP) addresses insular freight logistics under operational uncertainty. The problem extends the deterministic Bi-Objective Insular Traveling Salesman Problem (BO-InTSP) lineage to a multi-vessel setting where dock and vessel availability are uncertain. Two optimization paradigms are developed and compared: two-stage stochastic programming (SP) with sample average approximation, and Γ-robust optimization (RO) with budgeted uncertainty sets.

The case study is the Chiloé and Palena archipelago in southern Chile, comprising 21 islands (and isolated sectors) with 33 potential collection sites (docks), served by a fleet of vessels departing from a depot in Dalcahue.

## Repository Structure

```
U-BO-InVRP-data/
├── README.md                  # This file
├── LICENSE                    # CC BY 4.0
├── instances/
│   ├── README.md              # Instance format description
│   ├── Original5-1.csv        # 5-island test instance
│   └── Original21-1.csv       # 21-island Chiloé-Palena instance
└── results/
    ├── README.md              # Description of result files
    ├── pareto_fronts/         # Pareto front solutions (deterministic, SP, RO)
    └── tables/                # Summary tables reported in the paper
```

## Case Study

The archipelago of Chiloé and Palena is located in southern Chile (approximately 42°S). The instance data is derived from the case study originally introduced by Miranda et al. (2015) and subsequently extended by Miranda-Gonzalez et al. (2018, 2021) and Zambra-Rivera et al. (2024). The 21-island instance includes:

- **21 islands** (20 islands and one isolated continental sector) with populations ranging from approximately 160 to 600 inhabitants.
- **33 potential docks** (collection sites) distributed across the islands.
- **Distance matrix** computed from real maritime distances in nautical miles.
- **Depot** located at the port of Dalcahue.

## Instance Format

See [`instances/README.md`](instances/README.md) for a detailed description of the CSV format, column definitions, and data sources.

## Results

See [`results/README.md`](results/README.md) for a description of the output files, including Pareto front solutions under deterministic, stochastic, and robust formulations.

## Citation

If you use these datasets or results in your research, please cite:

```bibtex
@article{maturana2026ubo,
  author  = {Maturana-Ross, Javier and Vo{\ss}, Stefan},
  title   = {Uncertain Bi-Objective Insular Vehicle Routing Problem: Stochastic Programming and Robust Optimization Approaches},
  journal = {[Journal Name]},
  year    = {[Year]},
  doi     = {[pending]}
}
```

## Related Publications

The following publications provide context for the BO-InTSP lineage and the Chiloé-Palena case study:

- Miranda, P. A., Blazquez, C. A., Obreque, C., Maturana-Ross, J., & Weintraub, G. Y. (2015). An optimization-based approach for an integrated waste collection system: A real application in the southern Chile. *Transportation Research Part E*, 77, 227–247. https://doi.org/10.1016/j.tre.2015.03.002
- Miranda-Gonzalez, P. A., Maturana-Ross, J., Blazquez, C. A., & Obreque, C. (2018). Exact formulation and analysis for the bi-objective insular traveling salesman problem. *Asia-Pacific Journal of Operational Research*, 35(5), 1850034. https://doi.org/10.1142/S0217595918500343
- Miranda-Gonzalez, P. A., Maturana-Ross, J., Blazquez, C. A., & Obreque, C. (2021). The bi-objective insular traveling salesman problem with maritime and ground transportation costs. *Mathematics*, 9(21), 2641. https://doi.org/10.3390/math9212641
- Zambra-Rivera, M., Miranda-Gonzalez, P. A., Maturana-Ross, J., & Obreque, C. (2024). A multiperiod household waste collection system for a set of rural islands. *Optimization Letters*, 18, 1777–1815. https://doi.org/10.1007/s11590-024-02100-x

## License

The datasets and results in this repository are licensed under the [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/).
