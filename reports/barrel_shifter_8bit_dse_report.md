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
| **Serial Fault Simulation (SFS)** | 33.661 | 1.00x | 90.83% | 21 | 36 (98.2% red.) |
| **Parallel Pattern Fault Simulation (PPFS)** | 2.307 | 14.59x | 90.83% | 21 | 32 (98.4% red.) |
| **Concurrent Fault Simulation (CFS)** | 8.856 | 3.80x | 96.94% | 7 | 36 (98.2% red.) |

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
| 2 | 24.5% | 0.285 | 24.5% | 0.294 | 29.7% | 0.047 |
| 4 | 27.1% | 0.408 | 27.1% | 0.281 | 33.6% | 0.056 |
| 8 | 28.8% | 0.708 | 28.8% | 0.320 | 37.6% | 0.104 |
| 16 | 38.0% | 1.033 | 38.0% | 0.311 | 44.1% | 0.123 |
| 32 | 43.7% | 1.615 | 43.7% | 0.294 | 49.8% | 0.194 |
| 64 | 50.7% | 2.659 | 50.7% | 0.303 | 56.8% | 0.335 |
| 128 | 57.6% | 4.727 | 57.6% | 0.511 | 63.8% | 0.710 |
| 256 | 65.9% | 7.875 | 65.9% | 0.675 | 72.1% | 1.168 |
| 512 | 74.2% | 13.282 | 74.2% | 1.011 | 80.3% | 2.267 |
| 1024 | 82.5% | 21.322 | 82.5% | 1.503 | 88.6% | 4.581 |
| 2048 | 90.8% | 33.042 | 90.8% | 2.153 | 96.9% | 9.232 |
