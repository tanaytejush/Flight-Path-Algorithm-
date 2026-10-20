# Flight-Path-Algorithm

A C++ implementation of the **closest pair of points** problem using divide and conquer. Given a set of points in a 2D plane, it finds the smallest distance between any two of them in O(n log² n) time.

## How it works

1. Sort the points by x-coordinate.
2. Recursively split the set in half and find the smallest distance in each half.
3. Take the smaller of the two distances (`d`) and check the strip of points within `d` of the dividing line, sorted by y-coordinate.
4. For small sets (3 points or fewer) a brute-force check is used.

This kind of routine is useful as a building block for collision and proximity checks, for example keeping flight paths apart.

## Run it

```bash
g++ flight_path_algorithm.cpp -o closest
./closest
```

The example points are hard-coded in `main()`:

```cpp
Point P[] = {{2, 3}, {12, 30}, {40, 50}, {5, 1}, {12, 10}, {3, 4}};
```

Edit that array to try your own input. The program prints the smallest distance found.

## Files

| File | Description |
|------|-------------|
| `flight_path_algorithm.cpp` | Closest-pair implementation and driver code |

## Credits

The algorithm follows the standard divide-and-conquer approach described on GeeksforGeeks.


---

<sub>Made by [tanaytejush](https://github.com/tanaytejush)</sub>
