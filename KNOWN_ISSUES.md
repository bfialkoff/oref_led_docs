# Known Issues & Troubleshooting

## Known Issues

<!-- No known issues at this time. -->

None currently. File issues at https://github.com/bfialkoff/oref_led_docs/issues.

## Troubleshooting

### Yellow LED stays on (error state)

The yellow LED means the monitor can't reach the alert API. Check:

1. **Network connectivity** — `ping google.com` from the Pi
2. **API health** — `curl https://pikud-alert.bfialkoff.workers.dev/health` — should return `{"ok": true, ...}`
3. **API key** — verify `.env` has the correct `ALERT_API_KEY`
4. **DNS resolution** — `nslookup pikud-alert.bfialkoff.workers.dev`

### LEDs don't light up

1. **Wiring** — run `python test.py` to cycle through all three LEDs
2. **GPIO permissions** — make sure your user is in the `gpio` group: `groups` should show `gpio`
3. **Pin numbers** — the code uses BCM numbering (GPIO 17, 27, 22), not physical pin numbers

### Service won't start

```bash
sudo systemctl status pikud-leds
sudo journalctl -u pikud-leds --no-pager -n 50
```

Common causes:
- Missing `.env` file
- `.venv/` not created (run `uv sync`)
- Python path wrong (check `setup.sh` uses the correct venv path)

### Service starts but LEDs don't respond

The service runs as a non-root user. Verify GPIO access:

```bash
# Check if lgpio/gpiozero works for your user
python3 -c "from gpiozero import LED; led = LED(17); led.on(); led.off(); print('OK')"
```

## Reporting Bugs

Open an issue at https://github.com/bfialkoff/oref_led_docs/issues with:

1. What happened vs what you expected
2. Output of `sudo journalctl -u pikud-leds --no-pager -n 50`
3. Output of `curl https://pikud-alert.bfialkoff.workers.dev/health`
4. Your Pi model and OS version (`cat /etc/os-release`)
