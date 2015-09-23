# Credits

1. The `misaka_md2html.py` converter was developed by Jason6Anderson, posted on Vimwiki [issue 384](http://code.google.com/p/vimwiki/issues/detail?id=384)
1. Code highlighting support is provided by [Pygments][]
1. Equation rendering support is provided by [MathJax][] 
1. Stylesheet colors are based on [Solarized][]
1. And all editing was done in [Vimwiki][]

[Vimwiki]: http://code.google.com/p/vimwiki
[Pygments]: http://pygments.org/
[MathJax]: http://www.mathjax.org/
[Solarized]: http://ethanschoonover.com/solarized

# Installation

## Requirements

* python3
* misaka
* Jinja2
* houdini.py
* Pygments

*Note: misaka, Jinja2, houdini.py and Pygments can be installed using `pip install <package>` or similar.*

To install all requirements on Ubuntu 15.04 use:

```bash
sudo apt-get install python3 python3-pip python3-misaka python3-jinja2 python3-pygments
sudo pip3 install houdini.py
```

## Installation

To install the bootstrapper just clone the repository into a local directory
```bash
git clone <repo_url> <local_dir>
```

## Configuration

In your .vimrc use a vimwiki configuration similar to:

```vim
" Configuration for Misaka Bootstrap
let g:vimwiki_list = [{
  \ 'syntax'           : 'markdown',
  \ 'ext'              : '.md',
  \ 'template_default': 'default',
  \ 'template_ext': '.html',
  \ 'index'            : 'README',
  \ 'path_html'        : '<local_dir>/Html/',
  \ 'nested_syntaxes'  : {'ruby': 'ruby', 'python': 'python', 'c++': 'cpp', 'sh': 'sh', 'bash': 'sh', 'r': 'R', 'R': 'R', 'vim': 'vim', 'objc': 'objc', 'xml': 'html', 'html': 'html', 'jscript': 'javascript', 'javascript': 'javascript', 'css': 'css', 'ascript': 'applescript', 'mkd': 'markdown'},
  \ 'custom_wiki2html' : '<local_dir>/bin/misaka_md2html.py',
  \ 'list_margin'      : 1,
  \ 'force'            : 1,
  \ 'temp'             : 0,
  \ 'template_path': '~/vimwiki/templates', 
  \ }]
```

*Note: As of now, template_default, template_ext and template_path have no impact on how misaka_md2html.py behaves.*

The following rules apply:
1. *custom_wiki2html* should point to this file.
2. *path_html* must be set
3. *syntax* should equal 'markdown'
4. *css_name* should point to the css file you want to use. It has a default value of style.css so copying the provided style.css from autoload/vimwiki/ to your *path_html* should be sufficient to get started. 
