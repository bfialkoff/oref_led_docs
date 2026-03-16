# Setup Guide

## What You Need

- The alert monitor device
- A standard USB-C phone charger (5V) or any USB power source
- Your phone (for the one-time WiFi setup)

## First-Time Setup

### Step 1: Plug In

Plug the device into a USB-C charger. The LED will start **blinking yellow** -- this means it's ready to be configured.

### Step 2: Connect Your Phone

1. Open WiFi settings on your phone
2. Connect to the network called **"PikudAlert-Setup"**
3. A setup page will open automatically
   - If it doesn't appear, open your browser and go to `http://192.168.4.1`

### Step 3: Configure

1. **Select your WiFi network** from the list and enter the password
2. **Choose your city** -- tap the search box and start typing in Hebrew. A list of matching cities will appear. Tap your city to select it. The city field marked with **\*** is required.
3. Tap **Save**

### Step 4: Place It

The device will restart and connect to your WiFi. The LED will turn **solid green** -- all clear, monitoring is active.

Place the device in your safe room where you can see the LED. That's it.

## LED Guide

| LED | What It Means |
|---|---|
| Yellow blinking | Setup mode / no WiFi -- connect your phone to "PikudAlert-Setup" |
| Green solid | All clear -- no active alerts in your city |
| **Red fast blink** | **Alert active -- stay in the safe room** |
| Yellow solid | Connection issue -- check your internet. Will recover on its own. |

**Note:** Alert data may be delayed by up to two minutes compared to the official siren. When the LED turns green, the official all-clear has been given.

## Changing WiFi or City

If you move, change your WiFi, or want to monitor a different city:

1. **Press and hold the small button near the USB port** for 3 seconds
   - The LED will go solid while you hold it
   - After 3 seconds, the device resets
2. The LED starts **blinking yellow** -- back in setup mode
3. Follow Steps 2-3 above

**Tip:** The other button (further from the USB port) simply restarts the device without erasing your settings.

## Updates

Updates happen automatically. The device periodically checks for new firmware and installs it on its own. You don't need to do anything.

## Troubleshooting

| Problem | Solution |
|---|---|
| LED doesn't turn on | Try a different USB-C cable or charger. |
| Yellow blink won't stop | Can't connect to WiFi. Check your password. Try moving closer to the router. Hold the button near USB for 3s to reset and try again. |
| Yellow solid | Connected to WiFi but can't reach the alert service. Check your internet. Will recover on its own. |
| Setup page won't load | Make sure your phone is connected to "PikudAlert-Setup" (not your home WiFi). Try `http://192.168.4.1` in your browser. |
| Red blink but no alert in my area | The device monitors the city you chose. Hold the button near USB for 3s to change it. |
