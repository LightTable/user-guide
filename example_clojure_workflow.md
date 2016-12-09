# Example Workflow - Clojure

While by no means the only possible workflow, below is a sample of how you might make use of Light Table's features to enhance your Clojure experience.

### Open Project Folder

### Connect

The Connection panel gives several different options for connections, but we will only be interested in one specific option. Use the Command Panel and search for "Connect: Add Connection". From the resulting Connection panel, select the "Clojure" option and connect to the `project.clj` file.

### Do Some Work

### Look up Documentation

### Jump to Definition

### Evaluate

To evaluate the form at the cursor position use `Ctrl-Enter` or, in the command pane, use `Eval: Eval a form in editor`. This will evaluate the outer-most form the cursor is touching, such as a function definition.

To evaluate the entire file, use `Ctrl-Shift-Enter` or, in the command pane, use `Eval: Eval editor contents`. As all forms in the file will be evaluated, this can be useful to quickly propagate any changes made to commonly used functions near the top of the namespace. 

### Watch
