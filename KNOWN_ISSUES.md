# Known Issues & Troubleshooting

## Known Issues

None currently. Report issues at https://github.com/bfialkoff/oref_led_docs/issues.

## Troubleshooting

### LED doesn't turn on at all

- Make sure the USB-C cable is connected and providing power (you should see a small red power light on the device itself).
- Check that the LED board is wired correctly: 5V to V_USB, GND to GND, DI to IO8.
- Try a different USB-C cable -- some cables are charging-only and don't supply enough power.

### Yellow blink won't stop (can't connect to WiFi)

- Make sure you entered the correct WiFi password during setup.
- Move the device closer to your WiFi router.
- Hold the button near the USB port for 3 seconds to reset WiFi settings, then set up again.
- Make sure your WiFi is 2.4GHz -- the device does not support 5GHz networks.

### Yellow solid light (error state)

- The device is connected to WiFi but can't reach the alert service.
- Check your internet connection -- try loading a website on your phone.
- This usually resolves on its own once the internet connection is restored.
- If it persists, restart the device by pressing the button near the LED.

### Setup page doesn't appear on phone

- Make sure your phone is connected to **"PikudAlert-Setup"** (not your home WiFi).
- Try opening your browser and going to `http://192.168.4.1`.
- If the "PikudAlert-Setup" network doesn't appear, the device might have already connected to a saved WiFi network. Hold the button near USB for 3 seconds to reset.

### Device keeps restarting

- This can happen if WiFi is unstable. The device will keep trying to connect and eventually succeed.
- Make sure the WiFi signal is strong enough where the device is placed.

## Reporting Issues

Open an issue at https://github.com/bfialkoff/oref_led_docs/issues with:

1. What you see (LED color and pattern)
2. What you expected to see
3. How long the device has been in this state
