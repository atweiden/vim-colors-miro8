Perfect for 8-color terminals
=============================

This is Jason W. Ryan's [miro8](https://bitbucket.org/jasonwryan/shiv/src/477cdc351c8609f5d40d1577f19ec250351140bc/.vim/colors/miro8.vim?at=default)
color scheme for Vim, uploaded to GitHub in a Vundle-compatible way.

See [this blog post](http://jasonwryan.com/blog/2011/04/06/vim-colours-in-the-console/)
for more info.


Screenshot
----------

![miro8.vim](https://i.imgur.com/0e0BcJd.png)


Usage
-----

```vim
set background=dark
if $TERM == "rxvt-unicode-256color" || $TERM == "xterm-256color" || $TERM == "screen-256color" || $COLORTERM == "gnome-terminal"
  set t_Co=256
  let g:jellyx_show_whitespace = 1
  colorscheme jellyx
elseif $TERM == "linux"
  colorscheme miro8
endif
```

```sh
# Linux console colors (jwr dark)
if [ "$TERM" = "linux" ]; then
   echo -en "\e]P0000000" #black
   echo -en "\e]P83d3d3d" #darkgrey
   echo -en "\e]P18c4665" #darkred
   echo -en "\e]P9bf4d80" #red
   echo -en "\e]P2287373" #darkgreen
   echo -en "\e]PA53a6a6" #green
   echo -en "\e]P37c7c99" #brown
   echo -en "\e]PB9e9ecb" #yellow
   echo -en "\e]P4395573" #darkblue
   echo -en "\e]PC477ab3" #blue
   echo -en "\e]P55e468c" #darkmagenta
   echo -en "\e]PD7e62b3" #magenta
   echo -en "\e]P631658c" #darkcyan
   echo -en "\e]PE6096bf" #cyan
   echo -en "\e]P7899ca1" #lightgrey
   echo -en "\e]PFc0c0c0" #white
   clear # bring us back to default input colours
fi
```
