# bash-profile-stuff

1. Enter terminal
2. Execute: `cd ~; nano .bash_profile`
3. Put in this code:
```
parse_git_branch() {
     git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/ (\1)/'
}
export PS1="\u@\h \[\033[32m\]\w\[\033[33m\]\$(parse_git_branch)\[\033[00m\] $ "
alias bp="cd ~; nano .bash_profile"
alias rbp="source ~/.bash_profile"
alias ls="ls -CF"
alias gs="git status"
```
4. Press 'Ctrl+o' to 'Writeout'.
5. Press 'Ctrl+x' to 'Exit'.
6. Close Terminal, reopen to refresh.
7. Change directory to a git repo, and see __great things__!
