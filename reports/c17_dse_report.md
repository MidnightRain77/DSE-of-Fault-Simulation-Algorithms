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
| **Serial Fault Simulation (SFS)** | 0.067 | 1.00x | 100.00% | 0 | 10 (68.8% red.) |
| **Parallel Pattern Fault Simulation (PPFS)** | 0.044 | 1.52x | 100.00% | 0 | 7 (78.1% red.) |
| **Concurrent Fault Simulation (CFS)** | 0.040 | 1.68x | 100.00% | 0 | 10 (68.8% red.) |

## Undetected Faults

*All simulated faults were detected (100% coverage).*

## Vector Budget Scaling (Design Space Exploration)

| Vectors | SFS Cov (%) | SFS Time (ms) | PPFS Cov (%) | PPFS Time (ms) | CFS Cov (%) | CFS Time (ms) |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| 2 | 33.3% | 0.008 | 33.3% | 0.004 | 33.3% | 0.005 |
| 4 | 41.7% | 0.013 | 41.7% | 0.004 | 41.7% | 0.007 |
| 8 | 66.7% | 0.024 | 66.7% | 0.005 | 66.7% | 0.015 |
| 16 | 87.5% | 0.031 | 87.5% | 0.006 | 87.5% | 0.019 |
| 32 | 100.0% | 0.038 | 100.0% | 0.007 | 100.0% | 0.029 |
