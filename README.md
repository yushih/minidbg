# A trace debugger
Trace debugger is built upon https://github.com/TartanLlama/minidbg. It traces the execution of program on the source level and logs each excuted line to a file.

## Usage
A new debugger command is added:

```trace <source file> <log file>```

Each time a line in `<source file>` is executed, a line `<source file>:<line number>` is logged to `<log file>`.

## Rationale
This tool was created to debug a specific problem:
- The code was complex and unfamiliar;
- When a function was invoked twice with the same parameter, different results were produced.

The idea was to trace each invocation and see where the log started to bifurcate. With the help of this tool I was able to pinpoint the problem without examining the whole source.
