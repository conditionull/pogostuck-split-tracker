### Linux compatible version of [this project](https://github.com/derJunker/pogostuck-split-tracker)

I’ve been running this on Arch for several months without any problems. Feel free to report any issues you come across

> [!NOTE]
> Check out the [releases](https://github.com/conditionull/pogostuck-split-tracker/releases) tab if you don't want to manually install

### Manual Installation
Install the latest version of Node.js
```sh
git clone git@github.com:conditionull/pogostuck-split-tracker.git
cd pogostuck-split-tracker/
npm install
npm run dist
```
Locate the executable
```sh
cd dist
./pogostuck-split-tracker-1.1.1.AppImage 
```

You probably want an easy way to launch the application.
Create a desktop entry:
```sh
cd ~/.local/share/applications/
touch pogo-split-tracker.desktop
# editor of your choice
nvim pogo-split-tracker.desktop 
```

Paste the following in `pogo-split-tracker.desktop`:
```ini
[Desktop Entry]
Name=Split Tracker
Exec=ABSOLUTE/PATH/TO/pogostuck-split-tracker/dist/pogostuck-split-tracker-1.1.1.AppImage
Icon=steam_icon_688130
Terminal=false
Type=Application
Categories=Game;
```
Make sure to correct the exec path^^
<br /><br />

Usually, desktop entry changes are automatically picked up by the desktop environment.

If this is not the case, and you want to forcefully update the desktop entries defined in ~/.local/share/applications, run the following command: 
```sh
update-desktop-database ~/.local/share/applications
```
Your app launcher should now be listing the application^^
> [!TIP]
> If something is still wrong. Add the `-v` (verbose) argument to show possible desktop entry errors. _(lacks MimeType key warning can be ignored)_

<br />

> [!IMPORTANT]
> This is a fork, check out the [full details here](https://github.com/derJunker/pogostuck-split-tracker) to get started once you launch the application. [derJunker](https://github.com/derJunker) even made a [video guide!](https://www.youtube.com/watch?v=TiV_zLOi0zc)<br />
If you want to support the original author [click here](https://buymeacoffee.com/derjunker)