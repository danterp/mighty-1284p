# Mighty 1284P: An Arduino core for the ATmega1284P #
  

## What is it? ##

Everything you need to run [Arduino](http://arduino.cc/) on an [ATmega1284P](http://www.atmel.com/devices/ATMEGA1284P.aspx) microcontroller.

This is a refreshed version of [maniacbug's mighty-1284p core](https://github.com/maniacbug/mighty-1284p) which was based on Arduino 1.0. With the invaluable help of many kind folks on the Arduino forum, I was able to produce this updated core based on Arduino 1.0.5. (If you're interested, and a bit masochistic, [here](http://forum.arduino.cc/index.php?topic=235521.0) is the rather lengthy discussion that took place during the process of updating the core.)

## Revision history ##

**13May2014 Jack Christensen**
- Added a 1M baud version of Optiboot.
- Added the "Mighty Mini 1284P" board to the boards.txt file.

**05May2014 Jack Christensen**
- Updates to pins_arduino.h files for correct pin mapping.
- Renamed the core directory from "standard" to "mighty" and updated board.txt accordingly.
- Changed wiring_analog.c to support correct analog pin mapping. This single-line change is the only change needed to the Arduino 1.0.5 "cores" files. [An equivalent change](http://github.com/arduino/Arduino/pull/1368) has been made in the Arduino repository and should be included in later releases.

**03May2014 Jack Christensen**
- An attempt to bring the mighty-1284p core up to Arduino 1.0.5 level. In researching the changes I came to the conclusion that the core was originally based on Arduino 1.0 and that since then all the changes in maniacbug's core files necessary to support the ATmega1284P had been worked into subsequent Arduino releases. This may have occurred as early as Arduino 1.0.1. Nevertheless, this update is working with Arduino 1.0.5 and while it may work with earlier releases, I do not plan to test them, so there is no guarantee.
- The initial commit is therefore just a matter of removing the cores directory and updating the boards.txt file to point at the cores directory in the Arduino distribution.

**23Jun2012 maniacbug**
- Everything is here and has been initially tested.  It should work fine.  There is more detailed testing which must be completed before calling it completely 'done' though.
- The platform now includes optiboot.  This bootloader is better in every way than the previous version, so it is recommended in all cases.  The prior one is included for reference.

## Installation

1. Go to http://github.com/JChristensen/mighty-1284p, click the **Download ZIP** button and save the ZIP file to a convenient location on your computer.
2. Go to your Arduino sketchbook folder. If it does not contain a folder named **hardware**, create one.
3. Unzip the downloaded file into the **hardware** folder.
4. The download from GitHub will have a dash and branch name appended, so the folder will be named, e.g. mighty-1284p-master or mighty-1284p-v1.0.5. Rename the folder to just **mighty-1284p**.
3. Restart the Arduino IDE.
4. Select the desired board from the Tools > Board menu and enjoy those extra pins and all that extra memory!

## Requirements

* Works with Arduino 1.0.5. It may work on other versions as early as 1.0.1 but these have not been tested.
* The [USBtinyISP](http://www.adafruit.com/products/46) is advertised as not able to program chips with more than 64K of flash, however there are varying reports of success using it with the ATmega1284P. Sometimes error messages are given but the upload process seems to have worked OK. Be forewarned. YMMV.

## See also

http://maniacbug.wordpress.com/2011/11/27/arduino-on-atmega1284p-4/

## Supported Boards

* **Mighty 1284p 16MHz using Optiboot** - The main board. Use this unless you have some clear reason to use another board. This uses a straightforward pinout that is especially helpful on a breadboard-built unit.
* **Bobuino** - [CrossRoads' board](http://crossroadsfencing.com/BobuinoRev17/index.html) built for maximum compatibility with Arduino Uno-class shields.
* **Mighty Mini 1284P** - A small breadboard-friendly version of the Mighty 1284p built with SMT components. Open-source design [available on GitHub](http://goo.gl/5fAHca).
* **avr-developers.com pinouts 16MHz using Optiboot** - Some people prefer the pinouts from avr-developers.com.  The classic pinouts.
* **Original Mighty 1284p 16MHz** - The very first bootloader I (maniacbug) ever got working.  Not recommended for use, but here as historical record.
* **Original Mighty 1284p 8MHz** - Ditto, but runs at 8MHz.