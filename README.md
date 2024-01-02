# React Native Light-Gun

This is a React Native app that uses the Expo framework and the expo-barcode-scanner and expo-sensors modules to emulate a console light-gun like the one of the Sega Dreamcast (the most modern iteration of the technology). The app uses the camera and a QR code for optical tracking in order to infer where the TV screen is and where within the display the gun is pointing in, it detects flick gestures to know when the gun (phone) is reloaded. This is because the Sega Dreamcast light gun has an accelerometer to tell when you rotate it up to reload. If you really like the app, search Aliexpress for 'AR Gun Controller' and you will find cheap (under 10 $/£) devices that you can hold your phone in for that added sense of arcade realism. While this method of positional tracking is susceptible to motion blur, you really don't need anything other than a phone and therefore it costs nothing. Any QR code will work, the bigger the better, you can use one from discarded advertising or packing material instead of printing. 

## Prerequisites

To run this app, you need to have the following installed on your system:

- Node.js and npm
- Expo CLI (`npm install -g expo-cli`)
- Expo Go app on your iPhone or Android device
- A QR code printed or displayed on another device
- A PC with an emulator that can receive the tracking data from the app

## Installation

- Clone this repository with `git clone [REPO_URL]`
- Switch to the project's root directory in terminal
- Install the dependencies by running `npm install`

## Usage

- Run `expo start` to start the Expo server
- Scan the QR code with the Expo Go app on your device
- Grant the app permission to access the camera and the device motion
- Point the camera at the tracking QR code and adjust the screen scale with the slider
- Flick your device up to reload the gun and play a sound effect
- To receive the tracking data on your PC, you can use the `netcat` command or the `PC.js` script provided in the project folder. For example:

Using netcat:
nc -l -p 3000

The specific implementation will depend on the emulator you're using.
