# Design Space Exploration Report: barrel_shifter_8bit

## Circuit Information

| Parameter | Value |
| :--- | :--- |
| Circuit Name | `barrel_shifter_8bit` |
| Primary Inputs (PIs) | 11 |
| Primary Outputs (POs) | 8 |
| Logic Gates | 75 |
| Total Circuit Nodes | 179 |
| Original Total Faults | 342 |
| Collapsed Faults | 229 (33.0% reduction) |
| Test Vectors Evaluated | 2048 |

## Algorithm Performance Comparison

| Algorithm | Time (ms) | Speedup vs SFS | Fault Coverage (%) | Undetected Faults | Compacted Test Vectors |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **Serial Fault Simulation (SFS)** | 34.014 | 1.00x | 90.83% | 21 | 36 (98.2% red.) |
| **Parallel Pattern Fault Simulation (PPFS)** | 2.309 | 14.73x | 90.83% | 21 | 32 (98.4% red.) |
| **Concurrent Fault Simulation (CFS)** | 8.695 | 3.91x | 96.94% | 7 | 36 (98.2% red.) |

## Undetected Faults

The following 21 faults remained undetected:

- `m0_7_b SA0`
- `m1_7_b SA0`
- `m1_6_b SA0`
- `m2_7_b SA0`
- `m2_6_b SA0`
- `m2_5_b SA0`
- `m2_4_b SA0`
- `s2_br2 SA0`
- `s2_br2 SA1`
- `s2_br3 SA0`
- `s2_br3 SA1`
- `s2_br4 SA0`
- `s2_br4 SA1`
- `s2_br5 SA0`
- `s2_br5 SA1`
- `s1_br2 SA0`
- `s1_br2 SA1`
- `s1_br3 SA0`
- `s1_br3 SA1`
- `s0_br2 SA0`
- `s0_br2 SA1`

## Vector Budget Scaling (Design Space Exploration)

| Vectors | SFS Cov (%) | SFS Time (ms) | PPFS Cov (%) | PPFS Time (ms) | CFS Cov (%) | CFS Time (ms) |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| 2 | 24.5% | 0.275 | 24.5% | 0.282 | 29.7% | 0.051 |
| 4 | 27.1% | 0.394 | 27.1% | 0.281 | 33.6% | 0.060 |
| 8 | 28.8% | 0.627 | 28.8% | 0.283 | 37.6% | 0.080 |
| 16 | 38.0% | 0.994 | 38.0% | 0.315 | 44.1% | 0.127 |
| 32 | 43.7% | 1.620 | 43.7% | 0.290 | 49.8% | 0.196 |
| 64 | 50.7% | 2.693 | 50.7% | 0.318 | 56.8% | 0.353 |
| 128 | 57.6% | 4.654 | 57.6% | 0.464 | 63.8% | 0.643 |
| 256 | 65.9% | 7.796 | 65.9% | 0.683 | 72.1% | 1.185 |
| 512 | 74.2% | 13.129 | 74.2% | 1.052 | 80.3% | 2.304 |
| 1024 | 82.5% | 21.230 | 82.5% | 1.512 | 88.6% | 4.517 |
| 2048 | 90.8% | 32.792 | 90.8% | 2.168 | 96.9% | 8.859 |
