SimpleNES
=============


An NES emulator written in C++ for purely educational purposes.

Currently WIP.

Only games with atmost 2 program banks, 1 character banks and no "mapper" are supported.  
Only one controller is setup at the moment.


Examples of games that have been tested to run (but not limited to):

(USA/Japan or World versions only i.e. NTSC compatible)

* Super Mario Bros.
* Wrecking Crew
* Ice Climber
* Mario Bros.
* Donky Kong
* Donkey Kong Jr.
* Arkanoid
* Balloon Fight
* Tennis
* Elevator Action
* Excite bike

Screenshots
------------------------
![Screenshot 1](http://amhndu.github.io/Projects/screenshots/nes4.png)
![Screenshot 2](http://amhndu.github.io/Projects/screenshots/nes2.png)
![Screenshot 3](http://amhndu.github.io/Projects/screenshots/nes3.png)
![Screenshot 4](http://amhndu.github.io/Projects/screenshots/nes1.png)


Compiling
-----------

You need:
* SFML 2.0+ development headers and library
* C++11 compliant compiler
* CMake build system

Compiling is straight forward with cmake, just run cmake on the project directory with CMAKE_BUILD_TYPE=Release
and you'll get Makefile or equivalent for your platform, with which you can compile the emulator

For e.g., on Linux/OS X/BSDs:
```
$ cd SimpleNES
$ mkdir build/ && cd build/
$ cmake -DCMAKE_BUILD_TYPE=Release ..
$ make -j4    #Replace 4 with however many cores you have to spare
```

Running
-----------------

Just pass the path to a .nes image like

```
$ ./SimpleNES ~/Games/super_mario_bros.nes
```

Only for demonstration purposes, [download this archive of roms](https://www.dropbox.com/s/mfzukqy8uul4ae3/demo-roms.tar.gz?dl=0)


For supported command line options, try
```
$ ./SimpleNES -h
```

Controller
-----------------

These keybindings are hard-coded (for Player 1)

 Button        | Mapped to
 --------------|-------------
 Start         | Return/Enter
 Select        | Right Shift
 A             | J
 B             | K
 Up            | W
 Down          | S
 Left          | A
 Right         | D

F2 pauses/resumes emulation

