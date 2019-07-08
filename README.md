# Triangle library for x64

cause the original version use long to represent pointer value. However in x64 the  pointer is 64 bit long. Replace the whole long to __int64 can solve this problem.

# How to build

To use triangle in windows, we must delete the unix-related function. Luckily, if you just want to build a library, the thing you should take care about is just unix timestamp which evaluate the performance of this library.

So, to build this library, you should define these macro in your preprocessor options.

```c++
#define NO_TIMER
#define ANSI_DECLARATORS
#define TRILIBRARY
```