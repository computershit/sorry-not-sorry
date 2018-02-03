## sorry not sorry, marina & pearl

Automatically skip Splatoon 2's intro. Forked from the amazing [snowball-thrower](https://github.com/bertrandom/snowball-thrower). Tested on a Teensy++ v2.0. Hastily hacked and tested after seeing posts on /r/NintendoSwitch and /r/Splatoon regarding the absurdity of not being able to skip the game's intro featuring Marina & Pearl. Perhaps this ridiculous method of providing a feature that should be included by default will highlight to Nintendo the need for a skip option.



#### How to use

Open Splatoon 2 and select the user. Plug your Teensy into a USB port on your Switch or dock, go grab a beer, and unplug the Teensy when you return.

This repository has been tested using a Teensy 2.0++.

#### Compiling and Flashing onto the Teensy 2.0++
Go to the Teensy website and download/install the [Teensy Loader application](https://www.pjrc.com/teensy/loader.html). For Linux, follow their instructions for installing the [GCC Compiler and Tools](https://www.pjrc.com/teensy/gcc.html). For Windows, you will need the [latest AVR toolchain](http://www.atmel.com/tools/atmelavrtoolchainforwindows.aspx) from the Atmel site. See [this issue](https://github.com/LightningStalker/Splatmeme-Printer/issues/10) and [this thread](http://gbatemp.net/threads/how-to-use-shinyquagsires-splatoon-2-post-printer.479497/) on GBAtemp for more information. (Note for Mac users - the AVR MacPack is now called AVR CrossPack. If that does not work, you can try installing `avr-gcc` with `brew`.)

LUFA has been included as a git submodule, so cloning the repo like this:

```
git clone --recursive git@github.com:computershit/sorry-not-sorry.git
```

will put LUFA in the right directory.

Now you should be ready to rock. Open a terminal window in the `sorry-not-sorry` directory, type `make`, and hit enter to compile. If all goes well, the printout in the terminal will let you know it finished the build! Follow the directions on flashing `Joystick.hex` onto your Teensy, which can be found page where you downloaded the Teensy Loader application.

#### Thanks

Thanks to (Shiny Quagsire)[https://github.com/shinyquagsire23] for his [Splatoon post printer](https://github.com/shinyquagsire23/Switch-Fightstick) and progmem for his [original discovery](https://github.com/progmem/Switch-Fightstick).

Thanks to [bertrandom](https://github.com/bertrandom/snowball-thrower/pull/1) for actually doing all the work, and for the very creative DSL wrapped around the button maps. 