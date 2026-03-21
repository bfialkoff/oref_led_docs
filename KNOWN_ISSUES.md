# Known Issues & Troubleshooting

## Known Issues

None currently. Report issues at https://github.com/bfialkoff/oref_led_docs/issues.

## Troubleshooting

### LED doesn't turn on at all

- Try a different USB-C cable -- some cables are charge-only.
- Try a different charger or USB port.
- Make sure the charger provides 5V (any standard phone charger works).

### Blue blink won't stop (can't connect to WiFi)

- Make sure you entered the correct WiFi password during setup.
- Move the device closer to your WiFi router.
- The device only supports 2.4GHz WiFi networks (not 5GHz).
- Hold the button near the USB port for 3 seconds to reset and try again.

### Blue solid light (not blinking)

- The device is connected to WiFi but can't reach the alert service.
- Check your internet connection.
- This usually resolves on its own once the connection is restored.
- If it persists, press the button near the LED to restart the device.

### Setup page doesn't appear on phone

- Make sure your phone is connected to **"PikudAlert-Setup"** (not your home WiFi).
- Try opening your browser and going to `http://192.168.4.1`.
- If "PikudAlert-Setup" doesn't appear, the device may already be connected to WiFi. Hold the button near USB for 3 seconds to reset.

### Device keeps restarting

- This can happen if WiFi is unstable. The device will keep trying and eventually connect.
- Make sure the WiFi signal is strong enough where the device is placed.

## Reporting Issues

Report problems at https://github.com/bfialkoff/oref_led_docs/issues with:

1. What you see (LED color and pattern)
2. What you expected to see
3. How long the device has been in this state
