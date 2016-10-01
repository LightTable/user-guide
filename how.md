# How Do I...

### Change settings (fonts, line numbers...)?

Settings are represented as behaviors in Light Table. To modify your user behaviors, execute the `Settings: User behaviors` command and modify the file that is opened. For example, to turn on the line number gutter, find the `:editor` tag and in the square brackets type "number". Then select `Editor: Show line numbers` behavior. This workflow lets you search for the behavior you want via the auto-complete and then the helper will show you what parameters are needed (if any) for that behavior.

All settings in Light Table work this way and behaviors give you the ability to fundamentally change the functionality of Light Table.

### Configure behaviors

To add a behavior to your `user.behaviors` file, add a vector in the format `[:TAG :COMMAND :ARG1 :ARG2 ...]` e.g. `[:editor :lt.objs.editor/no-wrap]`. If a command takes arguments append them after the command e.g. `[:app :lt.objs.app/set-default-zoom-level 0.8]`. Behaviors that are set by default can be subtracted/removed by prefixing the command with '-'  e.g. `[:editor :-lt.objs.editor/no-wrap]`.

### Change theme

To set the editor theme execute the `Settings: User behaviors` command, type `[:editor :lt.objs.style/set-theme "" ]` and in between quotation marks type a theme name (auto-complete will help you here). To see what different themes look like, try [the CodeMirror theme demo](http://codemirror.com/demo/theme.html). Note that some themes listed there may not be available because LightTable may not be on the same CodeMirror version as the demo. To try third party themes, like [these ones](https://github.com/FarhadG/code-mirror-themes), download them and add an entry for it in user.behaviors file:  `[:app :lt.objs.style/provide-theme "theme-name" "/full/path/to/theme/css"]`. Once a theme is provided you can set it with the aforementioned `set-theme`.

### Evaluate code inline?

Within an editor, eval a single "block" (or form if you're used to LISP) is bound to Cmd/Ctrl+Enter by default and evaling an entire file is bound to Cmd/Ctrl+Shift+Enter. Not all file types know how to eval, to find out what kinds of clients are available for evaluation, open the `connect` tab and press the "Add Connection" button. This will give you a list of all the clients Light Table knows how to start.

### Change keybindings?

Keybindings are defined in .keymap files in Light Table. To open the user keymap, execute the `Settings: User keymap` command. To see the default keybindings you can execute the `Settings: Default keymap` command. Keys are bound based on context (tag), which allows you to create contextual command schemes.

### Configure keybindings

To add a keybinding to your `user.keymap` file, add a vector in the format `[:TAG "KEYBINDING" :COMMAND]` e.g. `[:editor "alt-w" :editor.watch.watch-selection]`. If a command takes arguments wrap the command and its arguments in a parentheses e.g. `[:editor "alt-(" (:paredit.select.parent "(")]`. If you want to bind multiple commands to the same keybinding, use a simple vector for the whole binding-command e.g. `[:editor  "alt-(" (:paredit.select.parent "(") :smart-indent-selection]`. Keybindings that are set by default can be subtracted/removed by prefixing the key with '-'  e.g. `[:app "-ctrl-shift-d" :docs.search.show]`.

### Split windows?

You can create a new tabset by either right clicking in the tab area and selecting `New tabset` or by using the `Tabs: Add a tabset` command in the command bar. To close a tabset you can either use the `Tabs: Remove active tabset` command or resize it such that it has 0 width.

### Open a new window?

By default, Cmd/Ctrl+Shift+N is bound to the command `Window: Open new window`, which you can also just execute from the command tab.

### Open a browser tab for live modification?

You can open a browser tab by either using the `Browser: add browser tab` command or by choosing the browser client type form the "Add Connection" menu in the `connect` tab. Once open, it is now available as an evaluation client and Cmd/Ctrl+R is bound to refreshing it.

### Bring up auto-completion?

Auto-complete is bound to the Tab key if there's some non-space character preceding the cursor, otherwise a tab is inserted.

### Eval an arbitraty unit of code?

If you have something selected Light Table will send the selection text for eval if you press Cmd/Ctrl+Enter.

### Eval Clojure?

To eval Clojure, open a .clj file and press Cmd/Ctrl+Enter. Light Table will find a leiningen project if there is one or it will use it's local REPL client to evaluate your code.

### Eval ClojureScript

You can eval ClojureScript [a couple of different
ways](https://github.com/LightTable/Clojure#clojurescript-eval). For your ClojureScript project,
building your cljs assets and then pressing Cmd/Ctrl+Enter is recommended. To read more about this
workflow, [see the Clojure plugin REAMDE](https://github.com/LightTable/Clojure#clojurescript-workflows).

### Eval Javascript in NodeJS?

To eval in a Node process:

1. Go to the `connect` tab
2. Click "Add Connection"
3. Select "NodeJS"
4. Choose a Javascript file to start the node server with.
5. Open a .js file
6. Press Cmd/Ctrl+Enter
7. Select your nodejs client from the popup

### Eval Python?

The easiest way is to simply open a Python file and press Cmd/Ctrl+Enter. This will cause Light Table to start a python client that it can then send code to.

### Use IPython for Python eval?

By default, if Light Table can find a recent IPython installed on your machine, it will use it to provide a much more robust python evaluation environment. If you don't have it installed, follow these [instructions](http://ipython.org/ipython-doc/stable/install/install.html) to do so (make sure you install pyzmq as well). With it you can use matplotlib and pylab inline. To see if Light Table is using IPython for Python eval, open the `connect` tab and look to see if your Python client has the type of `ipython`. Note that in order for Light Table to use IPython, pyzmq also needs to be installed.

### See the output from STDOUT and STDERR?

When you print from a client, it will appear in the Console, which can be opened by clicking the blue number in the bottom right corner of the editor, from the `View` menu, or by using the `Console: Toggle console` command.

### Use a different client once I've evaled something?

From the `connect` tab, find the client and make sure the editor you evaled in is active. The connected client(s) will appear highlighted. Click the "unset" button to force Light Table to re-evaluate what clients are available to eval in the editor.

### Close a client?

From the `connect` tab, find the client and click the "disconnect" button.

### Install a Plugin

Open the command pane and find the command "Plugins: Show Plugin Manager". In the manager, search for a plugin. Hover over a search result and click its install button.

### Toggle Vim keybindings?

Install the `Vim` plugin using the Plugin Manager and then run the command `App: Reload
behaviors`. If Emacs is already installed, disable it in users.behaviors with `[:editor
:-lt.plugins.emacs/activate-emacs]`.

### Toggle Emacs keybindings?

Install the `Emacs` plugin using the Plugin Manager and then run the command `App: Reload
behaviors`. If Vim is already installed, disable it in users.behaviors with `[:editor
:-lt.plugins.vim/activate-vim]`.

### Exclude files from the workspace?

Open your user behaviors and in the `:app` tag start typing "ignore". Select the `Files: Set ignore pattern` behavior.

### Change the location of the lighttable directory?

You can use the environment variable `LTHOME` to tell the command line scripts where to find LT.

### Find out what version of Light Table I'm using?

Use the `App: Light Table version` command from the command tab.

### Plugins directory

The plugins directory varies depending on the platform:

* Mac: `~/Library/Application\ Support/LightTable/plugins`
* Linux: `~/.config/LightTable/plugins`
* Windows: `%APPDATALOCAL%/LightTable/plugins`

Alternatively, you can see your location from running the command `App: Light Table version`.

### User plugin

Your complete configuration, including plugins you've installed, is stored in a User plugin. Since the User plugin is just a directory, you can share it by putting it under revision control e.g. git and uploading it to a service like Github. To explore it, add it to your workspace with the command `Settings: Add User plugin to workspace`. Any custom keybindings and behaviors are added to `user.keymap` and `user.behaviors`. To write commands, behaviors and more, see `src/lt/plugins/user.cljs`. To open your `user.cljs` at anytime use the command `Settings: User script`. Inside the default `user.cljs` is an example command and behavior. If you're upgrading Light Table, you will need to add two behaviors to `user.behaviors` in order for the examples to work:

```clojure
[:app :lt.objs.plugins/load-js "user_compiled.js"]
[:user.hello :lt.plugins.user/on-close-destroy]
```

Run the command `User: Say Hello` to see your own command!


### Write a plugin

Plugins are a great way to share your Light Table enhancement with the community. The recommended way to generate one is with `lein new lt-plugin my-plugin --to-dir MyPlugin`. Make sure to run that it in [your plugin directory](#plugins-directory). Add the generated plugin to your workspace and open the generated `.cljs` file. With your [LT UI connection set up](#eval-clojurescript), eval the file with `Cmd-Shift Enter`. Now try your new plugin command `Say Hello`! For more about writing plugins, see [this wiki page](https://github.com/LightTable/LightTable/wiki/For-Developers#creating-a-plugin).

### Submit a plugin

If it's your first time submitting a plugin, make sure you have a valid `plugin.edn`. Fill out the keys as follows:

* `:name`*: Camel case is recommended
* `:version`*: Must be in format X.X.X e.g. 0.1.4
* `:source`*: Must be a github url e.g. https://github.com/USER/PLUGIN
* `:behaviors`*: Refers to the behaviors file which is needed to load the plugin and define any keybinding or behavior.
* `:desc`: Primary means users can find your plugin
* `:author`: Your name and another useful way to find your plugin

`*` Means the field is required.

When releasing a new version, you must update the `:version` key and push the new git tag e.g. `git tag X.X.X && git push --tags`. With your updated `plugin.edn`, add or update your plugin to the [plugin metadata repository](https://github.com/LightTable/plugin-metadata) using [these instructions](https://github.com/LightTable/plugin-metadata#submit-a-plugin).

### For more questions, see [the user contributed FAQ](https://github.com/LightTable/LightTable/wiki/FAQ).
