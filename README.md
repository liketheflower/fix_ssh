# fix_ssh
# error 1:  
 File "/usr/lib64/python2.7/lib-tk/Tkinter.py", line 1745, in __init__
    self.tk = _tkinter.create(screenName, baseName, className, interactive, wantobjects, useTk, sync, use)
_tkinter.TclError: couldn't connect to display "mymachine.com:0.0"


Solution:
the problem is fixed:
1. enable X11 on mac which is changed to X quartz
2. type the command to set the DISPLAY in the remore machine:
```python
export DISPLAY="127.0.0.1:10.0"
```
