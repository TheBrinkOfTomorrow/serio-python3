# serio-python3

Forked from github.com/devttys0/serio

Includes python3 update by mattmart3 (https://github.com/mattmart3)

# Original description

Allows uploading of binary files from a host PC to an embedded Linux system via the embedded system's serial port or telnet connection without any special binaries on the embedded system.

The only requirements on the embedded system is that it provides an interactive shell on the serial port, and that the shell's echo command supports the -n and -e options.


# How-to:

Install necessary python3 packages (assuming Debian based distribution):
```
sudo apt install python3 python3-pip python3-venv
```
Create a Python3 virtual environment and activate it:
```
python3 -m venv ~/.venv
source ~/.venv/bin/activate
```
Install pyserial module:  (note: not 'serial' module - this doesn't work)
```
pip3 install pyserial
```

Transfer file to target:  (assuming target device is on /dev/ttyUSB0)
```
python3 serio.py -e </path/to/source/filename> -d </path/to/target/filename> /dev/ttyUSB0
```
