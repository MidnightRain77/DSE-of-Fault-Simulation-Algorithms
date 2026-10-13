# Design Space Exploration Report: comparatOR_4bit_structural

## Circuit Information

| Parameter | Value |
| :--- | :--- |
| Circuit Name | `comparatOR_4bit_structural` |
| Primary Inputs (PIs) | 8 |
| Primary Outputs (POs) | 3 |
| Logic Gates | 23 |
| Total Circuit Nodes | 73 |
| Original Total Faults | 140 |
| Collapsed Faults | 98 (30.0% reduction) |
| Test Vectors Evaluated | 256 |

## Algorithm Performance Comparison

| Algorithm | Time (ms) | Speedup vs SFS | Fault Coverage (%) | Undetected Faults | Compacted Test Vectors |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **Serial Fault Simulation (SFS)** | 1.371 | 1.00x | 100.00% | 0 | 25 (90.2% red.) |
| **Parallel Pattern Fault Simulation (PPFS)** | 0.267 | 5.13x | 100.00% | 0 | 21 (91.8% red.) |
| **Concurrent Fault Simulation (CFS)** | 0.838 | 1.64x | 100.00% | 0 | 25 (90.2% red.) |

## Undetected Faults

*All simulated faults were detected (100% coverage).*

## Vector Budget Scaling (Design Space Exploration)

| Vectors | SFS Cov (%) | SFS Time (ms) | PPFS Cov (%) | PPFS Time (ms) | CFS Cov (%) | CFS Time (ms) |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| 2 | 37.8% | 0.095 | 37.8% | 0.071 | 37.8% | 0.038 |
| 4 | 44.9% | 0.124 | 44.9% | 0.068 | 44.9% | 0.045 |
| 8 | 52.0% | 0.175 | 52.0% | 0.068 | 52.0% | 0.062 |
| 16 | 59.2% | 0.272 | 59.2% | 0.069 | 59.2% | 0.096 |
| 32 | 69.4% | 0.413 | 69.4% | 0.073 | 69.4% | 0.152 |
| 64 | 79.6% | 0.615 | 79.6% | 0.081 | 79.6% | 0.254 |
| 128 | 89.8% | 0.878 | 89.8% | 0.104 | 89.8% | 0.426 |
| 256 | 100.0% | 1.046 | 100.0% | 0.137 | 100.0% | 0.722 |
