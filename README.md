# VHDL Counter Overflow Bug
This repository demonstrates a common error in VHDL:  an integer counter that doesn't handle overflow correctly.  The `buggy_counter.vhdl` file contains the erroneous code, while `fixed_counter.vhdl` provides the corrected version.

## The Bug
The `buggy_counter` entity is intended to count from 0 to 15. However, once it reaches 15, the next increment will cause an overflow, resulting in unpredictable behavior, potentially wrapping around to 0 or causing a simulation failure.

## The Solution
The `fixed_counter` entity addresses this by explicitly checking for the upper bound before incrementing. This prevents overflow and ensures correct operation.

## How to use
1. Clone this repository.
2. Simulate both `buggy_counter.vhdl` and `fixed_counter.vhdl` using your preferred VHDL simulator (e.g., ModelSim, GHDL).
3. Observe the behavior of each counter.  The buggy counter will eventually overflow, while the fixed counter will stop at 15.