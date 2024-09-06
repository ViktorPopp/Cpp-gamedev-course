# Raylib Course
In this course you will learn how to create your own games using Raylib.

## 1. Creating a window
As always the first thing you need to do is create a window or else your drawings will go to the void. Create a window using ```InitWindow(int width, int height, const char* title)```. You can now check if the window is ready to be drawn on by calling ``` IsWindowReady(void)```. Now we wan't to create the game loop. The game loop is the while loop that runs each frame until the user closes the window.
```cpp
while (!WindowShouldClose()) {}
```
So finally if the user closes the window we have to close the program. We can do that by calling ```CloseWindow(void)```. Here is our code so far:
```cpp
#include "raylib.h"

int main() {
    /* Initialize */ 
    const int window_width = 800;
    const int window_height = 600;
    const char* title = "My first window";
    InitWindow(window_width, window_height, title);

    /* Game loop */
    while (!WindowShouldClose()) {

    }

    /* Terminate */
    CloseWindow();
}
```
Now note that for the most part Raylib does not use objects. For C++ devs i recommend creating your own wrapper library around Raylib if you like OOP. Also before you continue i also recommend to try out SFML as it also is a great library for games that use a object oriented approach instead of Raylib's functional approach.