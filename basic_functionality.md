# Basic Functionality

All you could want to know about: files, navigation, connections, commands, and searching documentation

### Opening and creating new files

To create a new file, use the `New file` menu item in the `File` menu or press cmd/Ctrl-N
To open a file, use the `Open file` menu item in the `File` menu or press cmd/Ctrl-Shift-O

### Workspace tree (or how to open files)

Opening each file individually through the native open dialogs isn't very efficient. The `workspace` tree allows you to instead add files and folders into a file explorer that you can then use to open/rename/delete/etc the files you're interested in. To open the workspace tree, click the `Workspace` item in the view menu. You can then add files or folders to the workspace using the buttons at the top.

![workspace tab](/images/start/wsadd.png)

Once you have items in your workspace, you can use the right-click context menu to do the standard file actions you would expect (rename, delete, new file, etc) as well as remove them from the workspace if you no longer want them there.

![workspace tab menu](/images/start/wsmenu.png)

When you open a new window of Light Table, you'll be given a new blank workspace - if you want to switch to a recently used one, click the recent button and select one of your old workspaces from the list.

![workspace tab recent](/images/start/wsrecent.png)

### Navigation pane

Once you have files and folders in your workspace, the `navigate` pane provides the quickest way to open a file by name. Opening it is bound to Cmd/Ctrl+O by default.

![navigate tab](/images/start/navi.png)

The navigate tab is a "filter list" where typing in the top input will filter the results down to those that match what you've typed. All filter lists inside of Light Table use a form of sequential partial substring matching, which is a fancy way of saying that you can type letters and as long as those letters appear in order in one of the list items it will be considered a match. This allows you to type "mcf" to match "my-cool-file" and so on, dramatically increasing efficiency of filter operations.

![navigate tab filtered](/images/start/navi2.png)

### Connections pane

The `connect` pane shows you a list of currently connected "clients" that can be used for doing language operations like eval. To open it, use the `Connections` item in the `View` menu or the `Connect: Show connect bar` command.

![connect tab](/images/start/con.png)

This list allows you to disconnect a client, which often kills the process it is associated to, or unset a client associated to an editor. You might do the latter when you want to change the context in which you eval something, for example. Clients associated with the currently active editor will appear highlighted.

![connect tab](/images/start/consel.png)

The `connect` tab also allows you to explicitly add a connection to a client, by presenting a list of all the available client type for you to select one from.

![connect tab](/images/start/conadd.png)

### Command pane

The `command` pane is your one stop shop to figure out if Light Table can do something. It is a filter list like navigate that presents a list of all the visible commands in Light Table. Want to open a file or change some setting? Type "open file" or "setting" to filter down to what you want to do and then press enter to do it. Opening the `command` pane is bound to Ctrl+Space by default, but you can use the `Commands` item in the `View` menu as well.

![command tab](/images/start/cmd.png)

The command pane will also show keybindings for the given command underneath the command's name.

![command tab](/images/start/cmdopts.png)

### Inline Documentation

> Note: This functionality is dependent on the language plugin associated with the file.

With your cursor on a function, it is possible to see the documentation at a glance. Simply press Ctrl-D and any documentation found will be displayed in the editor. To hide the documentation, either press Ctrl-D again, or right click the box and select clear.

### Language Documentation Pane

The documentation 
