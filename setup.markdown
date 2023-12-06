# Setup

## Open Bot Project information

1. The [webpage](https://www.openbotbrain.org/) for the project.
2. The [firmware repository](https://github.com/OpenBotBrain/controller-firmware).
3. CI builds, stored as the result in the actions. For example, [this
   one](https://github.com/OpenBotBrain/controller-firmware/actions/runs/6678041626).
4. The [discord server](https://discord.gg/39TEWpQReU). That is somewhat active, but could use more friends.

## Hardware

The links are only useful as examples. You can find all these things
in the local versions of the sites.


### Battery

The board without a battery mostly works but it does not have enough
power to drive motors or the (very optional) Raspberry Pi Zero.

Any Lipo battery would work but I got this
[one](https://www.ebay.co.uk/itm/354254105023?var=623640855098). It is
a tad too big and a small one would also work. The sensor/motor
connectors were supposed to be on top of the board, but since they
have the left leaning latch, apparently their connectors are also
mirrored and we got them after getting the board made, so we had to
put them below. So there is not as much space for the batter as we
wanted.

### ST-Link programmer

To program the MCU we need a programmer. The one by the manufacturer
is this
[one](https://www.st.com/en/development-tools/st-link-v2.html). But it
is bulky and expensive. I have never seen one, everyone seems to use
the cheap ones you can get on ebay or amazon. Like this
[one](https://www.amazon.co.uk/Programmer-Emulator-Downloader-Debugger-Programming/dp/B0B5WYQ4FT/ref=sr_1_4?crid=1CA9NIRK6MS2H&keywords=st-link+v2&qid=1701856564&sprefix=st-l%2Caps%2C122&sr=8-4).

### TTL to USB interface (optional)

A final piece of hardware that would be maybe convenient is a USB
interface to the TTL serial ports in the board. I do not think we need
this to begin with, but it may come in handy later depending on what
we do. I got this
[one](https://www.amazon.co.uk/Serial-Converter-Featuring-Original-FT232RL/dp/B075N82CDL/ref=sr_1_3_pp?crid=2IG3NAR5H5G94&keywords=ftdi+usb+to+serial+ttl&qid=1701856593&sprefix=ftdi%2Caps%2C76&sr=8-3).
They are not expensive, and would get one that has a chance of having
a "genuine FTDI" one. Apparently they work best, and they are
supported by everything. For example, on a mac the FTDI one does not
require installing drivers, and installing a closed source flaky
drivers are not my idea of fun.

## Software

### Upload utility

The ST-link needs an utility to control it. The official expensive
comes with one, I have never used it. I use the free software one that
is available [here](https://github.com/stlink-org/stlink).

### Toolchain

The gcc version for the board is: gcc-arm-none-eabi. For Debian based
distros, the compiler can be installed with '''sudo apt-get install
gcc-arm-none-eabi'''. There
[readme](https://github.com/OpenBotBrain/controller-firmware/blob/main/README.md)
for the firmware has some details for windows.
