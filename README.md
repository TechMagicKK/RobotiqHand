# RobotiqHand control python2.7 module from external ubuntu pc
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

