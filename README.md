Many people do not provide enough information when reporting bugs.

Why?

Most people are unaware of what information may be relevant when reporting a
bug. So, they often omit information that the programmers need to fix the bug.

The first step in responding to a bug report is to try and reproduce the
problem. If a programmer cannot reproduce your problem, they cannot help you
solve it.

**Good bug reports are concise but do not omit information.**

# Components of a Bug Report

A good bug report consists of:

* Test Case: Minimal and complete code that demonstrates the bug.
* Steps to Reproduce: The step of actions will produce the Observed Output using the Test Case when performed in the Environment.
* Expected Output: Your expectation of what should have happened when following the Steps to Reproduce.
* Observed Output: The complete and unabridged output that you experienced when following the Steps to Reproduce instead of the Expected Output.
* Environment: The Environment is a description of the software and hardware configuration that you used when you experienced the Observed Output by following the Steps to Reproduce. 

## Test Case

The Test Case is minimal and complete code that demonstrates the bug.

### Minimal

The Test Case must use as little code as possible to demonstrate the bug. There
are two approaches to minimizing test cases.

* Write From Scratch: Create a new program, and add in only what is needed to
demonstrate the bug by following the Steps to Reproduce. This approach works
best when you believe you know the source of the bug.
* Reduce Existing Code: Try temporarily removing parts of the code, and then
check if it still reproduces the bug when you follow the Steps to Reproduce.
Tools like [creduce](https://embed.cs.utah.edu/creduce/) and
[delta](http://delta.tigris.org/) can be used to automate reduction.

### Complete

The Test Case must be a complete and valid C++ program. All the code needed to
compile your Test Case must be included in the Test Case.

* The Test Case should be a single source file. 
* You must define a `main` function if the bug occurs at runtime.
* You may only use the C++ standard library and the software that you are reporting the bug against.

## Steps to Reproduce

The Steps to Reproduce is the sequence of actions that will produce the
Observed Output using the Test Case when performed in the Environment.

* Any auxiliary files (configuration files, scripts, input files for the Test
Case, etc) that are used in the Steps to Reproduce must be included in the bug
report.
* You must verify that the Steps to Reproduce produce the Observed Output in
the Environment.

## Expected Output

The Expected Output is your expectation of what you believe should have
happened when you followed the Steps to Reproduce.

* You should explain why you believe the Expected Output is the correct behavior.
* Support your explaination by citing documentation, standards or existing best practice.

## Observed Output

The Observed Output is the complete and unabridged output that you experienced
when following the Steps to Reproduce instead of the Expected Output

* Any files created when performing the Steps to Reproduce are part of the Observed Output.
* For command line applications, the Observed Output includes the entire textual output of running the Steps to Reproduce on your command line.
* For graphical applications, the Observed Output includes screenshots or screen recordings as you perform the Steps to Reproduce.
* To the best of your ability, explain why the Observed Output happened.

## Environment

The Environment is a description of the software and hardware configuration
that you used when you experienced the Observed Output by following the Steps
to Reproduce. 

The following must be included in the Environment: 

* Version of the software you are reporting the bug against. Try a few different versions and attempt to determine which version are broken, and which (if any) are not broken.
* Whether or not the bug is a regression. A regression is a bug that did not occur with an earlier version of the software.
* Name and versions of all software used in the Test Case or Steps to Reproduce.
* Compiler Toolchain Type and Version
* Operating System Type and Version
* CPU Architecture
* Kernel Type and Version

# Examples

TODO
