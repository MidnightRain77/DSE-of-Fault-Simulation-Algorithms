# Design Space Exploration Report: alu_6bit_gate_level

## Circuit Information

| Parameter | Value |
| :--- | :--- |
| Circuit Name | `alu_6bit_gate_level` |
| Primary Inputs (PIs) | 15 |
| Primary Outputs (POs) | 7 |
| Logic Gates | 80 |
| Total Circuit Nodes | 236 |
| Original Total Faults | 458 |
| Collapsed Faults | 328 (28.4% reduction) |
| Test Vectors Evaluated | 32768 |

## Algorithm Performance Comparison

| Algorithm | Time (ms) | Speedup vs SFS | Fault Coverage (%) | Undetected Faults | Compacted Test Vectors |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **Serial Fault Simulation (SFS)** | 436.207 | 1.00x | 98.17% | 6 | 88 (99.7% red.) |
| **Parallel Pattern Fault Simulation (PPFS)** | 24.075 | 18.12x | 98.17% | 6 | 74 (99.8% red.) |
| **Concurrent Fault Simulation (CFS)** | 171.967 | 2.54x | 98.17% | 6 | 88 (99.7% red.) |

## Undetected Faults

The following 6 faults remained undetected:

- `s0_br3 SA1`
- `s0_br5 SA1`
- `s0_br7 SA1`
- `s0_br9 SA1`
- `s0_br11 SA1`
- `s0_br13 SA1`

## Vector Budget Scaling (Design Space Exploration)

| Vectors | SFS Cov (%) | SFS Time (ms) | PPFS Cov (%) | PPFS Time (ms) | CFS Cov (%) | CFS Time (ms) |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| 2 | 18.6% | 0.561 | 18.6% | 0.576 | 18.6% | 0.065 |
| 4 | 27.7% | 0.912 | 27.7% | 0.528 | 27.7% | 0.081 |
| 8 | 32.3% | 1.376 | 32.3% | 0.534 | 32.3% | 0.118 |
| 16 | 39.3% | 2.219 | 39.3% | 0.534 | 39.3% | 0.189 |
| 32 | 46.3% | 3.834 | 46.3% | 0.551 | 46.3% | 0.320 |
| 64 | 53.4% | 6.309 | 53.4% | 0.586 | 53.4% | 0.518 |
| 128 | 60.4% | 10.417 | 60.4% | 0.808 | 60.4% | 0.914 |
| 256 | 67.4% | 16.993 | 67.4% | 1.247 | 67.4% | 1.708 |
| 512 | 72.6% | 26.667 | 72.6% | 1.879 | 72.6% | 3.108 |
| 1024 | 76.8% | 43.031 | 76.8% | 2.939 | 76.8% | 5.856 |
| 2048 | 81.1% | 71.441 | 81.1% | 4.861 | 81.1% | 11.436 |
| 4096 | 85.4% | 132.550 | 85.4% | 7.890 | 85.4% | 22.567 |
| 8192 | 89.6% | 193.196 | 89.6% | 11.917 | 89.6% | 43.429 |
| 16384 | 93.9% | 298.233 | 93.9% | 18.106 | 93.9% | 87.475 |
| 32768 | 98.2% | 430.966 | 98.2% | 24.135 | 98.2% | 171.793 |
