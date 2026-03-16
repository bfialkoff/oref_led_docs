# Pikud HaOref LED Alert Monitor

A compact device that monitors Pikud HaOref (Israel Home Front Command) alerts in real-time and displays the current status using a color-changing LED.

## What It Does

The device connects to your home WiFi and continuously checks for alerts in your city. The LED shows you the current status at a glance:

| LED | Meaning |
|-----|---------|
| **Red (blinking)** | Alert active -- seek shelter immediately |
| **Green (slow pulse)** | All clear -- no active alerts |
| **Yellow (solid)** | Cannot reach alert service -- check your internet |
| **Yellow (blinking)** | Setup mode -- connect your phone to configure |
| **Blue (solid, 3 seconds)** | WiFi connected successfully |

## What's In The Box

- Alert monitor device (ESP32-C3 microcontroller)
- WS2812B RGB LED breakout
- USB-C cable for power

## Quick Start

1. Plug in the device
2. Connect your phone to the **"PikudAlert-Setup"** WiFi network
3. Select your WiFi network, enter password, choose your city
4. Done -- the LED shows your alert status

See the full [Setup Guide](SETUP.md) for detailed instructions.

## How It Works

The device checks for alerts every 30 seconds. It connects to a secure cloud service that relays official Pikud HaOref data. Firmware updates are installed automatically -- the device checks for new versions every 6 hours and updates itself.

## Documentation

- [Setup Guide](SETUP.md) -- First-time setup, LED meanings, WiFi reset
- [Troubleshooting](KNOWN_ISSUES.md) -- Common issues and solutions

## License

MIT
