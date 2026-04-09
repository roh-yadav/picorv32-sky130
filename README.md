# PicoRV32 Physical Design on SKY130

Full RTL-to-GDS physical design of PicoRV32 RISC-V processor using OpenLane on SKY130 130nm PDK.

## Results

| Metric | Value |
|--------|-------|
| Process | SKY130 130nm |
| Die Area | 1000 x 1000 um |
| Core Utilization | 40% |
| Clock Period | 20ns (50MHz) |
| Setup Violations | 0 |
| Hold Violations | 0 |
| DRC Violations | 0 |
| Fanout Violations | 13 (reduced from 178) |

## Tools Used

- OpenLane v1.0.2
- SKY130A PDK
- KLayout 0.28
- OpenSTA
- OpenROAD

## Key Learnings

- Fixed floorplan density errors by tuning FP_CORE_UTIL
- Reduced fanout violations 93% using stronger CTS clock buffers
- Critical path slack: 10.34ns MET at typical corner
