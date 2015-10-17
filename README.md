## Media Player Classic Qute Theater

A clone of Media Player Classic reimplimented in Qt.

[Media Player Classic Home Cinema] (mpc-hc) is considered by many to be the
quintessential media player for the Windows desktop.  Media Player Classic
Qute Theater (mpc-qt) aims to reproduce most of the interface and
functionality of mpc-hc while using [libmpv] to play video instead of
DirectShow.


## Features

* play back simple video files
* control playback using the control buttons
* seek with the seek bar
* navigate by chapters
* select audio/video/subtitle tracks
* change playback rate
* resize the window automatically using zoom factors
* build playlists with the quick open command
* batch play from playlists
* launch files from from the command line
* stream video from streaming sites

**Note:**  This is alpha software and some of the functionality isn't written
yet.  For the most part, unwritten portions relate to setting options,
streaming from devices, and storing favorites.


### Improvements over mpc-hc

**Multiple playlists:**  When you're watching shows on your backlog, load
every show into seperate playlists and still keep track of the last played
file *for each playlist*.  Finally you can eliminate the need to keep track of
your progress in a spreadsheet, all while never leaving the comfort of your
favorite media player.

**More to come:** Comprehensive video-output filter support; Encoding support.
Suggestions welcome.


## Prequisities

**For plebs:**  You need the Qt5 sdk installed and an edition of libmpv.  On
ubuntu you can install them with

>sudo apt-get install qtcreator libmpv-dev

If you want Qt5 documentation in Qt Creator, add *qt5-doc* to that command.
Beware that this may result in unguaranteed behaviour because package versions
usually lag by a version or so.

**For pros:**  Install qt sdk and compile [libmpv] from git head with
``--enable-libmpv-shared``.


## I don't know git, how do I run this?

You'll have to perform a little bit of footwork beforehand.  What you're going
to do is make a directory for this repo to sit in, and then compile it.

First ensure you have the prequisites as mentioned above, then open a terminal
and `cd` into your general source-code directory. If one does not exist,
`mkdir` one.

>mkdir src

>cd ~/src

Then, make a directory to checkout this git into, and `cd` into that.

>mkdir mpc-qt

>cd mpc-qt

At this stage you can checkout this git repository using the following
command:

>git checkout https://github.com/cmdrkotori/mpc-qt.git

Finally, `cd` into the checked-out repository and run qtcreator.

>cd mpc-qt

>qtcreator mpc-qt.pro

Use qtcreator's suggested build setup and click "Configure Project", then
press the big green arrow button in the bottom-left corner.  After this, the
executable should be in `~/src/mpc-qt/build-mpc-qt...`. Look for the `mpc-qt`
binary and run that whenever you want to, or stick a shortcut to that on your
taskbar/desktop.

[Media Player Classic Home Cinema]:https://mpc-hc.org/
[libmpv]:https://github.com/mpv-player/mpv
[mpv-build]:https://github.com/mpv-player/mpv-build
[bomi]:https://github.com/xylosper/bomi
[baka]:https://github.com/u8sand/Baka-MPlayer
