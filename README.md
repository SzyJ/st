# st - simple terminal
st is a simple terminal emulator for X which sucks less.

This is my own configuration of the [st terminal](https://st.suckless.org/).

## My additions
* Copy with Alt-w.
* Paste with Ctr-v.
* Scrollback patch applied with Shift/Alt + mousewheel
* Added colour syncing with [PyWal](https://github.com/dylanaraps/pywal/).
* TODO...

# Requirements
In order to build st you need the Xlib header files.

To use the colour changing PyWal must be installed.


# Installation
Edit config.mk to match your local setup (st is installed into
the /usr/local namespace by default).

In the ``` config.h ``` file, update path to your PyWal header for st.
This should be in the format of:
```
   /home/<USER>/.cache/wal/colors-wal-st.h
```


Afterwards enter the following command to build and install st (if
necessary as root):
```
    make clean install
```

# Running st
If you did not install st with make clean install, you must compile
the st terminfo entry with the following command:
```
    tic -sx st.info
```
See the man page for additional details.


# Credits
Based on Aurélien APTEL <aurelien dot aptel at gmail dot com> bt source code.
