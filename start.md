# Inline Evaluation

### Clojure

If you have some Clojure code in a file already, you can get going with inline eval by:

1. Create a new file and save it with a `.clj` extension or open a `.clj` file
2. Press Cmd/Ctrl+Enter to evaluate a form
3. Wait for the client to connect (this can take a bit the first time)
4. Once connected you'll see your result.

### Javascript/HTML/CSS

In order to evaluate Javascript, HTML, or CSS, we need a browser to see the result in. To open a browser tab in Light Table:

1. In the view menu click the `commands` item
2. Type "brows" and press enter when the `Browser: add browser tab` command is highlighted
3. Use the URL bar at the bottom to open your page. This can be a `file://` URL to open an HTML file locally, or it can be something on the network.

Now that we have a place to send our code, let's open a `.js` file and eval something:

4. Create a new file and save it with a `.js` extension or open a `.js` file
5. Press Cmd/Ctrl+Enter while the cursor is over a top-level block of code. To eval an inner block, select and then eval it.
5. Select the webpage name from the available clients popup
6. You'll now see results inline!
7. Evaling from a `.css` file will inject the CSS into the page.
8. Evaling from an `.html` file will refresh the browser tab.

### Python

Getting started with Python is as simple as:

1. Create a new file with a `.py` extension or open a `.py` file
2. While over some code press Cmd/Ctrl+Enter
3. Allow Light Table a few seconds while it connects to a python process
4. You'll now see results inline!

If you want to use Light Table to do matplotlib/pylab graphs and such, you'll need to install the IPython kernel:

1. Follow these [instructions](http://ipython.org/ipython-doc/stable/install/install.html) to install IPython (note: it must IPython 1.0 or greater and you *must* install pyzmq as well in order for it to work with Light Table.)
2. Make sure IPython is on your path
3. Restart Light Table
4. Open a `.py` file by pressing Cmd/Ctrl+Shift+O
5. Over an expression that will return a graph, press Cmd/Ctrl+Enter
6. You'll see the graph embedded below your expression.
