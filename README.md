# How to ...

## Comment installer node.js sous Ubuntu ?
sudo apt-get update

sudo apt-get install nodejs npm

## Display the current git branch in the prompt ?
1. Download the Git's source code [here](https://github.com/git/git).
2. Copy the **contrib/completion/git-prompt.sh** file to your home directory.
3. Edit the .bashrc file like this :
  ```
. ~/git-prompt.sh
if [ "$color_prompt" = yes ]; then
    PS1='${debian_chroot:+($debian_chroot)}\[\033[01;32m\]\u@\h\[\033[00m\]:\[\033[01;34m\]\w\[\033[00m\] \e[32m$(__git_ps1 "(%s)") \e[0m\$'
else
    PS1='${debian_chroot:+($debian_chroot)}\u@\h:\w $(__git_ps1 "(%s)") \$'
fi
  ```
4. (Optional) Change the color: see this [link](https://misc.flogisoft.com/bash/tip_colors_and_formatting)
5. To apply modifications run:

source .bashrc

Learn [here](https://git-scm.com/book/en/v2/Appendix-A%3A-Git-in-Other-Environments-Git-in-Bash)
