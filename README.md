# Pumpkin Pi

A small Linux single-board computer based on the Allwinner V3s.

## Hardware Specifications

| Component | Specification |
|---|---|
| SoC | Allwinner V3s (eLQFP-128) |
| CPU | Single-core ARM Cortex-A7, up to 1.2 GHz (typically 1.008 GHz) |
| RAM | 64 MiB DDR2, 400 MHz, integrated into the SoC |
| PMIC | X-Powers AXP202 |
| Power rails | 1.2V (CPU/System), 3.3V (I/O), 3.0V (Analog) |
| DDR2 power supply | 1.8V via dedicated SY8088AAC regulator |
| Flash storage | 16 MiB Winbond W25Q128JVFIQ SPI NOR (SPI0) |
| Main oscillator | 24 MHz crystal, ±10 ppm, 12 pF |
| RTC oscillator | 32.768 kHz crystal, ±20 ppm, 12.5 pF |
| Power input | USB Type-C (16-pin connector, power only) |
| Serial interfaces | UART0, UART2 |
| GPIO | 6 exposed GPIO pins (PE19–PE24) |
| Programming | Dedicated SPI NOR programming header |
| Status LED | White LED with Linux heartbeat support |
| Fan connector | 2-pin JST-PH, 3.3V |
| PCB | 4 layers, 49.9 × 45 mm |

## Software

Firmware and Linux support are yet to be implemented.

## Project Files

The repository contains the KiCad schematic, PCB layout, custom symbols, footprints, and 3D models.

If KiCad reports a missing `PumpkinPi` footprint library, reconnect `PumpkinPi.pretty` through **Preferences → Manage Footprint Libraries**.

## License

The Pumpkin Pi hardware design is licensed under
[CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/).

See Third-Party Credits for attribution of reused and adapted designs.

## Third-Party Credits

This project is partially based on and inspired by the [FunKey S Hardware](https://github.com/FunKey-Project/FunKey-S-Hardware) project.

The following elements were reused or adapted from its hardware design:

- KiCad schematic symbols for the Allwinner V3s and AXP20x PMIC.
- Crystal oscillator circuits (24 MHz and 32.768 kHz).
- SVREF reference voltage circuitry.
- DDR2 power supply design using the SY8088 regulator.
- General power management and schematic design concepts.

The original FunKey S hardware design is licensed under [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/). Components and circuits reused in Pumpkin Pi have been adapted for this board.

Credit goes to the FunKey Project contributors for making their hardware design publicly available.
