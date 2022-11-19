# Remote Control Android with Python

## BlueStacks

Settings->Advanced->Android Debug Bridge->Connect to Android at IP:Port

IP and port change with every restart. Find the current settings programatically in `C:/ProgramData/BlueStacks_nxt/bluestacks.conf`. Search for `bst.instance.{someInstance}.display_name="BlueStacks Window name"`.

`bst.instance.{someInstance}.status.adb_port="{BlueStacksPort}"` gives the current port in use. IP seems to be always 127.0.0.1.

### adb

```
adb start-server
adb connect 127.0.0.1 BlueStacksPort
```

## ADB

How to execute pinch-zoom gesture?

### Pure Python ADB

https://pypi.org/project/pure-python-adb/


## VNC

If used with BlueStacks, it might be necessary to switch to Settings->Graphics->Graphics engine mode->Compatibility

### Android

#### droidVNC-NG

https://github.com/bk138/droidVNC-NG

Install droidVNC-NG from playstore

Package name: net.christianbeier.droidvnc_ng

```
adb shell cmd package list packages -3
adb uninstall net.christianbeier.droidvnc_ng
```
### Python

#### vncdotool
Python: vncdotool - https://vncdotool.readthedocs.io/en/latest/library.html

Gets me one image per second.

#### asyncvnc

https://github.com/barneygale/asyncvnc

#### pyVNC

https://github.com/cair/pyVNC


## Windows Desktop - Python

How to perform a pinch-zoom gesture?

Fast screenshot capture.

Single instance and can only run in foreground (https://www.youtube.com/watch?v=J3fatZ2OVIU).

### OpenCV

Great [OpenCV Object Detection in Games](https://www.youtube.com/watch?v=KecMlLUuiE4&list=PL1m2M8LQlzfKtkKq2lK5xko4X-8EZzFPI) tutorial on Youtube from [Learn Code By Gaming](https://www.youtube.com/@LearnCodeByGaming)

Beware - search for images generated from the corresponding source. Take a screenshot on desktop to extract templates from there. Do not use screenshot from within emulator or adb.


### pyautogui



