# TinyUSB project template

An IAR template project to build TinyUSB examples.

## Supported board

- NUCLEO-G0B1RE
- LPCXpresso55S69
- STM32F4DISCOVERY
- STM32L0538-DISCO
- STM32H573I-DK
- STM32F723E-DISCO
- NUCLEO-U5A5Zj-Q

## Setup

### Prerequisites

1. Clone TinyUSB and this template repositories.
2. Add `TUSB_DIR` configuration variable in IAR.
    1. Open `Tools -> Configure Custom Argument Variables`, switch to `Global` tab
    2. Click `New Group …`, name it to `TUSB`
    3. Click `Add Variable …`, name it to `TUSB_DIR`, change it’s value to the path of your TinyUSB stack, for example `C:\tinyusb`
3. Checkout dependencies according to TinyUSB guide: https://docs.tinyusb.org/en/latest/reference/getting_started.html#dependencies

### build

1. In workspace, choose configuration according to the board, eg.`TUSB_STM32F723E-DISCO`.
2. In workspace, uncheck `Exclude from build` of the example in interest, eg.`cdc_dual_ports` Ensure it's checked for other projects.
3. In `Project Option -> C/C++ Compiler -> Preprocessor`, ensure example path is listed in include, eg.`$TUSB_DIR$\examples\device\cdc_dual_ports\src`, Also ensure other examples' path are NOT included,  eg. NO `$TUSB_DIR$\examples\device\uac2_headset\src`.

4. build project and profit.
