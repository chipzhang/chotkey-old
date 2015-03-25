# cHotKey #
Cross-platform keyboard automation, mapping and logging.
<br>
<br>
<h2>(A) Features:</h2>
<h4>1. Hotkey triggers.</h4>
Execute programs on specific hotkey triggers. It can capture a single modifier key and even multiple times of keystrokes (e.g. twice ctrl).<br>
<h4>2. Keyboard mapping.</h4>
Generate fake key strokes on specific triggers.<br>
<h4>3. Keystroke logging.</h4>
Log the user keyboard strokes to a file, with detailed information (Date, time, window title and window class name).<br>
<h4>4. Cross-platform.</h4>
The windows version and Linux version share the same configuration file format.<br>
<br>
<br>
<br>
<h2>(B) Problems:</h2>
<h4>1. Currently the program is command line only.</h4>
<h4>2. Currently the program only supports en-US keyboard layout.</h4>
<h4>3. The Linux version has the following problems (see next section for details):</h4>
<ul><li>The hotkeys are not consumed, but propagated to other programs.<br>
</li><li>Need root privileges.<br>
<br>
<br>
<h2>(C) Technology notes related to the Linux version:</h2>
There are many methods to capture keystrokes under Linux: Using X11 functions, input-subsystem, or I/O port.<br>
<br>
<br>
The first way doesn't need root privileges but it can only capture key bindings with modifier key. i.e. It doesn't support global keyboard listening and doesn't support capturing a single modifier key. (At least as far as I have tried, that's true) The other ways need root privileges.<br>
<br>
<br>
Since there are already many existing similar applications (e.g. xbindkeys) but they cannot capture a single modifier key, my aim is to write a new program that can implement it.<br>
<br>
<br>
This program is actually implemented using the second method.<br>
For input-subsystems, program can only capture a keystroke (read from input device) or simulate a keystroke (write to input device). There is no way to consume a keystroke (i.e. stop it from propagating).<br>
<br>
<br>
<b>In conclusion, there is no perfect solution for Linux.</b>
<br>
<br>
<br>
<h3><a href='http://chotkey.googlecode.com/files/cHotKey%201.00%20Binaries%20%28Public%29.zip'>Download</a></h3>