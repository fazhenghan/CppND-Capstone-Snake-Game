# CPPND: Capstone Snake Game Example

This is a starter repo for the Capstone project in the [Udacity C++ Nanodegree Program](https://www.udacity.com/course/c-plus-plus-nanodegree--nd213). The code for this repo was inspired by [this](https://codereview.stackexchange.com/questions/212296/snake-game-in-c-with-sdl) excellent StackOverflow post and set of responses.

<img src="snake_game.gif"/>

The Capstone Project gives you a chance to integrate what you've learned throughout this program. This project will become an important part of your portfolio to share with current and future colleagues and employers.

In this project, you can build your own C++ application or extend this Snake game, following the principles you have learned throughout this Nanodegree Program. This project will demonstrate that you can independently create applications using a wide range of C++ features.

## Dependencies for Running Locally
* cmake >= 3.7
  * All OSes: [click here for installation instructions](https://cmake.org/install/)
* make >= 4.1 (Linux, Mac), 3.81 (Windows)
  * Linux: make is installed by default on most Linux distros
  * Mac: [install Xcode command line tools to get make](https://developer.apple.com/xcode/features/)
  * Windows: [Click here for installation instructions](http://gnuwin32.sourceforge.net/packages/make.htm)
* SDL2 >= 2.0
  * All installation instructions can be found [here](https://wiki.libsdl.org/Installation)
  >Note that for Linux, an `apt` or `apt-get` installation is preferred to building from source. 
* gcc/g++ >= 5.4
  * Linux: gcc / g++ is installed by default on most Linux distros
  * Mac: same deal as make - [install Xcode command line tools](https://developer.apple.com/xcode/features/)
  * Windows: recommend using [MinGW](http://www.mingw.org/)

## Basic Build Instructions

1. Clone this repo.
2. Make a build directory in the top level directory: `mkdir build && cd build`
3. Compile: `cmake .. && make`
4. Run it: `./SnakeGame`.


## CC Attribution-ShareAlike 4.0 International


Shield: [![CC BY-SA 4.0][cc-by-sa-shield]][cc-by-sa]

This work is licensed under a
[Creative Commons Attribution-ShareAlike 4.0 International License][cc-by-sa].

[![CC BY-SA 4.0][cc-by-sa-image]][cc-by-sa]

[cc-by-sa]: http://creativecommons.org/licenses/by-sa/4.0/
[cc-by-sa-image]: https://licensebuttons.net/l/by-sa/4.0/88x31.png
[cc-by-sa-shield]: https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg

## Rubric criteria

1. The project demonstrates an understanding of C++ functions and control structures.

* An example of this is the VectorOccupies function in game.cpp, which takes a vector of points and checks if any of them match a given x & y coordinate. The function uses a for each loop to go through a copy of the vector and return true or false accordingly.

2. The project makes use of references in function declarations.

* Two functions in game.cpp, PlaceItem (line 77) and RemoveItem (line 92), use pass-by-reference to modify a vector of SDL_Points. These functions can take any vector as an argument, such as food or poison, and change its contents. Pass-by-reference makes these functions more flexible and efficient.

3. Classes use appropriate access specifiers for class members.

* A new private member function has been added to snake.h, along with an enum on line 36 that replaces the growing boolean. The enum allows the snake to have three different body_state values: None, Grow, and Shrink. None is the default value when the snake is moving normally, Grow is set when the snake eats food and calls the GrowBody function, and Shrink is set when the snake eats poison and calls the ShrinkBody function.

4. Classes abstract implementation details from their interfaces.

* Several functions in game.cpp, such as OpenCell (line 64), VectorOccupies (81), PlaceItem (95), and others, have clear and concise comments that explain their inputs, outputs, and behaviors.

5. The project uses smart pointers instead of raw pointers.

* In game.h, on lines 22 and 23, two vectors are declared that store SDL_Points. Instead of holding the SDL_Points directly, a shared_ptr is used. This ensures that the memory management of the points is handled automatically and safely.
