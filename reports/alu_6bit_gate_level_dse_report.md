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
| **Serial Fault Simulation (SFS)** | 450.360 | 1.00x | 98.17% | 6 | 88 (99.7% red.) |
| **Parallel Pattern Fault Simulation (PPFS)** | 23.953 | 18.80x | 98.17% | 6 | 74 (99.8% red.) |
| **Concurrent Fault Simulation (CFS)** | 170.193 | 2.65x | 98.17% | 6 | 88 (99.7% red.) |

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
| 2 | 18.6% | 0.542 | 18.6% | 0.527 | 18.6% | 0.056 |
| 4 | 27.7% | 0.885 | 27.7% | 0.543 | 27.7% | 0.081 |
| 8 | 32.3% | 1.363 | 32.3% | 0.527 | 32.3% | 0.117 |
| 16 | 39.3% | 2.277 | 39.3% | 0.589 | 39.3% | 0.201 |
| 32 | 46.3% | 3.743 | 46.3% | 0.545 | 46.3% | 0.308 |
| 64 | 53.4% | 6.299 | 53.4% | 0.561 | 53.4% | 0.507 |
| 128 | 60.4% | 10.460 | 60.4% | 0.838 | 60.4% | 0.928 |
| 256 | 67.4% | 17.104 | 67.4% | 1.239 | 67.4% | 1.674 |
| 512 | 72.6% | 26.659 | 72.6% | 1.903 | 72.6% | 3.110 |
| 1024 | 76.8% | 43.136 | 76.8% | 2.992 | 76.8% | 5.877 |
| 2048 | 81.1% | 71.548 | 81.1% | 4.762 | 81.1% | 11.389 |
| 4096 | 85.4% | 118.401 | 85.4% | 8.227 | 85.4% | 22.754 |
| 8192 | 89.6% | 192.808 | 89.6% | 11.993 | 89.6% | 43.559 |
| 16384 | 93.9% | 296.001 | 93.9% | 17.798 | 93.9% | 85.264 |
| 32768 | 98.2% | 424.491 | 98.2% | 23.810 | 98.2% | 169.573 |
