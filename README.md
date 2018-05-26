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



error 1
File "/usr/lib64/python2.7/lib-tk/Tkinter.py", line 1745, in init self.tk = _tkinter.create(screenName, baseName, className, interactive, wantobjects, useTk, sync, use) _tkinter.TclError: no display name and no $DISPLAY environment variable

solution :

export DISPLAY=:0.0

change the ssh -X ***** to ssh -Y ***

error 2
File "/usr/lib64/python2.7/lib-tk/Tkinter.py", line 1745, in init self.tk = _tkinter.create(screenName, baseName, className, interactive, wantobjects, useTk, sync, use) _tkinter.TclError: couldn't connect to display ":0.0"

export DISPLAY=:10.0

error 3
window = Tk.Tk() File "/usr/lib64/python2.7/lib-tk/Tkinter.py", line 1745, in init self.tk = _tkinter.create(screenName, baseName, className, interactive, wantobjects, useTk, sync, use) _tkinter.TclError: couldn't connect to display ":10.0"

solution: detach the screen and reattach then the problem is solved.


# Still not display well

reconnect

export DISPLAY=:localhost:11.0

echo $DISPLAY
localhost:11.0

