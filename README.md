*Baided on ["The Ultimate vimrc"](https://github.com/amix/vimrc)*

**The best way to use:**  
--------------------

Make an alias:  

```
alias edit="docker run -ti --rm -v $(pwd):/home/developer/workspace jare/vim-bundle"
```

Have fun!  

```
edit some.file
```

*[How to use docker without sudo](http://askubuntu.com/questions/477551/how-can-i-use-docker-without-sudo)*

**Plugins**  
------------
1. [Airline](https://github.com/bling/vim-airline)     
2. [Tagbar](https://github.com/majutsushi/tagbar)    
3. [EasyGrep](https://github.com/vim-scripts/EasyGrep)      
4. [Bufexplorer](https://github.com/jlanzarotta/bufexplorer)      
5. [CtrlP](https://github.com/kien/ctrlp.vim)     
6. [The NERD Tree](https://github.com/scrooloose/nerdtree)      
7. [NERDTree tabs](https://github.com/jistr/vim-nerdtree-tabs)       
8. [Syntastic](https://github.com/scrooloose/syntastic)
9. [YouCompleteMe](https://github.com/Valloric/YouCompleteMe)
10. [Vim-Scala](https://github.com/derekwyatt/vim-scala)   
11. [Solarized Colorscheme for Vim](https://github.com/altercation/vim-colors-solarized)       
12. [Taglist](https://github.com/vim-scripts/taglist.vim)      
13. [Commentary](https://github.com/tpope/vim-commentary)      
14. [Vim-expand-region](https://github.com/terryma/vim-expand-region)     
15. [Fugitive](https://github.com/tpope/vim-fugitive)      
16. [Gitgutter](https://github.com/airblade/vim-gitgutter)      
17. [Vim-go](https://github.com/fatih/vim-go)    
18. [Vim-markdown](https://github.com/plasticboy/vim-markdown)    
19. [Vim-indent-object](https://github.com/michaeljsmith/vim-indent-object)       
20. [Vim-multiple-cursor](https://github.com/terryma/vim-multiple-cursors)       
21. [Vim-repeat](https://github.com/tpope/vim-repeat)      
22. [Vim-surround](https://github.com/tpope/vim-surround)      
23. [The Most Recently Used (MRU](https://github.com/vim-scripts/mru.vim)      
24. [YankRing](https://github.com/vim-scripts/YankRing.vim)      
25. [Vim-HAML](https://github.com/tpope/vim-haml)       
26. [SnipMate](https://github.com/garbas/vim-snipmate)       
27. [snipMate & UltiSnip Snippets](https://github.com/honza/vim-snippets)      
28. [vim-addon-mw-utils](https://github.com/marcweber/vim-addon-mw-utils)     
29. [tlib](https://github.com/tomtom/tlib_vim)      

**[.vimrc](https://github.com/JAremko/alpine-vim/blob/master/.vimrc)** 
------------------------------------------------------------------------
    

If you don't need YouCompleteMe, Python and "big" features use `jare/vim-bundle:no-ycm` instead. It's one-third the size of this image.

Keep in mind:
------------

* To see fancy arrows you need [Powerline Fonts](http://askubuntu.com/questions/283908/how-can-i-install-and-use-powerline-plugin) on your machine. But if you don't need them remove `let g:airline_powerline_fonts = 1` from the
[.vimrc](https://github.com/JAremko/alpine-vim/blob/master/.vimrc)   

![With and without](http://i.imgur.com/yRWBFgn.jpg)   

* For Golang support you need to symlink goroot and gopath in to the root of the workspace. Or mount them with `-v <local_goroot>:<container_groot> -v <local_gopath>:<container_gopath>` and set environment variables `-e GOROOT=<container_groot> -e GOPATH=<container_gopath>`

* If you have problem with colors - switch your terminal to the `solarized dark` theme and make sure that it uses default palette and  256 colors.

* If your terminal doesn't support 256 colors change `TERM` environment variable. For example `docker run .. -e TERM=xterm ...`

**I managed to strip down the image from around 300MB to almost 100MB. Hopefully without breaking things. Leave a comment if you noticed a bug.**
