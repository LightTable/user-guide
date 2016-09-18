# For Vim Users

## Intro

Welcome Vimmers! Contributions to help fellow Vimmers are appreciated.

To use Light Table as a vim user, install [the Vim plugin](https://github.com/LightTable/Vim). The plugin uses [CodeMirror's implementation](https://github.com/codemirror/CodeMirror/blob/master/keymap/vim.js). For an overview of implemented vim features, see [their demo](http://codemirror.net/demo/vim.html). While CodeMirror's implementation does not have all of vim's features, it has a number of its core primitives. It also has the significant advantage of being a small, readable, well-tested implementation that has a low barrier of entry to new contributors.

## Ex Commands

The Vim plugin comes with a few ex commands. Some other ex-command equivalents (equivalent functionality but _not_ bound by default to the same keys):

* `:e[dit]` - Edit and autocomplete files by path using the [Claire plugin](https://github.com/joshuafcole/Claire)
* `:Q or gq` -  Paragraph reformatting using the [Reflow plugin](https://github.com/rschroll/reflow)
* `:map` - Find what is mapped to a given key combo with the [Describe Key plugin](https://github.com/Frozenlock/describe-key)
* `:b[uffer]` - [This is an implementation](https://github.com/cldwalker/ltfiles/blob/43b254e92a7574b8000b5e1f98b0dc44a2d37436/src/lt/plugins/user/tab.cljs#L46-L74) that opens buffers/tabs that have been previously opened using a dropdown/filter list. Feel free to add to your user.cljs until it's made into a proper plugin.

## Plugins

Some vim-related plugins to consider installing:

* [Claire](https://github.com/joshuafcole/Claire) - Provides :edit-like command
* [Vim-Focus](https://github.com/mmower/vim-focus) - Revert to normal mode when a tab loses focus.
* [Marks](https://github.com/bfabry/marks) - Provides at least two additional marks
* [Relative Line Numbers](https://github.com/davecoates/lt-relativelinenumbers) - Provides relative line numbering similar to an equivalent vim plugin
* [Reflow](https://github.com/rschroll/reflow) - Reformat paragraphs
