# Configuration

### Change settings (e.g., fonts, line numbers)?

Settings are represented as behaviors in Light Table. To modify your user behaviors, execute the `Settings: User behaviors` command and modify the file that is opened. 

For example, to turn on the line number gutter, find the `:editor` tag and in the square brackets type "number". Then select `Editor: Show line numbers` behavior. This workflow lets you search for the behavior you want via the auto-complete and then the helper will show you what parameters are needed (if any) for that behavior.

All settings in Light Table work this way and behaviors give you the ability to fundamentally change the functionality of Light Table.

### Configure behaviors

To add a behavior to your `user.behaviors` file, add a vector in the format `[:TAG :COMMAND :ARG1 :ARG2 ...]` (e.g., `[:editor :lt.objs.editor/no-wrap]`). If a command takes arguments append them after the command (e.g., `[:app :lt.objs.app/set-default-zoom-level 0.8]`). Behaviors that are set by default can be disabled/subtracted/removed by prefixing the command with `-`  (e.g., `[:editor :-lt.objs.editor/no-wrap]`).

### Change theme

To set the editor theme execute the `Settings: User behaviors` command, type `[:editor :lt.objs.style/set-theme "" ]` and in between quotation marks type a theme name (auto-complete will help you here). To see what different themes look like, try [the CodeMirror theme demo](http://codemirror.com/demo/theme.html). Note that some themes listed there may not be available because LightTable may not be on the same CodeMirror version as the demo. To try third party themes, like [these ones](https://github.com/FarhadG/code-mirror-themes), download them and add an entry for it in user.behaviors file:  `[:app :lt.objs.style/provide-theme "theme-name" "/full/path/to/theme/css"]`. Once a theme is provided you can set it with the aforementioned `set-theme`.

### Change keybindings?

Keybindings are defined in .keymap files in Light Table. To open the user keymap, execute the `Settings: User keymap` command. To see the default keybindings you can execute the `Settings: Default keymap` command. Keys are bound based on context (tag), which allows you to create contextual command schemes.

### Configure keybindings

To add a keybinding to your `user.keymap` file, add a vector in the format `[:TAG "KEYBINDING" :COMMAND]` e.g. `[:editor "alt-w" :editor.watch.watch-selection]`. If a command takes arguments wrap the command and its arguments in a parentheses e.g. `[:editor "alt-(" (:paredit.select.parent "(")]`. If you want to bind multiple commands to the same keybinding, use a simple vector for the whole binding-command e.g. `[:editor  "alt-(" (:paredit.select.parent "(") :smart-indent-selection]`. Keybindings that are set by default can be subtracted/removed by prefixing the key with '-'  e.g. `[:app "-ctrl-shift-d" :docs.search.show]`.

### Exclude files from the workspace?

Open your user behaviors and in the `:app` tag start typing "ignore". Select the `Files: Set ignore pattern` behavior.

### Change the location of the lighttable directory?

You can use the environment variable `LTHOME` to tell the command line scripts where to find LT.

### Find out what version of Light Table I'm using?

Use the `App: Light Table version` command from the command tab.
