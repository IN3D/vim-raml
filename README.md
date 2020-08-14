# vim-raml
Vim syntax and language settings for RAML

## UPDATE

`vim-raml` is now a part of [Vim 8](https://github.com/vim/vim/blob/master/runtime/syntax/raml.vim) and [NeoVim](https://github.com/neovim/neovim/blob/master/runtime/syntax/raml.vim)! You likely don't need this unless you're using Vim 7.x.

## About

vim-raml is a superset of Vim's own syntax settings for YAML, as RAML itself is a superset of YAML. Obviously, filetype detection is provided for RAML files as well to make use of the expanded syntax, as well language formatting defaults.

The best way to showcase vim-raml is really just to show it.

This is a RAML file highlighted with Vim's default YAML highlighting, using the popular solarized-dark theme.

<img src="https://github.com/IN3D/vim-raml/blob/master/screenshots/yaml_highlighting.png" height="575">

And this is a RAML file highlighted with vim-raml:

<img src="https://github.com/IN3D/vim-raml/blob/master/screenshots/raml_highlighting.png" height="575">

You'll notice several changes:
 - The RAML version header, manditory in RAML now stands out brightly, rather than looking like a comment.
 - Parameter interpolation i.e. ```<<thing>>``` is highlighted inside of blocks and values.
 - Delimiters and blocks i.e. ```-, |, etc``` are consistently highlighted (flaky in YAML).
 - HTTP verbs, response codes, data types, and route definitions are all colored separately from regular keys to help immediately distingush different levels of the data structure.
   - HTTP verbs include all that are supported by RAML: get, post, put, delete, head, patch, and options
   - Response codes e.g. 200, 201, 404, 401, etc are colored like numbers (for obvious reasons)
   - Data types e.g. ```type: integer```. Supports all RAML datatypes. string, number, integer, date, boolean, and file.
   - Route definitions: these include ```/posts:``` or ```/{id}:```

## Installation

vim-raml doesn't have any strange or esoteric requirements.
Provided you're using Vundle, Pathogen or any of the other standard Vim plugin managers. You can install vim-raml exactly how you'd expect.

For completeness, to install via Vundle just add the following into your .vimrc with your other plugins
```viml
Plugin 'IN3D/vim-raml'
```
Then run:
```
:source %
:PluginInstall
```

Or for Pathogen:
```bash
cd ~/.vim/bundle
git clone https://github.com/IN3D/vim-raml.git
```
And Pathogen should pick it up the next time Vim is started.


## Questions, suggestions, and issues

If you have a question, suggestion, or have found an issue with vim-raml. The best way to bring it to my attention is to open an issue at [https://github.com/IN3D/vim-raml/issues](https://github.com/IN3D/vim-raml/issues).

## License

Copyright (c) Eric Hopkins. Distributed under the same terms as Vim itself.
See `:help license`.
