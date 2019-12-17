# RobotiqHand for control from external ubuntu pc
## environments
```
ur3e
external ubuntu 18.04 pc
python 2.7
```
## prepare on ur3e
```
append 'rs485' Settings/System/URCaps
remove 'Robotiq_Grippers' Settings/System/URCaps
setup Settings/System/Network
```
## prepare on ubuntu pc
```
$ git clone https://github.com/TechMagicKK/RobotiqHand.git
on test_robotiq.py, change HOST ip address to ur3e
```

## test
```
$ python test_robotiq.py
```

