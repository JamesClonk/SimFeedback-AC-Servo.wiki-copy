SimFeedback supports the following games:

* Assetto Corsa Competizione
* Assetto Corsa
* iRacing
* Project Cars 1 and 2
* Dirt Rally
* RaceRoom
* RFactor 2
* more to come ...

Btw do you know, you can write your own [TelemetryProvider](./TelemetryProvider) for any game.

## Game Setup Instructions

### Assetto Corsa (Competizione)
Nothing to configure, will work out of the box.

Source Code is available [here](https://github.com/SimFeedback/SimFeedback-AC-Servo/tree/master/Src/ACTelemetryProvider).

### iRacing 

Edit app.ini in C:\Users\USERNAME\Documents\iRacing.


`irsdkEnableMem=1                        	; enable memory based telemetry`

`irsdkLog360Hz=1                         	; Log some telemetry at 360 Hz rather than at 60 Hz`

### Project Cars

Go to game Settings -> System

Select Shared Memory "Project CARS 2"

![Project Cars Setup 1](https://github.com/SimFeedback/SimFeedback-AC-Servo/blob/master/Docs/Project%20CARS%202-1.png)

![Project Cars Setup 1](https://github.com/SimFeedback/SimFeedback-AC-Servo/blob/master/Docs/Project%20CARS%202-2.png)


### Dirt Rally
Edit hardware_settings_config.xml  in C:\Users\USERNAME\Documents\my games\DiRT Rally\hardwaresettings.

`<udp enabled="true" extradata="3" ip="127.0.0.1" port="20777" delay="1" />`

### RFactor 2
Rfactor 2 needs a game plugin to be installed.

You can find it in `SimFeedback/ext/rf2/x86` for 32bit and `SimFeedback/ext/rf2/x64` for 64bit. 

Copy the `Steam\steamapps\common\rFactor 2\Bin32\Plugins` or RF2SimFeedbackPlugin.dll to `Steam\steamapps\common\rFactor 2\Bin64\Plugins`.

Plugin will be enabled by default.

Source code is available [here](https://github.com/SimFeedback/SimFeedback-AC-Servo/tree/master/Src/RF2).

