To generate your Linux Bash Nice Prompt: https://scriptim.github.io/bash-prompt-generator/

How to install
--
1. Add to `~/.bashrc` 
```
export PS1=...
```
2. Source `~/.bashrc` or restart the terminal
```BASH
source ~/.bashrc
```

Example:
--
My favorite:
```BASH
export PS1='\n\n\[\e[0;96m\]------------------------------------------------------------\n\[\e[0m\]\u\[\e[0m\]@\[\e[0m\]\h\[\e[0m\]:\[\e[0;38;5;226m\]\w\n \[\e[0m\]├ \[\e[0m\]branch: \[\e[0;1;38;5;202m\]$(git branch 2>/dev/null | grep '"'"'^*'"'"' | colrm 1 2)\n \[\e[0m\]└ \[\e[0m\]\A \[\e[0m\]=\[\e[0m\]>\[\e[0;38;5;40m\]$ \[\e[0m\]'
```
![Screenshot](https://github.com/amenophis1er/notebook/blob/main/Screenshot%20from%202022-07-08%2016-49-02.png?raw=true "Screenshot")
