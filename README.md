# Undefined Behavior when Accessing Vector via Raw Pointer
This code demonstrates a common error in C++ when using raw pointers to access elements in a `std::vector`.  Accessing elements beyond the vector's bounds leads to undefined behavior, potentially resulting in crashes or corrupted data.

## Bug Description
The bug lies in accessing `ptr[10]` in the code.  The vector `vec` only has 10 elements (indices 0-9). Attempting to access index 10 invokes undefined behavior. 

## How to Reproduce
1. Compile and run the provided `bug.cpp` file.
2. Observe the potential crash or unexpected behavior.

## Solution
The solution uses range-based for loops or `at()` method to prevent out-of-bounds access.