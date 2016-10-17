# Common Terms

### Eval

Eval, short for evaluation, is the act of executing code inside of a running process. This means you modify the code that is currently executing without having to restart whatever you're doing. This also gives you the ability to evaluate an expression and see the result of it in real time based on the actual state of your application.

### REPL

REPL stands for Read-Eval-Print-Loop, wikipedia has a [decent description](http://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop) of it. Basically the gist of it is that it's a little prompt that you can type code in and when submit that code, it evaluates it, prints the result, and lets you do it again. REPLs make for a great way to try things out. Inside of Light Table we remove the need for a special prompt, and instead you can eval directly in a file to see what something does/evaluates to.

### Instarepl

The Instarepl is a term we coined for an editor that evaluates as you type and shows you not only the result of an expression, but also how all the variables in your code are filled in to get that result. This allows you to see data flow through your program and amounts to a sort of real-time debugging. Results are blue and variable values are shown in purple to the right of their use in the code.

### Client

A client is a process that is connected to Light Table that we can send messages to. Usually these messages revolve around being able to eval code in that process, but they don't necessarily have to. For example, in order to eval Python code, we run a Python process that talks to Light Table over TCP and acts a client for us to send code to.

### Workspace

In the Light Table world, a workspace is the group of files and folders that you're interested in. Workspaces are saved and created automatically, and you can access the last 20 workspaces you've used by clicking the "recent" button at the top of the workspace tree.

### BOT Architecture

### Behavior

Light Table's functionality is defined by functions that respond to a set of triggers. This combination of a function and the triggers that it reacts to is called a behavior. Behaviors serve as the way to define what Light Table does in any number of situations and operate as a very powerful settings system. Behaviors are not applied directly to objects, but rather to "tags". These tags allow you to specify behavior for kinds of things at different levels of specificity. For example, you can apply behavior to all editors by adding a behavior to the `:editor` tag or to only clojure editors by adding it to the `:editor.clojure` tag. To modify behaviors, execute the `Settings: User behaviors` command.

### Object

### Tag

### Command

### Plugins

### Theme

### Keybindings
