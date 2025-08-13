# External script for [Wii wallpaper](https://steamcommunity.com/sharedfiles/filedetails/?id=3526096300) by [Lillykyu](https://www.lillykyu.gay/)
### Original Script by [Pixel1011](https://github.com/Pixel1011) - Modified to Support Windows 11 24H2


## Usage instructions
**NOTE: make sure your path to where you extract it does not have a space in it! powershell is terrible**

1. Download the zip file from releases.
2. Extract into a folder
3. Enable Verbose logging in wallpaper engine
4. Edit the info.txt with your executables and log path in the format shown in the file
5. Run ``install.bat`` and if that succeeds then run ``start.bat``

If you need to make any edits, run ``stop.bat``, edit your info.txt then run ``start.bat`` to restart it

**Another note: this does not directly support applications with arguments, if you wish to run an application with arguments, use ``cmd /c yourcommandhere``, eg ``cmd /c start https://www.youtube.com/watch?v=dQw4w9WgXcQ``. You can check [here](https://docs.google.com/document/d/1BVPGTDyzMaWZIGxTkfvdh9g5MXfPOBSAIsLmjvk29fE/edit?tab=t.0) for more examples to put in your info.txt!**

**Video tutorials [here!](https://docs.google.com/document/d/1BVPGTDyzMaWZIGxTkfvdh9g5MXfPOBSAIsLmjvk29fE/edit?tab=t.tl4p3yca6zrf)**

Once that is done, you dont need to do anything else, just keep these files and the script will automatically start upon reboots!

If you wish to uninstall the program, run ``uninstall.bat``, delete these files and your done!

## FAQ/Common issues


### Your getting an error message looking like this:*
![image](http://img.pixelator.xyz/3PpSF0iN.png)
Remove spaces from your path to where you extracted the zip! (this does not mean within your info.txt)

In this example the folder "Wii Wallpaper" has a space in the middle, remove it and rerun install!

---

### "The operation was canceled by the user. OR when running start, a powershell window flashes with an error and then closes, with your wallpaper not functioning"
![image](http://img.pixelator.xyz/mTE2qzag.png)

This is caused by the exe being blocked by windows smartscreen.

You will need to go into the dont-touch folder and run the ``lillywallpaper.exe`` manually once

You may also see a popup looking like this

![image](http://img.pixelator.xyz/JY93dHgw.png)


Click __More info__ and press **Run Anyways**.
You may then close the cmd that pops up and run ``stop.bat``
You can then run ``start.bat`` and it should run as normal!

---

If all else fails, try restarting your pc!

## Build instructions
### IGNORE IF USING FOR GENERAL USAGE
Run these commands in order in the main directory:
  - ``pnpm i or npm i``
  - ``tsc``
  - ``pkg .\dist\index.js --targets latest-win-x64 --output ./dont-touch/lillywallpaper.exe``

Support the original creator on ko-fi! 

:3
[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/N4N6145I0V)

(or feel free to leave a star, that is nice too :D)
