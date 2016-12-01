Title: Linux processes
Date: 2016-12-01 19:23

## Possible process states
- D    uninterruptible sleep (usually IO)
- R    running or runnable (on run queue)
- S    interruptible sleep (waiting for an event to complete)
- T    stopped by job control signal
- t    stopped by debugger during the tracing
- W    paging (not valid since the 2.6.xx kernel)
- X    dead (should never be seen)
- Z    defunct ("zombie") process, terminated but not reaped by its parent
