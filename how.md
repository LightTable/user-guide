# How Do I...

### Evaluate code inline?

Within an editor, eval a single "block" (or form if you're used to LISP) is bound to Cmd/Ctrl+Enter by default and evaling an entire file is bound to Cmd/Ctrl+Shift+Enter. Not all file types know how to eval, to find out what kinds of clients are available for evaluation, open the `connect` tab and press the "Add Connection" button. This will give you a list of all the clients Light Table knows how to start.

### Split windows?

You can create a new tabset by either right clicking in the tab area and selecting `New tabset` or by using the `Tabs: Add a tabset` command in the command bar. To close a tabset you can either use the `Tabs: Remove active tabset` command or resize it such that it has 0 width.

As of v0.8.1, it is not possible to split horizontally, but there is an issue open to address this.

### Open a new window?

By default, Cmd/Ctrl+Shift+N is bound to the command `Window: Open new window`, which you can also just execute from the command tab.

### Open a browser tab for live modification?

You can open a browser tab by either using the `Browser: add browser tab` command or by choosing the browser client type form the "Add Connection" menu in the `connect` tab. Once open, it is now available as an evaluation client and Cmd/Ctrl+R is bound to refreshing it.

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
