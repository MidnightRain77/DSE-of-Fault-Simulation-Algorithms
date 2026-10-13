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
| **Serial Fault Simulation (SFS)** | 0.928 | 1.00x | 100.00% | 0 | 25 (90.2% red.) |
| **Parallel Pattern Fault Simulation (PPFS)** | 0.211 | 4.40x | 100.00% | 0 | 21 (91.8% red.) |
| **Concurrent Fault Simulation (CFS)** | 0.624 | 1.49x | 100.00% | 0 | 25 (90.2% red.) |

## Undetected Faults

*All simulated faults were detected (100% coverage).*

## Vector Budget Scaling (Design Space Exploration)

| Vectors | SFS Cov (%) | SFS Time (ms) | PPFS Cov (%) | PPFS Time (ms) | CFS Cov (%) | CFS Time (ms) |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| 2 | 37.8% | 0.086 | 37.8% | 0.054 | 37.8% | 0.031 |
| 4 | 44.9% | 0.097 | 44.9% | 0.050 | 44.9% | 0.035 |
| 8 | 52.0% | 0.137 | 52.0% | 0.051 | 52.0% | 0.050 |
| 16 | 59.2% | 0.219 | 59.2% | 0.049 | 59.2% | 0.074 |
| 32 | 69.4% | 0.322 | 69.4% | 0.053 | 69.4% | 0.131 |
| 64 | 79.6% | 0.510 | 79.6% | 0.058 | 79.6% | 0.212 |
| 128 | 89.8% | 0.768 | 89.8% | 0.081 | 89.8% | 0.322 |
| 256 | 100.0% | 0.799 | 100.0% | 0.096 | 100.0% | 0.519 |
