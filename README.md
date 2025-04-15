# ESP32Instances

NodeJS tool to find ESP32 instances on the network listening to UDP. Supports [WLED](https://github.com/wled/WLED), [WLED-MM](https://github.com/MoonModules/WLED-MM), [MoonBase](https://github.com/ewowi/MoonBase) and [MoonLight](https://github.com/MoonModules/MoonLight)

<img width="908" alt="Screenshot 2025-04-15 at 22 34 17" src="https://github.com/user-attachments/assets/a8cdf33e-2e83-4662-a0e3-778dded1fcd7" />

ESP32Instances is a [MoonModules](http://MoonModules.org) product, ⚖️GPL-v3

# Install

Up and running in seconds:

* Clone this repo to folder xyz (choose your place)
* ```cd xyz```
* install nodeJS if not installed already
* ```npm init -y``` to create package.json
* ```npm install ws``` to enable websockets
* ```node ESP32Instances.js``` to start a webserver listening to udp 65506 and hosting html on 8192. 65506 is used by WLED and Moon. 8192 can be changed if you prefer another port.
* ```index.html``` to start the webpage showing the instances. Click on the IP number to go to the Instance itself
