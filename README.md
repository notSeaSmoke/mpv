mpv config I use, primarily for anime. Mostly stolen from [LightArrowsEXE](https://github.com/LightArrowsEXE/dotfiles/tree/master/mpv/.config/mpv) with some edits for my own use. 

This config is geared to be used with [Emby](https://emby.media/) -> [jellyfin-mpv-shim](https://github.com/iwalton3/jellyfin-mpv-shim) + [Taiga](https://github.com/erengy/taiga). However, profiles for simulcasts won't work with Emby, since Emby doesn't send the name of the group in the title. Taiga still works so it'll update MAL/Anilist. If you want to use the auto profile for filtering simulcasts, don't use it with Emby.

## How to install the base setup:

**Windows:**<br>
1) Create a new folder in `%appdata%` and call it mpv. <br>
2) Dump the contents of this directory in there. <br>
3) Change the paths as necessary in `mpv.conf`.<br>

## How to install VapourSynth and the filtering dependencies:

### Note: If you do not wish to use VapourSynth for filtering simulcasts, comment out the simulcast profile in mpv.conf. However, Vapoursynth is still required for the rest of the filters (deinterlace, sharpen). 

1) Install the [latest version of VapourSynth](https://github.com/vapoursynth/vapoursynth/releases).<br>
1.1. Install [Python](https://www.python.org/downloads/), and make sure it's added to PATH. Note that VapourSynth doesn't work with Python 3.9 yet, so you'll have to install 3.8 or below.<br>
2) Locate the following directories:<br>
 \* C:\Users\[your username]\AppData\Roaming\VapourSynth\plugins64<br>
 \* C:\Users\[your username]\AppData\Local\Programs\Python\Python38\Lib\site-packages<br>
3) Check the .vpy scripts in the repo (in the `vs` directory) and follow the links to the listed dependencies.
4) Download and move the required files to the relevant directories (Python modules go to the `site-packages` directory, everything else goes in the `plugins64` directory).
5) Verify that the scripts are running as intended by cycling through the profiles and pressing the `~` key during playback. It should tell you if it failed, and if it did what the missing dependencies are.

## Dependencies:

* [Youtube-dl](https://github.com/ytdl-org/youtube-dl/releases)
* [Gandhi Sans](https://www.fontsquirrel.com/fonts/gandhi-sans) and [Noto Sans](https://fonts.google.com/specimen/Noto+Sans)

## Included shaders/scripts:

* [acompressor](https://github.com/mpv-player/mpv/blob/master/TOOLS/lua/acompressor.lua)
* [autocrop](https://github.com/mpv-player/mpv/blob/master/TOOLS/lua/autocrop.lua)
* [autoload](https://github.com/mpv-player/mpv/blob/master/TOOLS/lua/autoload.lua)
* [auto-profiles](https://github.com/wiiaboo/mpv-scripts/blob/master/auto-profiles.lua)
* [boss-key](https://github.com/detuur/mpv-scripts)
* [playlistmanager](https://github.com/jonniek/mpv-playlistmanager)
* [reload](https://github.com/4e6/mpv-reload)
* [repl](https://github.com/rossy/mpv-repl)
* [status-line](https://github.com/mpv-player/mpv/blob/master/TOOLS/lua/status-line.lua)
* [visualizer](https://github.com/mfcc64/mpv-scripts/blob/master/visualizer.lua)


* [FSRCNNX](https://github.com/igv/FSRCNN-TensorFlow/releases)
* [KrigBilateral](https://gist.github.com/igv/a015fc885d5c22e6891820ad89555637)
* [Static Noise Luma](https://pastebin.com/yacMe6EZ)
* [ravu-r3](https://github.com/bjin/mpv-prescalers)