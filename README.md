# Razerkb

Razerkb is a Python tool for setting up RGB lighting for Razer keyboards* in Linux.

## Installation

Clone or download the repository.

```bash
git clone git@github.com:dogue/razerkb.git
```

## Usage

```bash
usage: razerkb [-h] [-l FILE | -s RGB]

Configure RGB lighting for Razer keyboards

optional arguments:
  -h, --help            show this help message and exit
  -l FILE, --load FILE  Load a color map from JSON file
  -s RGB, --set RGB     Set a global static color (hexadecimal)
```

`--set` expects a 6 digit hexadecimal representation of an RGB value without the leading hash (#). Example: `razerkb -s 00ff00` would set the entire board to static green.

`--load` expects a JSON file containing a keymap with color specifications. This file can be built using razerkb-buildmap. I must warn you that the process is slow and tedious. To ensure all keys are properly mapped, the script lights each up one at a time and requests that the user define the key and a color for it.

Colors can be defined in the `color-definitions.json` file. Each entry is an array where the elements represent red, green, and blue values from 0-255.

The included `color-map.json` is my personal setup. Use it, change it, delete it. Do as you'd like. I included it as an example.

## Requirements
Razerkb depends on [OpenRazer](https://openrazer.github.io/).

## *Ya Buts & Caveats
The Razer Black Widow Elite is the keyboard I have and the only Razer device I have any experience with. This tool makes a *lot* of assumptions, based on my hardware. It may require minor tweaks in order to work for you.

Good luck. OpenRazer is *not* well-documented.

## License
[Unlicense](https://choosealicense.com/licenses/unlicense/)