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
| **Serial Fault Simulation (SFS)** | 8.399 | 1.00x | 99.66% | 1 | 26 (98.7% red.) |
| **Parallel Pattern Fault Simulation (PPFS)** | 1.493 | 5.63x | 99.66% | 1 | 20 (99.0% red.) |
| **Concurrent Fault Simulation (CFS)** | 10.187 | 0.82x | 99.66% | 1 | 26 (98.7% red.) |

## Undetected Faults

The following 1 faults remained undetected:

- `nc3_br5 SA1`

## Vector Budget Scaling (Design Space Exploration)

| Vectors | SFS Cov (%) | SFS Time (ms) | PPFS Cov (%) | PPFS Time (ms) | CFS Cov (%) | CFS Time (ms) |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| 2 | 49.7% | 0.561 | 49.7% | 0.479 | 49.7% | 0.117 |
| 4 | 67.7% | 0.833 | 67.7% | 0.477 | 67.7% | 0.175 |
| 8 | 82.3% | 1.042 | 82.3% | 0.495 | 82.3% | 0.223 |
| 16 | 94.6% | 1.652 | 94.6% | 0.516 | 94.6% | 0.309 |
| 32 | 98.3% | 1.436 | 98.3% | 0.503 | 98.3% | 0.478 |
| 64 | 99.0% | 1.660 | 99.0% | 0.529 | 99.0% | 0.561 |
| 128 | 99.7% | 1.850 | 99.7% | 0.550 | 99.7% | 0.864 |
| 256 | 99.7% | 2.265 | 99.7% | 0.590 | 99.7% | 1.497 |
| 512 | 99.7% | 3.040 | 99.7% | 0.653 | 99.7% | 2.936 |
| 1024 | 99.7% | 4.828 | 99.7% | 0.914 | 99.7% | 5.150 |
| 2048 | 99.7% | 8.057 | 99.7% | 1.147 | 99.7% | 9.805 |
