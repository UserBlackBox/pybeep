# pybeep
python3 alternative to beep using ALSA

Created in Python 3.6 using pysine. Is designed to be an alternative to [beep](https://github.com/johnath/beep) for use on computers without a pcspkr like laptops. Has the same arguments as beep.

## Install
Copy the binary to your path in `/bin` or `~/.local/bin`

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
• Support for more beep arguments

• Argument aliases

## Resources 
Original beep program: [https://github.com/johnath/beep](https://github.com/johnath/beep)

Original beep man page: [https://linux.die.net/man/1/beep](https://linux.die.net/man/1/beep)

Compatible beep music bash scripts: [https://github.com/ShaneMcC/beeps](https://github.com/ShaneMcC/beeps)
