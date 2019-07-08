# Triangle library for x64

Because the original version use long type to represent pointer type, in x64 pointer type is 64 bit long. Replace all long type to __int64 can solve this problem.

# How to build

To use triangle in windows, we must delete the unix-related function. Luckily, if you just want to build a library, the thing you should take care about is just unix timestamp which is used to evaluate the performance of this library.

So, to build this library, you should define these macro in your preprocessor options.

```c++
#define NO_TIMER
#define ANSI_DECLARATORS
#define TRILIBRARY
```
