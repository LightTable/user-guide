  # User Guide

_Note: This book is a work in progress and under heavy revision. Some content may be inaccurate, describe features no longer supported, or just plain wrong.

Here you will learn about the next generation code editor, Light Table. We will start with the basics and work our way to more advanced features and usages.

Let's get started!

## Install it from lighttable.com

http://www.lighttable.com/

## First Clojure Eval

Start LightTable, and open a new file by pressing `Ctrl-N`

Set syntax to Clojure (`Ctrl-Space` to open the command bar, then type/select 'Set editor syntax', type/select Clojure)

type (+ 1 2) `Ctrl-Enter` (`Cmd-Return` on Mac)

This will tell LightTable to install dependencies. Then eval that expression.

## Start an instarepl

Press `Ctrl-Space` to show the command bar, then
type "repl" in the command search box, select one item to run it:

  * Open a clojure instarepl
  * Make current editor an instarepl

instarepl currently only works for clojure files (.clj).

## User settings
You can access user settings by opening the Commands menu (Ctrl + Space) and typing `Settings: `. The following items should appear in the menu:

* Settings: User keymaps
* Settings: User behaviors
* Settings: Default keymaps
* Settings: Default behaviors
* Settings: Workspace behaviors

Additionally, you can access the same settings files directly by navigating to them in the following locations:

  * Mac: `~/Library/Application Support/LightTable/User/`
  * Linux: `~/.config/LightTable/User/`
  * Windows: `%APPDATALOCAL%/LightTable/User/`

## What next

You may want to

  * Check the shortcuts. Type Ctrl-Space shortcut Enter

    The basic shortcuts
    ~~~
      Ctrl-W       close tab
      Ctrl-O       open file
      Ctrl-N       new file
      Ctrl-F       find
      Ctrl-Space   show command bar
      Cmd-digit   switch to the Nth tab (Ctrl-digit on Linux)
    ~~~

  * To change various settings type Ctrl-Space `Settings: User behaviors`

    * Change a theme by editing the string theme name in (:lt.objs.style/set-theme "default") for example (:lt.objs.style/set-theme "ibdknox")
    * Try vim mode by adding (:lt.plugins.vim/activate-vim) (Note: The Vim plugin must be installed. See [this article](https://groups.google.com/forum/?fromgroups#!topic/light-table-discussion/TuJmH5Bpo2c) for details.)
    * Try emacs mode by adding (:lt.plugins.emacs/activate-emacs)
    * Contribute to this wiki page. Questions and updates welcome.

---

Below are links users both new and old will find useful. 

## New Users

If you are coming from Vim, see [For Vim Users](for-emac-users.md).

If you are coming from Emacs, see [For Emacs Users](for-vim-users.md).

## Tutorials & Screencasts

  * [Getting the feel for the Light Table's instarepl](http://blog.maio.cz/2013/08/getting-feel-for-light-tables-instarepl.html) by Marian Schubert
  * [Set of screencasts](http://www.youtube.com/user/Misophistful/videos) on Clojure programming in LightTable by James Trunk
  * [Set of screencasts](http://www.zubairquraishi.com/zubairquraishi/clojurescript--light-table.html) on ClojureScript programming in LightTable by Zubair Quraishi
  * [ClojureScript Analysis & Compilation](http://swannodette.github.io/2014/01/14/clojurescript-analysis--compilation/) in LightTable by David Nolen
  * Leveraging [custom expressions](https://groups.google.com/forum/#!topic/light-table-discussion/lyFzPGI2XMs) to write [Idiomatic Clojure](https://metaphysicaldeveloper.wordpress.com/2013/11/18/idiomatic-clojure-with-lighttable/) code by Daniel Ribeiro
  * [A Guide to Watches](https://medium.com/@zindlerb/guide-to-light-table-watches-fad560f698d3) by Brian Zindler
  * [How to programmatically manage a Light Table-aware nREPL server](http://manuelp.herokuapp.com/posts/14) by Manuel Paccagnella
