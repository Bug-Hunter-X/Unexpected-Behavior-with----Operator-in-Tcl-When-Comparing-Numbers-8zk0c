# Tcl Bug: Unexpected == Behavior with Numeric Strings

This repository demonstrates a common, yet subtle, error in Tcl programming involving the `==` operator and numeric string comparisons.

## The Problem

Tcl's `==` operator performs string comparison.  This means that even if two strings represent numerically equivalent values, if the string representations differ, `==` will return `0` (false).

The `bug.tcl` file contains a procedure `badproc` which illustrates this issue.  It attempts to compare two numbers but fails to produce the correct result if the inputs are strings that represent those numbers.

## The Solution

The solution involves using the `expr` command to perform numerical comparison.  The `bugSolution.tcl` file demonstrates the corrected procedure.

## How to Run

1.  Clone this repository.
2.  Run the `bug.tcl` script using a Tcl interpreter (e.g., `tclsh bug.tcl`). Observe the unexpected results.
3.  Run the `bugSolution.tcl` script.  Observe the correct results.
