# VHDL Counter Bug: Unexpected Reset

This repository demonstrates a common bug in VHDL counters:  unintended resets due to improper handling of counter overflow.  The `buggy_counter.vhd` file contains the buggy code, while `fixed_counter.vhd` shows the corrected implementation.

**Bug Description:**
The original VHDL counter resets to 0 when it reaches the maximum count (15). While this might be intended behavior in some scenarios, it's often an oversight, causing unexpected behavior in the overall system.  The issue is not immediately apparent in simulation unless specific test cases are used.

**Solution:**
The corrected version (`fixed_counter.vhd`) provides a clear approach to avoid the accidental reset.  It introduces an additional condition within the 'if' statement to handle the overflow scenario as intended.  You may want to incorporate modulo arithmetic for other scenarios.