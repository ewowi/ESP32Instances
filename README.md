# ESP32Instances

NodeJS tool to find ESP32 instances on the network listening to UDP. Supports [WLED](https://github.com/wled/WLED), [WLED-MM](https://github.com/MoonModules/WLED-MM), [MoonBase](https://github.com/ewowi/MoonBase) and [MoonLight](https://github.com/MoonModules/MoonLight)

<img width="908" alt="Screenshot 2025-04-15 at 22 34 17" src="https://github.com/user-attachments/assets/a8cdf33e-2e83-4662-a0e3-778dded1fcd7" />

ESP32Instances is a [MoonModules](http://MoonModules.org) product, ⚖️GPL-v3

# InstallRun

* Clone this repo to folder xyz (choose your place)
* ```cd xyz```
* install nodeJS if not installed already
* ```npm init -y``` to create package.json
* ```npm install ws``` to enable websockets

# Run

* ```node ESP32Instances.js``` to start a webserver listening to udp 65506 and hosting html on 8192. 65506 is used by WLED and Moon. 8192 can be changed if you prefer another port.
* ```index.html``` to start the webpage showing the instances. Click on the IP number to go to the Instance itself

# Remarks

* Idea -> AI -> First commit
* This tool can easily be extended with a little knowledge of HTML / JS
    * More WLED UPD data can be extracted according to the [instance package definition](https://github.com/MoonModules/StarLight/blob/cc909d1663f3d775e0bc1ed0a4b5678889a34814/src/Sys/SysModInstances.h#L55-L66) and [sync package definition](https://github.com/MoonModules/StarLight/blob/cc909d1663f3d775e0bc1ed0a4b5678889a34814/src/Sys/SysModInstances.h#L76-L99) (UDP on port 21324)
    * More info can be extracted using the JSON get api of wled (e.g. <ip>/cfg etc). Commands can be send to WLED instances using JSON post
    * This is developed in parallel with [moonbase/instances](https://ewowi.github.io/MoonLight/moonbase/module/instances/) as this module will ask instances: what do you want me to control for you.

  <img width="696" alt="image" src="https://github.com/user-attachments/assets/50b4cb41-1deb-482a-89d1-3e787b9276b9" />


* Might also implement [Bluetooth support](https://github.com/MoonModules/MoonLight/issues/26)
