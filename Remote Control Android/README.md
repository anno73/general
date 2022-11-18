# Remote Control Android with Python

## BlueStacks

Settings->Advanced->Android Debug Bridge->Connect to Android at IP:Port

IP and port change with every restart. Find the current settings programatically in `C:/ProgramData/BlueStacks_nxt/bluestacks.conf`. Search for `bst.instance.{someInstance}.display_name="BlueStacks Window name"`.

`bst.instance.{someInstance}.status.adb_port="51013"` gives the current port in use. IP seems to be always 127.0.0.1.

## adb

```
adb start-server
adb connect 127.0.0.1 BlueStacksPort
```


## VNC

### Android

Install droidVNC-NG from playstore

Package name: net.christianbeier.droidvnc_ng

```
adb shell cmd package list packages -3
adb uninstall net.christianbeier.droidvnc_ng
```

Python: vncdotool - https://vncdotool.readthedocs.io/en/latest/library.html

Gets me one image per second.


## pyautogui

## OpenCV

