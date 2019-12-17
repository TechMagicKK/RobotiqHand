# RobotiqHand python module from external ubuntu pc
## environments
```
ur3e
external ubuntu 18.04 pc
python 2.7
```
## prepare on ur3e
```
Settings/System/URCaps
	append 'rs485'
	remove 'Robotiq_Grippers'
Settings/System/Network
	setup ur3e's network info.
```
## prepare on ubuntu pc
```
$ git clone https://github.com/TechMagicKK/RobotiqHand.git
on test_robotiq.py, change HOST ip address to ur3e
```
## test
```
$ python test_robotiq.py
to exit program, press ctrl-c.
```
## technical information
It is necessary rs485 URcap. That is daemon for communicate between ur3e's rs485 network and external pc via tcp/ip.
RobotiqHand module use this mechanism.
So you must activate rs485 URCap on ur3e.
And,
If you activate Robotiq_Gripper URCap on ur3e, That URCap always use inner rs485 network without exclusive.
This means external rs485 communication make conflict communication contents.
So if you wanna control 2f-85 via rs485 from external pc, you must deactivate Robotiq_Gripper URCap on ur3e.
If you use ROS, you don't need URScript, right? :)
