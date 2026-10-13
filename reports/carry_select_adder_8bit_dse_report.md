# Design Space Exploration Report: carry_select_adder_8bit

## Circuit Information

| Parameter | Value |
| :--- | :--- |
| Circuit Name | `carry_select_adder_8bit` |
| Primary Inputs (PIs) | 17 |
| Primary Outputs (POs) | 9 |
| Logic Gates | 71 |
| Total Circuit Nodes | 196 |
| Original Total Faults | 374 |
| Collapsed Faults | 294 (21.4% reduction) |
| Test Vectors Evaluated | 2048 |

## Algorithm Performance Comparison

| Algorithm | Time (ms) | Speedup vs SFS | Fault Coverage (%) | Undetected Faults | Compacted Test Vectors |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **Serial Fault Simulation (SFS)** | 7.666 | 1.00x | 99.66% | 1 | 26 (98.7% red.) |
| **Parallel Pattern Fault Simulation (PPFS)** | 1.425 | 5.38x | 99.66% | 1 | 20 (99.0% red.) |
| **Concurrent Fault Simulation (CFS)** | 10.760 | 0.71x | 99.66% | 1 | 26 (98.7% red.) |

## Undetected Faults

The following 1 faults remained undetected:

- `nc3_br5 SA1`

## Vector Budget Scaling (Design Space Exploration)

| Vectors | SFS Cov (%) | SFS Time (ms) | PPFS Cov (%) | PPFS Time (ms) | CFS Cov (%) | CFS Time (ms) |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| 2 | 49.7% | 0.553 | 49.7% | 0.460 | 49.7% | 0.118 |
| 4 | 67.7% | 0.796 | 67.7% | 0.469 | 67.7% | 0.160 |
| 8 | 82.3% | 1.002 | 82.3% | 0.500 | 82.3% | 0.215 |
| 16 | 94.6% | 1.305 | 94.6% | 0.498 | 94.6% | 0.292 |
| 32 | 98.3% | 1.458 | 98.3% | 0.521 | 98.3% | 0.386 |
| 64 | 99.0% | 1.615 | 99.0% | 0.524 | 99.0% | 0.573 |
| 128 | 99.7% | 1.876 | 99.7% | 0.558 | 99.7% | 0.887 |
| 256 | 99.7% | 2.339 | 99.7% | 0.579 | 99.7% | 1.494 |
| 512 | 99.7% | 2.998 | 99.7% | 0.709 | 99.7% | 2.744 |
| 1024 | 99.7% | 4.659 | 99.7% | 0.822 | 99.7% | 5.076 |
| 2048 | 99.7% | 7.770 | 99.7% | 1.190 | 99.7% | 9.890 |
