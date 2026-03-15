# Pikud HaOref LED Alert Monitor

A Raspberry Pi project that monitors Pikud HaOref (Israel Home Front Command) alerts and displays the current status using LEDs.

| LED | Meaning |
|-----|---------|
| **RED** | Active alert — rockets, missiles, or hostile aircraft detected |
| **GREEN** | All clear — no active alerts |
| **YELLOW** | Error — cannot reach the alert API (network issue, API down, etc.) |

## Quick Start

1. Download the latest release from the [Releases](https://github.com/bfialkoff/oref_led_docs/releases) page
2. Follow the [Setup Guide](SETUP.md)

## How It Works

The monitor polls a Cloudflare Worker API that proxies Pikud HaOref alert data. The Worker handles caching and rate limiting so the Pi doesn't hit OREF directly.

```
Pi (polls every 5s) → Cloudflare Worker (caches 60s) → OREF
```

Three LEDs connected to GPIO pins indicate the current state. The monitor runs as a systemd service that starts on boot.

## Documentation

- [Setup Guide](SETUP.md) — Hardware, wiring, software installation
- [Known Issues & Troubleshooting](KNOWN_ISSUES.md)

## License

MIT
