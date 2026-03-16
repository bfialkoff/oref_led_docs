# Pikud HaOref LED Alert Monitor

A small, silent device that shows the current Pikud HaOref (Israel Home Front Command) alert status for your city using a single color LED. Designed to be placed in your safe room.

**Red** means stay inside. **Green** means all clear.

> **Important:** This is not a life-saving device. Alert data may be delayed
> by up to two minutes compared to the official siren. Always follow
> official Pikud HaOref instructions. This device is intended as a
> supplementary, passive indicator -- not a replacement for sirens or
> official alert apps.

## Why

- **Completely silent** -- no sounds, no phone buzzing. Just a light.
- **Shabbat friendly** -- runs continuously without any interaction.
- **Safe room indicator** -- place it in your mamad. Red means the alert is still active. Green means the official all-clear has been given.
- **Stress free** -- no need to check your phone or the news. Glance at the light.

## LED Status

| LED | Meaning |
|-----|---------|
| **Red (blinking)** | Alert active in your city -- stay in the safe room |
| **Green (slow pulse)** | All clear -- you may leave the safe room |
| **Yellow (solid)** | Cannot reach alert service -- check your internet |
| **Yellow (blinking)** | Setup mode -- connect your phone to configure |

## Quick Start

1. Plug the device into a standard USB-C phone charger (5V)
2. On your phone, connect to the **"PikudAlert-Setup"** WiFi network
3. Select your home WiFi, enter the password, choose your city
4. Place the device in your safe room -- done

See the full [Setup Guide](SETUP.md) for detailed instructions.

## How It Works

The device connects to your home WiFi and checks for alerts every 30 seconds. When an alert is issued for your city, the LED turns red. When the all-clear is given, it turns green. The data comes from the official Pikud HaOref feed via a secure cloud service.

Firmware updates are automatic -- the device checks for new versions periodically and updates itself. No action needed.

## Important Disclaimer

This device relies on an internet connection and a third-party cloud service
to relay Pikud HaOref data. Alert information may be delayed by up to two
minutes. The device may fail due to power outages, internet disruptions, or
service interruptions.

**Do not rely on this device as your sole source of alert information.**
Always have an additional alert method available (official Home Front
Command app, radio, siren).

## Documentation

- [Setup Guide](SETUP.md) -- First-time setup, LED meanings, how to change WiFi or city
- [Troubleshooting](KNOWN_ISSUES.md) -- Common issues and solutions

## License

MIT
