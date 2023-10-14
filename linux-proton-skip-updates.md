For those on Linux using Proton, I have the sfse_loader.exe installed as a 2nd separate game in Steam.  This lets me use the prior version of Starfield until all the mods I use are updated.  This only works if you use this approach *prior* to upgrading your game to the latest version.

Using "Games, Add a non-Steam Game...":

- Target: `"/home/{your-user-name}/.local/share/Steam/steamapps/common/Starfield/sfse_loader.exe"`
- Start In: `/home/{your-user-name}/.local/share/Steam/steamapps/common/Starfield/`
- Launch Options: `-- Starfield.exe`
- Compatibility: Turn ON the "force the use..." if you want to pick Proton Experimental.

BUT - That creates a separate `compatdata` folder and you'll lose access to your mods/saves in the other WINE prefix.  This is fixable if you feel frisky as you can create a symlink from the old folder to the new folder.  

1. Launch once, this creates a new folder in `compatdata`.
2. Shut the game back down.
3. Rename the new folder out of the way.
4. Create a symbolic link from the old directory to the new directory: `ln -s 1716740 3367664357`

Note that "3367664357" will probably be different for your install and "1716740" is the existing Starfield folder.
