# Setup Guide

## Prerequisites

### Hardware

- Raspberry Pi (tested on Pi 4/5, any model with GPIO should work)
- 3x LEDs (red, green, yellow)
- 3x 220Ω resistors
- Breadboard and jumper wires

### Software

- Raspberry Pi OS (Bookworm or later)
- Python 3.11+
- [uv](https://docs.astral.sh/uv/) package manager
- An API key for the Pikud Alert service (contact the maintainer)

## Wiring

| LED | GPIO Pin | Physical Pin |
|-----|----------|-------------|
| Yellow (error) | GPIO 17 | Pin 11 |
| Red (alert) | GPIO 27 | Pin 13 |
| Green (clear) | GPIO 22 | Pin 15 |

Each LED connects: `GPIO pin → 220Ω resistor → LED anode (+) → LED cathode (-) → GND`

Use any GND pin (e.g., Pin 6, 9, 14, 20, 25).

<!-- TODO: Add wiring diagram image -->

## Installation

### 1. Download the latest release

```bash
# Check https://github.com/bfialkoff/oref_led_docs/releases for the latest version
wget https://github.com/bfialkoff/oref_led_docs/releases/download/vX.Y.Z/pikud-leds-vX.Y.Z.tar.gz
tar xzf pikud-leds-vX.Y.Z.tar.gz
cd pikud-leds-vX.Y.Z
```

### 2. Install uv (if not already installed)

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
source ~/.bashrc
```

### 3. Install dependencies

```bash
uv sync
```

This creates a `.venv/` with all Python dependencies. System packages like `gpiozero` are picked up from the system Python.

### 4. Configure

```bash
cp .env.example .env
nano .env  # paste your API key
```

### 5. Test

```bash
# Test LED wiring (cycles through all three LEDs)
.venv/bin/python test.py

# Test with mock alerts (no API needed)
.venv/bin/python main.py --test

# Test with real API
.venv/bin/python main.py
```

### 6. Install as boot service

```bash
bash setup.sh
```

This creates a systemd service that starts the monitor on boot. To check status:

```bash
sudo systemctl status pikud-leds
sudo journalctl -u pikud-leds -f  # live logs
```

### 7. Uninstall service

```bash
bash setup.sh --cleanup
```

## Command-Line Options

```bash
# Monitor all cities (default)
.venv/bin/python main.py

# Monitor specific cities
.venv/bin/python main.py --cities "נתניה - מזרח" "תל אביב - מרכז העיר"

# Use mock alerts for testing
.venv/bin/python main.py --test
```

## Updating

1. Download the new release
2. Extract to the same directory (overwrites source files)
3. Your `.env` will not be overwritten (it's not included in the release)
4. Run `uv sync` to update dependencies
5. Restart the service: `sudo systemctl restart pikud-leds`
