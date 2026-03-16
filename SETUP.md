# Setup Guide

## What You Need

- The alert monitor device
- The RGB LED (small board with a single LED)
- A USB-C cable and any USB power source (phone charger, power bank, etc.)
- Your phone (for initial WiFi setup)

## Wiring

Connect the LED breakout to the device:

| LED Board | Device |
|---|---|
| 5V | V_USB |
| GND | GND |
| DI | IO8 |

## First-Time Setup

### Step 1: Power On

Plug the device in via USB-C. The LED will start **blinking yellow** -- this means it's ready to be configured.

### Step 2: Connect Your Phone

1. Open WiFi settings on your phone
2. Connect to the network called **"PikudAlert-Setup"**
3. A setup page will open automatically
   - If it doesn't appear, open your browser and go to `http://192.168.4.1`

### Step 3: Configure

1. **Select your WiFi network** from the list and enter the password
2. **Choose your city** -- tap the search box and start typing in Hebrew. A list of matching cities will appear. Tap your city to select it. The field marked with **\*** is required.
3. Tap **Save**

### Step 4: Done

The device will restart and connect to your WiFi. You'll see:

1. **Blue solid** (3 seconds) -- WiFi connected
2. **Green slow pulse** -- all clear, monitoring active

That's it. The device is now monitoring alerts for your city.

## LED Status Guide

| LED | What It Means | What To Do |
|---|---|---|
| Yellow blinking | Setup mode / no WiFi | Connect your phone to "PikudAlert-Setup" and configure |
| Blue solid | WiFi connected | Wait -- switches to green in a few seconds |
| Green slow pulse | All clear | Nothing -- no active alerts in your city |
| **Red fast blink** | **Alert active** | **Seek shelter immediately** |
| Yellow solid | Connection error | Check your internet. Will recover automatically. |

## Changing WiFi or City

If you move to a new location or change your WiFi network:

1. **Press and hold the small button near the USB port** for 3 seconds
   - The LED will go solid while you hold it
   - After 3 seconds, the device resets
2. The LED starts **blinking yellow** -- setup mode
3. Follow Steps 2-4 from First-Time Setup above

**Note:** The other button (near the LED) is the reset button -- it just restarts the device without erasing your settings.

## Firmware Updates

Updates happen automatically. The device checks for new firmware every 6 hours. If a new version is available, it downloads and installs it, then restarts. You don't need to do anything.

## Troubleshooting

| Problem | Solution |
|---|---|
| LED doesn't turn on | Check that the LED board is wired correctly (5V, GND, DI). Try a different USB-C cable. |
| Yellow blink won't stop | The device can't connect to WiFi. Make sure you entered the correct password. Try moving closer to your router. Hold the button near USB for 3s to reset and try again. |
| Yellow solid (not blinking) | The device is connected to WiFi but can't reach the alert service. Check your internet connection. It will recover on its own when the connection is restored. |
| Setup page won't load on phone | Make sure you're connected to "PikudAlert-Setup" (not your home WiFi). Try going to `http://192.168.4.1` manually in your browser. |
| Red blink but no alert in my area | The device monitors the city you selected during setup. If you need to change cities, hold the button near USB for 3s to reset. |
