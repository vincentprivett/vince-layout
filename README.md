# Vince's Corne Keyboard Layout

This is heavily influenced by [markstos Corne layout](https://github.com/markstos/qmk_firmware/tree/markstos/keyboards/crkbd/keymaps/markstos), with adjustments to suit a UK keyboard layout.

A primarily 3x5 layout for split ergonomic keyboards with an extra column on each hand for rare and optional keys.

For a detailed description and keymap design choices see [markstos Corne layout article](https://mark.stosberg.com/markstos-corne-3x5-1-keyboard-layout).

## Layout

![Vince 3x5+1 Corne layout](vince-corne.svg)

## Hardware

- Corne (crkbd) split keyboard
- Elite-C controllers

## Prerequisites

1. Install QMK following the official guide: https://docs.qmk.fm/newbs_getting_started
2. Run `qmk setup` to clone the QMK firmware repository

## Installation

Copy the keymap folder from this repo into your QMK firmware tree:

```bash
cp -r qmk/keyboards/crkbd/keymaps/vince-corne ~/qmk_firmware/keyboards/crkbd/keymaps/
```

## Compile

```bash
qmk compile -kb crkbd/rev1 -km vince-corne
```

## Flash

1. Connect one half of the keyboard via USB.
2. Put the controller into bootloader mode by double-tapping the reset button on the Elite-C.
3. Flash the firmware:

```bash
qmk flash -kb crkbd/rev1 -km vince-corne
```

4. Repeat for the second half — connect it via USB and flash again with the same command.

> **Note:** Both halves run the same firmware. The keyboard detects which side is connected to USB and assigns it as the master.

## Disclaimer

This is my personal layout and is subject to evolve further with my tastes.