Title: Debugging of CPython processes with gdb
Date: 2016-04-25

Key points from [post](http://podoliaka.org/2016/04/10/debugging-cpython-gdb/) by Roman Podoliaka

Prerequisites
-------------

Install gdb and debugging symbols for CPython

    apt-get install gdb python-gdb

The installed debugging symbols will be used by the CPython script for gdb (`cpython/Tools/gdb/libpython.py`) in order to analyze the [PyEval_EvalFrameEx](https://docs.python.org/2/c-api/veryhigh.html#c.PyEval_EvalFrameEx) frames and map those to application level functions in your code. A frame is essentially a function call and the associated state in a form of local variables, CPU registers, etc.

Debugging
---------

Attach to a running CPython process

    gdb /usr/bin/python -p $PID

### Commands

`py-bt`

Get an application level backtrace for the current thread. Note that some frames are "missing". This is expected, as gdb counts all the interpreter level frames and only some of those are calls in application level code - PyEval_EvalFrameEx ones.

`py-list`

Find out what exact line of the application code is currently being executed.

`py-locals`

Look at local variables and their values.

Refer to the [debugging guide](https://docs.python.org/devguide/gdb.html) for complete list of available commands.
