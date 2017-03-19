# Basic Functionality

All you could want to know about: files, navigation, connections, commands, and searching. The division between basic functionality and advanced functionality is somewhat arbitrary, so be sure to check out both sections.

### Opening and creating new files

To create a new file, use the `New file` menu item in the `File` menu or press `cmd/Ctrl-N`.

To open a file, use the `Open file` menu item in the `File` menu or press `cmd/Ctrl-Shift-O`.

### Workspace tree \(or how to open files\)

Opening each file individually through the native open dialogs isn't very efficient. The `workspace` tree allows you to instead add files and folders into a file explorer that you can then use to open/rename/delete/etc the files you're interested in. To open the workspace tree, click the `Workspace` item in the view menu. You can then add files or folders to the workspace using the buttons at the top.

![workspace tab](/images/start/wsadd.png)

Once you have items in your workspace, you can use the right-click context menu to do the standard file actions you would expect \(e.g., rename, delete, new file\). From this context menu, it is also possible to remove files and folders from the workspace if you no longer want them.

![workspace tab menu](/images/start/wsmenu.png)

When you open a new window of Light Table, you will be given a new blank workspace - if you want to switch to a recently used one, click the recent button and select one of your old workspaces from the list.

![workspace tab recent](/images/start/wsrecent.png)

### Navigation pane

Once you have files and folders in your workspace, the `navigate` pane provides the quickest way to open a file by name. Opening it is bound to `Cmd/Ctrl+O` by default.

![navigate tab](/images/start/navi.png)

The navigate tab is a "filter list" where typing in the top input will filter the results down to those that match what you've typed. All filter lists inside Light Table use a form of sequential partial substring matching. This means you can type letters and as long as those letters appear in order in one of the list items it will be considered a match. For example, if you to type "mcf" then the partial substring matching will match "my-cool-file" and so on, which dramatically increases efficiency of filter operations.

![navigate tab filtered](/images/start/navi2.png)

### Command pane

The `command` pane is your one stop shop to figure out if Light Table can do something. It is a filter list like navigate that presents a list of all the visible commands in Light Table. Want to open a file or change some setting? Type "open file" or "setting" to filter down to what you want to do and then press enter to do it. Opening the `command` pane is bound to `Ctrl+Space` by default, but you can use the `Commands` item in the `View` menu as well.

![command tab](/images/start/cmd.png)

The command pane will show associated keybindings underneath a command, if there are any.

![command tab](/images/start/cmdopts.png)

### Connections pane

The `connect` pane shows you a list of currently connected "clients" that can be used for doing language operations like eval. To open it, use the `Connections` item in the `View` menu or the `Connect: Show connect bar` command.

![connect tab](/images/start/con.png)

This list allows you to disconnect a client, which often kills the process it is associated to, or unset a client associated to an editor. You might unset a client when you want to change the context in which you eval something. Clients associated with the currently active editor will appear highlighted.

![connect tab](/images/start/consel.png)

By presenting a list of all available client types, the `connect` tab allows you to explicitly add a connection to a client.

![connect tab](/images/start/conadd.png)

### Find

In an editor tab, you can find and replace some of the content via the command `Find: In current editor`. The default keybinding is `Ctrl-F`. This will open the find bar. In it you can enter, unsurprisingly, text to search for within the editor.

Find is smart-cased. This means if you type in all lower case then find assumes you mean to generically search for that run of characters. However, if you intentionally type an uppercase letter then find assumes you are looking for that specific string.

Enable regular expressions by wrapping your query in forward slashes \(`/`\). For instance, `/(item)/` will find all occurrences of lines containing 'item'. Capture groups can be used in the replace field. With the above example, you could append an 's' after 'item' with `$1s`.

### Search

Search allows you to search the entire workspace for text via the command `Searcher: Show`. The default keybinding is `Ctrl-Shift-F`. The command will open a new tab with an area to enter your query and one to display the found results.

Search has similarities with Find. Both are smart-cased, allow regular expressions for queries, and have capture groups available. See the Find section for information on those features.

`<workspace>` is the current Light Table workspace. Here is an [example](https://github.com/cldwalker/ltfiles/blob/d2459f26df08c10f4e74352e54dbf4919db5b7b0/src/lt/plugins/ltfiles/search.cljs#L12-L22) of providing your own aliases to use, in addition to `<workspace>`, via your User plugin.

> Note: Replacement is a destructive change in Search and there is no undoing! See [this issue](https://github.com/LightTable/LightTable/issues/1547) for status.

### Go to line

It is possible to quickly jump though a file to a specified line number by using the command `Editor: Go to line`. The default keybinding is`Ctrl-L`. This command will, as the name suggests, let you specify a line number to center the editor tab on. If you specify a line number larger than the file then the last line will be used.

### Fold Code

The command `Editor: Fold code at cursor`, default keybinding `Ctrl-=`, can be used to fold code. This folding currently does not work with Clojure and ClojureScript, however.

### Zoom

If the default size of Light Table is to large or small, it is possible to adjust via the commands \(and default keybindings\):

* `Window: Zoom in` \(`Ctrl-+`\)
* `Window: Zoom out` \(`Ctrl--`\)
* `Window: Zoom reset` \(`Ctrl-0`\)

### Cycle through tabs

`Ctrl-Tab` and `Ctrl-Shift-Tab` will, respectively, allow you to cycle forwards and backwards through open tabs.



