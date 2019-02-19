# ring-homekit

These are my config files for both homeassistant and homebridge to get the latest ring videos from the API to show up in the Home app on iOS and macOS devices.

The process looks like this:

1. Use HomeAssistant ring component to get latest videos using Ring API
2. Use HomeAssistant automations to download that video on a schedule to a spot on a file system
3. Use homebridge and the camera-ffmpeg module to use show each file as a camera accesssory.

### Prerequisites

You'll need both [HomeAssistant](https://www.home-assistant.io) and [HomeBridge](https://github.com/nfarina/homebridge) up and running for this.

If you don't have them both running on the same OS like I do, you'll need to figure out where you can export the files in a way that homebridge and ffmpeg can see them.