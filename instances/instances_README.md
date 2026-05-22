# Instance Data

This directory contains the instance files for the Uncertain Bi-Objective Insular Vehicle Routing Problem (U-BO-InVRP). Each instance is provided as a CSV file.

## Available Instances

| File | Islands | Docks | Description |
|------|---------|-------|-------------|
| `Original5-1.csv` | 5 | — | Small test instance for validation |
| `Original21-1.csv` | 21 | 33 | Full Chiloé-Palena archipelago instance |

## CSV Format

### Node Data

| Column | Type | Description |
|--------|------|-------------|
| `node_id` | int | Unique identifier for each node (0 = depot) |
| `island_id` | int | Island to which the dock belongs (0 for the depot) |
| `node_type` | str | `depot`, `dock`, or `transfer_port` |
| `latitude` | float | Geographic latitude (decimal degrees) |
| `longitude` | float | Geographic longitude (decimal degrees) |
| `num_docks` | int | Number of potential docks at this island |

### Distance Matrix

The inter-node distance matrix is included as a square CSV file where entry (i, j) represents the maritime distance in nautical miles between nodes i and j. Distances were computed using real shortest maritime routes between nodes.

## Data Sources

- **Island population and waste generation data**: Solid Waste Group at PUCV (GRS, 2009); Chilean National Statistics Institute (INE) census projections.
- **Maritime distances**: Computed from real navigation routes in the Chiloé-Palena archipelago.
- **Vessel parameters**: Volume capacity of 30 m³, navigation speed of 9 knots, maximum daily operation time of 11 hours, service time of 30 minutes per dock.

## Notes

- The 21-island instance includes 20 islands and one isolated continental sector (Ayacara Buill).
- The depot is located at the port of Dalcahue.
- Node identifiers and island assignments are consistent with the numbering used in Miranda et al. (2015) and Zambra-Rivera et al. (2024).
