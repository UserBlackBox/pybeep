# pybeep
python3 alternative to beep using ALSA

Created in Python 3.6 using [pysine](https://pypi.org/project/pysine/). Is designed to be an alternative to [beep](https://github.com/johnath/beep) for use on computers without a pcspkr like laptops. Has the same arguments as beep.

## Install
Either copy the binary in `dist\` or the python program to your path in `/bin` or `~/.local/bin`. Can be run without dependencies if used in binary form.

## Dependencies
**Dependencies for general use:**
* ALSA

**Dependencies for python3 program:**
* python3
* pysine
* portaudio19-dev

**Dependencies for compiling:**
* gcc
* cython

## Compiling
```
cython beep.py --embed #convert python to c
gcc -Os -I /usr/include/python3.6m -o beep beep.c -lpython3.6m -lpthread -lm -lutil -ldl #compile c code
```
Modify the gcc command with your python version which can be found with `python3 -V`

## Usage
```
beep [-f N] [-l N] [-d N]
beep [ OPTIONS ] [-n] [ OPTIONS ]
beep [-h] [--help]

Parameters:
-h, --help   show this help page
-f N         specify tone frequency where 0<N<20000
-l N         specify tone duration in milliseconds
-d N         specify gap duration between tones in milliseconds
-n           split between multiple tones in one command run
--verbose    show ALSA messages
```

## TODO
* Support for more beep arguments

* Argument aliases

## Resources 
Original beep program: [https://github.com/johnath/beep](https://github.com/johnath/beep)

Original beep man page: [https://linux.die.net/man/1/beep](https://linux.die.net/man/1/beep)

Compatible beep music bash scripts: [https://github.com/ShaneMcC/beeps](https://github.com/ShaneMcC/beeps)
