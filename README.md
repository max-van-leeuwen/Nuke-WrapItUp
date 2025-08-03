
![nuke collect all files for nuke script](https://maxvanleeuwen.com/wp-content/uploads/WrapItUp_nuke.png)

![collect nuke get all media for nukescript](https://maxvanleeuwen.com/wp-content/uploads/WrapItUp_CollectedMedia.png)


<br><br>

# WrapItUp

WrapItUp is an easy-to-use tool that can collect and relink almost all files required to make a Nuke script work on another machine. It has a user interface if you run it in Nuke, it can be executed from a command-line window for batch operations, and it can be called using a Python function.

I made sure to cram the entire thing in just one Python file, so you can simply drag-and-drop the file into Nuke's script editor if you wish to use it just once. To quickly collect all files for a nuke file, simply choose an empty folder in the “collection folder” box at the top of the window and hit Start.

Tested on Windows, Mac OS, and Linux (CentOS).

<br><br>

## Features and Settings

- Three copies of the Nuke script will be collected: the original, a relinked one, and a relative-relinked one (using a python-embedded TCL expression). The relative-relinked Nuke script will stay linked to its media, even if you move it to a completely different machine - as long as the media is right next to it.
- Media files with the path variables ####..., %**d (printf), %v and %V are supported.
- Gizmos will be collected, and the necessary menu.py and init.py files will be generated. Simply place these files in your .nuke folder to install them.
- A detailed CSV log file is generated to review which files were copied.

**Not supported:** Shared library plugins, (.dll, .dylib and .so files). There are simply too many dependencies and licenses involved to keep track of these.

See [my website (maxvanleeuwen.com/wrapitup)](https://maxvanleeuwen.com/wrapitup) for more information about all features and settings in this script, and for command-line/Python use!

<br><br>

## Installation

<br><br>

### Standard Nuke Installation

1. Place the WrapItUp folder in your .nuke folder (or somewhere else on your computer).
2. Go to your .nuke folder, and create a file called 'init.py'. If such a file already exists, open it.
3. In the init.py file, add this line of text to the end and save it:
   ```python
   nuke.pluginAddPath('./WrapItUp')
   ```

If you want to place the folder somewhere else than in the .nuke folder, make sure to change the path in the init.py file so that it points to that other path instead!

<br><br>

### Only Run Once (in Nuke)

If you are only running it once, you can simply drag-and-drop the WrapItUp/WrapItUp.py file into the script editor panel in Nuke and click 'Run the script'.

<br><br>

### Installation using NukeShared

1. Place the WrapItUp folder in the '_AutoInstaller' repository.

NukeShared is a way of installing plugins by dragging/dropping them in folders, see [this page](https://maxvanleeuwen.com/nukeshared) for more information.

If you encounter any issues (or if you have feedback/ideas), [let me know (maxvanleeuwen.com/contact)](https://maxvanleeuwen.com/contact)!

<br><br>

## Updates

### 2.2

- Nuke 16 (PySide 6) compatibility

### 2.1

- Added maximum of 5 node names in a path when media is reused (to prevent path name length overflow)

### 2.0

- Added -d flag in terminal to skip all disabled nodes, and (*) in UI list to show when nodes are disabled

### 1.9

- Fixed Nuke 13 (Python 3) compatibility

### 1.8

- Fixed Nuke 10.5 compatibility

### 1.7

- Added support for media in Project Directory (root settings)
- Added interactive license (nuke_i) support (for internal use, when scripts are relinked)
- Added more information to log CSV
- Fixed bug with font folder relinking
- Fixed bug with 0b files freezing the copying process

### 1.6

- Relinking and relative relinking now only modifies knobs of media that is not user-ignored

### 1.5

- Fixed 'open folder' keyboard shortcut
- Code cleanup

### 1.4

- Added 'go to node' button
- Fixed error on empty project font path

### 1.3

- Fixed TCL support on font paths
- Fixed issue with gizmo's and nuke script containing dots in their names
- UI labels now evaluate TCL as well
- Log now stores used nuke version

### 1.2

- File paths with TCL are supported
- Folder browser will ask to create new folders if the selected path does not exist

### 1.1

- Added PySide support (for Nuke 10.5 and older)
- Fixed Nuke closing on user interruption when 'exit on finish' is checked
- Fixed Nuke asking to save your Nuke script when 'exit on finish' is checked and script has not been saved

### 1.0

- Initial release
