## File Structure

we need 2 files in the home directory

- The first one: ~/.vimrc
- The second one is: ~/.vimrc.plug

and we need a folder in the home directory: ~/.vim/

inside this directory we need 4 directories: autoload, backup, colors, plugged

---

> we can set alot of configuration in the .vimrc file

this is a good place to start [Vimrc Configuration Guide](https://www.freecodecamp.org/news/vimrc-configuration-guide-customize-your-vim-editor/)

---

> after setting the configs now we want to add some plugins

> now we gonna use the .vimrc.plug file

we must link our .vimrc and .vimrc.plug files

so we gonna add these 3 lines of vim scripting to the .vimrc file

```vim
if filereadable(expand("~/.vimrc.plug"))
    source ~/.vimrc.plug
endif
```

in the .vimrc.plug file we need to write the following

```vim
call plug#begin('~/.vim/plugged')
    " you can put your plugins here 
    " example:
    Plug 'tpope/vim-fugitive'
call plug#end()
```

inside the call begin and call end we'll put our plugins

[15 Essential Plugins for VIM](https://www.tabnine.com/blog/top-vim-plugins/)

after adding plugins we should install them by opening vim and then running:

```bash
:PlugInstall
```

!!! install the plugins after creating the directories (.vim) (plugged)