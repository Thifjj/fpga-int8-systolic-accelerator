# INT8 Systolic Array Accelerator (FPGA)

This project implements an INT8 systolic array accelerator in VHDL,
packaged as an Avalon-MM slave IP and integrated into an FPGA SoC
using Intel Platform Designer.

## Architecture
- Processing Elements (PE): INT8 MAC, pipelined
- Accumulation: 32-bit signed
- Dataflow: systolic array (1D)
- Interface: Avalon-MM slave registers

## Integration
- Custom Avalon-MM IP
- Connected to Nios V (integration validated)
- Final synthesis limited by Quartus Lite license
- Planned Nios II port (same Avalon interface)

## Registers
| Offset | Description |
|------|------------|
| 0x00 | Control / Status |
| 0x04 | Weights |
| 0x08 | Input data |
| 0x0C | Result |

## Tools
- Quartus Prime 24.1
- Platform Designer
- VHDL-93
