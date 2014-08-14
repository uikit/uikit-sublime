uikit-sublime
=============

### UIkit Sublime Plugin

Auto-complete plugin for UIKit classes and data attributes. 

### UIkit

UIkit is a lightweight and modular front-end framework for developing fast and powerful web interfaces.

* Homepage: [http://www.getuikit.com](http://www.getuikit.com)
* Twitter: [@getuikit](http://twitter.com/getuikit)

### Installation

The plugin can be installed through Sublime Text's Package Control. Just search for `uikit`.

Alternatively, you can clone this repository to the Packages directory of your Sublime installation. In Mac OS, this looks as follows: 

```bash
cd ~/Library/Application Support/Sublime Text 3/Packages/
git clone git@github.com:uikit/uikit-sublime.git
```

### Usage

- **Class name autocompletion**: When inside double quotes of a class attribute (`class="<here>"`), suggestions will appear for all `uk-` classes.
- **Data attributes autocompletion**: 
- **Markup snippets**: Anywhere in your document, type `uikit` to see all available snippets. Scroll through them with your cursors and hit the return key to apply a snippet or the ESC key to cancel.

Note: In order for the suggestions to appear, your document needs to have the syntax set to `HTML` (or any child syntax like `HTML (PHP)`). You can set the syntax from the menu *View > Syntax* or via the Command Palette.

### Developer

*The following information explains how this plugin is maintained. Users do not need to care about those steps.*

To keep this plugin in sync with UIkit, class names, data attributes and markup snippets are extracted from the UIkit code base using a Grunt task provided by UIkit itself.

```bash
cd path/to/uikit
grunt
grunt sublime 
```

This will generate a file `/dist/uikit_completions.py`. Replace the according parts of the plugin's python file with the generated python snippet.

Snippets are generated in the `/dist/snippets` directory. Copy all files to the plugins `/snippets` directory.

To make a new version of the plugin available via package control, a new version tag needs to be created.

## Copyright and license

Copyright 2014 [YOOtheme](http://www.yootheme.com) GmbH under the [MIT license](LICENSE.md).
