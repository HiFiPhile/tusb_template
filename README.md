# TinyUSB project template

An IAR template project to build TinyUSB examples.

## Supported board

- NUCLEO-C071RB
- NUCLEO-G0B1RE
- STM32L0538-DISCO
- STM32F4DISCOVERY
- STM32H573I-DK
- STM32F723E-DISCO
- NUCLEO-U5A5Zj-Q
- LPCXpresso55S69
- MIMXRT1170-EVKB

## Setup

### Prerequisites

1. Clone TinyUSB into tinyusb directory or use a symbolic link.
2. Checkout dependencies according to TinyUSB guide: https://docs.tinyusb.org/en/latest/reference/getting_started.html#dependencies

### build

1. In workspace, choose configuration according to the board, eg.`TUSB_STM32F723E-DISCO`.
2. In workspace, uncheck `Exclude from build` of the example in interest, eg.`cdc_dual_ports` Ensure it's checked for other projects.
3. In `Project Option -> C/C++ Compiler -> Preprocessor`, ensure example path is listed in include, eg.`$TUSB_DIR$\examples\device\cdc_dual_ports\src`, Also ensure other examples' path are NOT included,  eg. NO `$TUSB_DIR$\examples\device\uac2_headset\src`.

4. build project and profit.
