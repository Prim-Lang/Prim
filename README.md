# Prim
Tooling for using Prim - a safe subset of Nim


## Functions

With Prim, whenever possible, prefer using `func` over `proc` (not that in Nim `func` == `proc` with the `{.noSideEffects.}` pragma).

To the exent possible, we  would like to have pure functions.
The first possible hurdle is the presence of `var` parameters, but disabling `var` should address this issue.

Something else to be aware of is that certain defects arising from unrecoverable program errors,
such as certain OS errors (running out of memory, etc.). Assertions also fall into this category in Nim.
Mathematical functions, of course, don't have assertion errors, but this is a reality of using physical
hardware.
