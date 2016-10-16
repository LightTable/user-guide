# Advanced Functionality

### Find

In an editor tab, you can find and replace some of the content via the command `Find: In current editor`. The default keybinding is `Ctrl-F`. This will open the find bar. In it you can enter, unsurpisingly, text to search for within the editor.

Regular expressions can be used by wrapping your query in forward slashes (`/`). For instance, `/.*item.*/` will find all occurrences of lines containing 'item'.

### Search

Search allows you to search the entire workspace for text via the command `Searcher: Show`. The default keybinding is `Ctrl-Shift-F`. The command will open a new tab 

`<workspace>` is the current Light Table workspace. Here is an [example](https://github.com/cldwalker/ltfiles/blob/d2459f26df08c10f4e74352e54dbf4919db5b7b0/src/lt/plugins/ltfiles/search.cljs#L12-L22) of providing your own aliases to use, in addition to `<workspace>`, via your User plugin. 

> Note: Currently, replacement is a destructive change and there is no undoing! See [this issue](https://github.com/LightTable/LightTable/issues/1547) for status.

### Jump to Definition

### Watches

### User Plugin

### Browser

### Autocomplete

Auto-complete is bound to the Tab key if there's some non-space character preceding the cursor, otherwise a tab is inserted.

### Console

When you print from a client, it will appear in the Console, which can be opened by clicking the blue number in the bottom right corner of the editor, from the `View` menu, or by using the `Console: Toggle console` command. STDOUT and STDERR are written to the console.

### Light Table Dev Console
