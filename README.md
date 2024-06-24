# 7-Segment-Drivers & reperesenting numbers visually using 7 segment displays
A 7 segment driver using Boolean logic and circuits 
## Overview
In the first part, we need be covering converting a 4-bit nibble input into a 7-bit output (1 for each segment of the display).
In the Second part, we will be covering how to represent bigger numbers using BCD algorithms and ripple blanking.

# Part 1
This includes the construction of the driver itself and numbers 0-9

## Segment divisions and logical K-maps
First of all, we need to figure out the logic of each segmentv of the display, this is done by using a 4 input K-map for each number
### A
![image](https://github.com/gbentham06/7-Segment-Driver/assets/169713724/0afbb6eb-627f-4f4a-9413-a841f0a78751)
This solves and simplifies to A = b'd' + a'c + bd + ac'

### B
![image](https://github.com/gbentham06/7-Segment-Driver/assets/169713724/0c7bc262-aa0b-4fc5-bdc5-78422bf8f457)
This solves and simplifies to B = b' + c'd' + ac' + ad' + a'cd

### C
![image](https://github.com/gbentham06/7-Segment-Driver/assets/169713724/dd876016-753e-45e5-9f84-a95a337a066b)
This solves and simplifies to C = d + a'c' + bc + ab'

### D
![image](https://github.com/gbentham06/7-Segment-Driver/assets/169713724/84e7d995-de0b-4f98-a637-e259e0b29f43)
This solves and simplifies to D = b'd' + ac' + a'b'c + a'cd' + bc'd + abd

### E
![image](https://github.com/gbentham06/7-Segment-Driver/assets/169713724/b7c51c1d-6e0f-46f6-a4cf-539d717519de)
This solves and simplifies to E = b'd' + a'cd' + ac'd'

### F
![image](https://github.com/gbentham06/7-Segment-Driver/assets/169713724/0672f8c7-2a28-46cd-a0a3-149c1424b123)
This solves and simplifies to F = a'c'd' + a'bc' + a'bd' + ab'c' + ab'd' + abc

### G
![image](https://github.com/gbentham06/7-Segment-Driver/assets/169713724/d26e474e-196f-47b7-ba9f-51266a2ad722)
This solves and simplifies to G = bc' + bd' + ac' +ab + a'b'c

## Appling this logic into the circuits
application of this is fairly easy if you structure it using 8 master wires (a,a',b,b',c,c',d,d')

### A
![image](https://github.com/gbentham06/7-Segment-Driver/assets/169713724/9311d4c1-8e8d-4e3a-9367-11ee827f9ef1)

### B
![image](https://github.com/gbentham06/7-Segment-Driver/assets/169713724/adb88ce9-83b6-4f7b-9f56-602d6245bbb9)

### C
![image](https://github.com/gbentham06/7-Segment-Driver/assets/169713724/c4a02741-71d1-40e7-9682-b9dd065b4c41)

### D
![image](https://github.com/gbentham06/7-Segment-Driver/assets/169713724/cea3ca8e-9d37-4733-9c01-0acb455e563d)

### E
![image](https://github.com/gbentham06/7-Segment-Driver/assets/169713724/11b9196e-11d3-48c8-b44d-a285feacb542)

### F
![image](https://github.com/gbentham06/7-Segment-Driver/assets/169713724/08651185-b9e1-403d-9e72-6bc71ff89406)

### G
![image](https://github.com/gbentham06/7-Segment-Driver/assets/169713724/9f029ae1-7a2d-485f-b89b-4917013aafe7)
