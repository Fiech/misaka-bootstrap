
%toc

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
git clone <repo_url> <local_dir>`
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

# Misaka Bootstrap

## $ `git clone git://github.com/tub78/misaka-bootstrap.git Wiki`

```bash
Cloning into 'Wiki'...
remote: Counting objects: 24, done.
remote: Compressing objects: 100% (14/14), done.
remote: Total 24 (delta 6), reused 24 (delta 6)
Receiving objects: 100% (24/24), 10.79 KiB, done.
Resolving deltas: 100% (6/6), done.
```


## $ `cd Wiki/; ls -l`

```bash
  drwxr-xr-x   136 Mar 16 19:03 Html
  drwxr-xr-x   170 Mar  3 23:37 Media
  -rw-r--r--  1164 Mar 17 00:06 README.md
  -rw-r--r--  3526 Mar 16 21:32 pygments.css
  -rw-r--r--  7290 Mar  3 23:29 style.css
  -rw-r--r--  4754 Mar 16 23:03 tags
  -rw-r--r--  1028 Mar 16 23:21 vimwiki.vimrc
```


## $ `cat README.md`

```markdown
  %toc
  # Misaka Bootstrap
 
  ...


```


## $ `ls -l Media/`

```bash
  total 24
  -rw-r--r--  807 Mar  3 22:39 spacer1x1.gif
  -rw-r--r--  303 Mar  3 22:48 spacer200.gif
  -rw-r--r--  630 Mar  3 22:48 spacer400.gif
```

## $ `ls -l Html/`

```bash
  total 16
  lrwxr-xr-x   8 Mar 16 19:03 Media -> ../Media
  lrwxr-xr-x  12 Mar 16 19:03 style.css -> ../style.css
```


## $ `ls -l bin/`

```bash
  total 32
  -rwxr-xr-x  13376 Mar 16 23:46 misaka_md2html.py
```



