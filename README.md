<p><span style="color: #000000;"><img src="https://maxvanleeuwen.com/wp-content/uploads/WrapItUp_nuke.png" alt="nuke collect all files for nuke script" width="675" height="676" /></span></p>
<p><span style="color: #000000;"> </span></p>
<p><span style="color: #000000;"> </span></p>
<p><span style="color: #000000;"><img src="https://maxvanleeuwen.com/wp-content/uploads/WrapItUp_CollectedMedia.png" alt="collect nuke get all media for nukescript" /></span></p>
<p><span style="color: #000000;"> </span></p>
<p><span style="color: #000000;"> </span></p>
<p><span style="color: #000000;"> </span></p>
<p><span style="color: #000000;"> </span></p>
<p><span style="color: #000000;"><strong>WrapItUp</strong></span></p>
<p><span style="color: #000000;"> </span></p>
<p><span style="color: #000000;">WrapItUp is an easy-to-use tool that can collect and relink almost all files required to make a Nuke script work on another machine.</span><br /><span style="color: #000000;">It has a user interface if you run it in Nuke, it can be executed from a command-line window for batch operations, and it can be called using a Python function.</span></p>
<p><span style="color: #000000;">I made sure to cram the entire thing in just one Python file, so you can simply drag-and-drop the file into Nuke's script editor if you wish to use it just once.<br />To quickly collect all files for a nuke file, simply choose an empty folder in the “collection folder” box at the top of the window and hit Start.</span></p>
<p> </p>
<p><span style="color: #000000;">Tested on Windows, Mac OS, and Linux (CentOS).</span></p>
<p><span style="color: #000000;"> </span></p>
<p><span style="color: #000000;"> </span></p>
<p><span style="color: #000000;"> </span></p>
<p><span style="color: #000000;"> </span></p>
<p><span style="color: #000000;"><strong>Features and settings</strong></span></p>
<p><span style="color: #000000;"> </span></p>
<ul>
<li><span style="color: #000000;">Three copies of the Nuke script will be collected: the original, a relinked one, and a relative-relinked one (using a python-embedded TCL expression).</span><br /><span style="color: #000000;">The relative-relinked Nuke script will stay linked to its media, even if you move it to a completely different machine - as long as the media is right next to it.</span></li>
<li><span style="color: #000000;">Media files with the path variables ####..., %**d (printf), %v and %V are supported.</span></li>
<li><span style="color: #000000;">Gizmos will be collected, and the necessary menu.py and init.py files will be generated. Simply place these files in your .nuke folder to install them.</span></li>
<li><span style="color: #000000;">A detailed CSV log file is generated to review which files were copied.</span></li>
</ul>
<p><span style="color: #000000;"> </span></p>
<p><span style="color: #000000;">Not supported: Shared library plugins, (.dll, .dylib and .so files).</span><br /><span style="color: #000000;">There are simply too many dependencies and licenses involved to keep track of these.</span></p>
<p><span style="color: #000000;"> </span></p>
<p><span style="color: #000000;">See <span style="color: #0000ee;"><a href="https://maxvanleeuwen.com/wrapitup"><span style="color: #0000ee;">my website (maxvanleeuwen.com/wrapitup)</span></a></span> for more information about all features and settings in this script, and for command-line/Python use!</span></p>
<p><span style="color: #000000;"> </span></p>
<p><span style="color: #000000;"> </span></p>
<p><span style="color: #000000;"> </span></p>
<p><span style="color: #000000;"> </span></p>
<p><span style="color: #000000;"><strong>Installation</strong></span></p>
<p><span style="color: #000000;"> </span></p>
<p><span style="color: #000000;"><em>Standard Nuke installation</em></span></p>
<p><span style="color: #000000;"> </span></p>
<ol>
<li><span style="color: #000000;">Place the WrapItUp folder in your .nuke folder (or somewhere else on your computer)</span></li>
<li><span style="color: #000000;">Go to your .nuke folder, and create a file called 'init.py'. If such a file already exists, open it.</span></li>
<li><span style="color: #000000;">In the init.py file, add this line of text to the end and save it:</span><br /><span style="color: #000000;">nuke.pluginAddPath('./WrapItUp')</span></li>
</ol>
<p style="margin-left: 30px;"><span style="color: #000000;">If you want to place the folder somewhere else than in the .nuke folder, make sure to change the path in the init.py file so that it points to that other path instead!</span></p>
<p><span style="color: #000000;"> </span></p>
<p><span style="color: #000000;"> </span></p>
<p><span style="color: #000000;"><em>Only run once (in Nuke)</em></span></p>
<p><span style="color: #000000;"> </span></p>
<p style="margin-left: 30px;"><span style="color: #000000;">If you are only running it once, you can simply drag-and-drop the WrapItUp/WrapItUp.py file into the script editor panel in Nuke and click 'Run the script'.</span></p>
<p><span style="color: #000000;"> </span></p>
<p><span style="color: #000000;"> </span></p>
<p><span style="color: #000000;"><em>Installation using NukeShared</em></span></p>
<p><span style="color: #000000;"> </span></p>
<ol>
<li><span style="color: #000000;">Place the WrapItUp folder in the '_AutoInstaller' repository.</span></li>
</ol>
<p style="margin-left: 30px;"><span style="color: #000000;"> </span></p>
<p style="margin-left: 30px;"><span style="color: #000000;">NukeShared is a way of installing plugins by dragging/dropping them in folders, see <span style="color: #0000ee;"><a href="https://maxvanleeuwen.com/nukeshared" target="_blank"><span style="color: #0000ee;">this page</span></a></span> for more information.</span></p>
<p><span style="color: #000000;"> </span></p>
<p><span style="color: #000000;"> </span></p>
<p><span style="color: #000000;"> </span></p>
<p><span style="color: #000000;"> </span></p>
<p><span style="color: #000000;"> </span></p>
<p><span style="color: #000000;">If you encounter any issues (or if you have feedback/ideas), <span style="color: #0000ee;"><a href="https://maxvanleeuwen.com/contact" target="_blank"><span style="color: #0000ee;">let me know (maxvanleeuwen.com/contact)</span></a></span>!</span></p>
<p><span style="color: #000000;"> </span></p>
<p><span style="color: #000000;"> </span></p>
<p><span style="color: #000000;"> </span></p>
<p><span style="color: #000000;"> </span></p>
<p><span style="color: #000000;"><strong>Updates</strong></span></p>
<p><span style="color: #000000;"> </span></p>
<p><span style="color: #000000;">2.1</span></p>
<p style="margin-left: 30px;"><span style="color: #000000;">Added maximum of 5 node names in a path when media is reused (to prevent path name length overflow)</span></p>
<p style="margin-left: 30px;"><span style="color: #000000;"></span></p>
<p><span style="color: #000000;">2.0</span></p>
<p style="margin-left: 30px;"><span style="color: #000000;">Added -d flag in terminal to skip all disabled nodes, and (*) in UI list to show when nodes are disabled</span></p>
<p style="margin-left: 30px;"><span style="color: #000000;"></span></p>
<p><span style="color: #000000;">1.9</span></p>
<p style="margin-left: 30px;"><span style="color: #000000;">Fixed Nuke 13 (Python 3) compatibility</span></p>
<p style="margin-left: 30px;"><span style="color: #000000;"></span></p>
<p><span style="color: #000000;">1.8</span></p>
<p style="margin-left: 30px;"><span style="color: #000000;">Fixed Nuke 10.5 compatibility</span></p>
<p style="margin-left: 30px;"> </p>
<p><span style="color: #000000;">1.7</span></p>
<p style="margin-left: 30px;"><span style="color: #000000;">added support for media in Project Directory (root settings)</span><br /><span style="color: #000000;">added interactive license (nuke_i) support (for internal use, when scripts are relinked)</span><br /><span style="color: #000000;">added more information to log CSV</span><br /><span style="color: #000000;">fixed bug with font folder relinking</span><br /><span style="color: #000000;">fixed bug with 0b files freezing the copying process</span></p>
<p style="margin-left: 30px;"><span style="color: #000000;"> </span></p>
<p><span style="color: #000000;">1.6</span></p>
<p style="margin-left: 30px;"><span style="color: #000000;">relinking and relative relinking now only modifies knobs of media that is not user-ignored</span></p>
<p><span style="color: #000000;"> </span></p>
<p><span style="color: #000000;">1.5</span></p>
<p style="margin-left: 30px;"><span style="color: #000000;">fixed 'open folder' keyboard shortcut<br />code cleanup</span></p>
<p><span style="color: #000000;"> </span></p>
<p><span style="color: #000000;">1.4</span></p>
<p style="margin-left: 30px;"><span style="color: #000000;">added 'go to node' button<br />fixed error on empty project font path</span></p>
<p><span style="color: #000000;"> </span></p>
<p><span style="color: #000000;">1.3</span></p>
<p style="margin-left: 30px;"><span style="color: #000000;">fixed TCL support on font paths</span><br /><span style="color: #000000;">fixed issue with gizmo's and nuke script containing dots in their names</span><br /><span style="color: #000000;">UI labels now evaluate TCL as well</span><br /><span style="color: #000000;">log now stores used nuke version</span></p>
<p style="margin-left: 30px;"><span style="color: #000000;"> </span></p>
<p><span style="color: #000000;">1.2</span></p>
<p style="margin-left: 30px;"><span style="color: #000000;">File paths with TCL are supported<br />Folder browser will ask to create new folders if the selected path does not exist</span></p>
<p style="margin-left: 30px;"><span style="color: #000000;"> </span></p>
<p><span style="color: #000000;">1.1</span></p>
<p style="margin-left: 30px;"><span style="color: #000000;">Added PySide support (for Nuke 10.5 and older)</span><br /><span style="color: #000000;">Fixed Nuke closing on user interruption when 'exit on finish' is checked</span><br /><span style="color: #000000;">Fixed Nuke asking to save your Nuke script when 'exit on finish' is checked and script has not been saved</span></p>
<p style="margin-left: 30px;"><span style="color: #000000;"> </span></p>
<p><span style="color: #000000;">1.0</span></p>
<p style="margin-left: 30px;"><span style="color: #000000;">Initial release</span></p>
