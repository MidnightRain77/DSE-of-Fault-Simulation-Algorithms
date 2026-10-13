# Design Space Exploration Report: c17

## Circuit Information

| Parameter | Value |
| :--- | :--- |
| Circuit Name | `c17` |
| Primary Inputs (PIs) | 5 |
| Primary Outputs (POs) | 2 |
| Logic Gates | 6 |
| Total Circuit Nodes | 19 |
| Original Total Faults | 34 |
| Collapsed Faults | 24 (29.4% reduction) |
| Test Vectors Evaluated | 32 |

## Algorithm Performance Comparison

| Algorithm | Time (ms) | Speedup vs SFS | Fault Coverage (%) | Undetected Faults | Compacted Test Vectors |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **Serial Fault Simulation (SFS)** | 0.099 | 1.00x | 100.00% | 0 | 10 (68.8% red.) |
| **Parallel Pattern Fault Simulation (PPFS)** | 0.050 | 1.98x | 100.00% | 0 | 7 (78.1% red.) |
| **Concurrent Fault Simulation (CFS)** | 0.059 | 1.68x | 100.00% | 0 | 10 (68.8% red.) |

## Undetected Faults

*All simulated faults were detected (100% coverage).*

## Vector Budget Scaling (Design Space Exploration)

| Vectors | SFS Cov (%) | SFS Time (ms) | PPFS Cov (%) | PPFS Time (ms) | CFS Cov (%) | CFS Time (ms) |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| 2 | 33.3% | 0.015 | 33.3% | 0.008 | 33.3% | 0.007 |
| 4 | 41.7% | 0.020 | 41.7% | 0.007 | 41.7% | 0.010 |
| 8 | 66.7% | 0.034 | 66.7% | 0.007 | 66.7% | 0.021 |
| 16 | 87.5% | 0.043 | 87.5% | 0.009 | 87.5% | 0.028 |
| 32 | 100.0% | 0.055 | 100.0% | 0.011 | 100.0% | 0.042 |
