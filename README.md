# VHDL Counter Bug

This repository demonstrates a common, subtle bug in VHDL code: an off-by-one error in a simple counter.  The `bug.vhdl` file contains the buggy code, while `bugSolution.vhdl` provides a corrected version.

The bug is related to how the counter handles the rollover condition. This could lead to unexpected behavior or glitches in a larger design.

## Bug Description

The counter is intended to count from 0 to 15 and then wrap around.  However, a subtle flaw in the rollover condition might cause it to skip a count or behave erratically.

## How to reproduce

1. Simulate the `bug.vhdl` code using a suitable VHDL simulator (e.g., ModelSim, GHDL).
2. Observe the `count` output's behavior, particularly when it approaches and passes the maximum count of 15.  The counter's behavior will differ from the expected behavior.

## Solution

The corrected code in `bugSolution.vhdl` addresses the issue by ensuring the rollover condition is properly handled. 

## Further Notes

This example highlights the importance of carefully testing VHDL code and paying close attention to edge cases, such as rollover conditions, to prevent subtle and difficult-to-detect errors.