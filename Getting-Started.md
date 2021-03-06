## How this all works

To bring motion to your Sim-Rig we need to configure the game first.
Most games do need some config file parameter changes, others do have build in config menus for enabling the telemetry output.

Once enabled, the telemetry data will be available by shared memory (same as a file but only stored in memory) or via network (most do use UDP).

See “Supported Games” -> “Game Setup Instructions”

Next comes the PC Software, SimFeedback. This software will request or receive the telemetry data several times per second. We call this the Sample Rate, a good sample rate is 100 Samples per second.

This data contains information about the position of the car.
By using this data Sample by Sample over time we can calculate the direction and the amount of movement of the car.
The software translates the calculated data into so called “Motion Cues”.

“Motion Cues” are movements of your Rig that simulate how the car is moving in the game.
Some of the data will be used to give you a one by one impression like Pitch or Roll. Other data like acceleration will use the “Jerk”. Jerk is the rate of change. Main reason for that is, that we could not simulate acceleration over a longer period of time, due to the limited range.

This “Motion Cues” will be send as position commands to the “Motion Controller”.

The “Motion controller” is a micro controller (Arduino Leonardo) that will take care of starting, stopping, position tracking and synchronization of all motors to control the “Servo Drivers”.

Finally, the “Servo Driver” will drive the motor.

## First things first

You need to get all the items listed on our [Shopping List](./Shopping-List)

Next get the [STL files](./STL-Files) from the repo

Check the [3D-Printing Instruction](./3D-Printing)

Start printing! 3D-Printing all necessary parts will take ~2 weeks using one printer!

Start to build the [electronics](./Electronics)

[Test the motors](./Motor-Test) by connecting them to the Servo Driver.

Install [SimFeedback](./SimFeedback)

Learn how to activate a Profile for your game and to start the Motion output.

Test the motor with the Servo driver attached to the Motion Controller (do not attach the motor to the actuator!).

Assemble the [Actuator](./Actuator)

Assemble the Actuators to your rig.

Go racing and have fun!
