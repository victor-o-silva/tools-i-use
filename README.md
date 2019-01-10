
## Local Tools

- [Bat](https://github.com/sharkdp/bat)
- [Commitizen](https://github.com/commitizen/cz-cli)
- [Docker](https://www.docker.com/get-docker) & [Docker Compose](https://docs.docker.com/compose/)
- [ffmpeg](https://www.ffmpeg.org/download.html)
- [Fzf](https://github.com/junegunn/fzf)
- [Git Flow Completion](https://github.com/bobthecow/git-flow-completion)
- [Git Flow](https://github.com/nvie/gitflow)
- [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
- [Gitmoji CLI](https://github.com/carloscuesta/gitmoji-cli)
- [Google Chrome](https://www.google.com.br/chrome/)
- [htop](https://hisham.hm/htop/)
- [Meld](http://meldmerge.org/)
- [NodeJS](https://nodejs.org/en/download/package-manager/#debian-and-ubuntu-based-linux-distributions)
- [Oh My ZSH](https://github.com/robbyrussell/oh-my-zsh)
- [Pipenv](https://github.com/pypa/pipenv/)
- [Postman](https://www.getpostman.com/apps)
- [PyCharm](https://www.jetbrains.com/pycharm/)
- [PyEnv](https://github.com/pyenv/pyenv)
- [Redshift](https://github.com/jonls/redshift)
- [Slack](https://slack.com/downloads/linux)
- [Terminology](https://www.enlightenment.org/about-terminology)
- [Tig](https://github.com/jonas/tig)
- [Trash](https://github.com/sindresorhus/trash#cli)
- [Visual Studio Code](https://code.visualstudio.com/download)
- [Z](https://github.com/rupa/z/blob/master/z.sh)

## External services

- [BitBucket](https://bitbucket.org)
- [FunRetro](https://funretro.github.io/distributed/)
- [Git Graph JS](http://gitgraphjs.com/)
- [GitHub](https://github.com/)
- [Learn Git Branching](https://learngitbranching.js.org/?NODEMO)
- [ngrok](https://ngrok.com/)

## Git config values

```bash
git config --global user.name "Victor Oliveira da Silva"
git config --global user.email "victor_o_silva@hotmail.com"
git config --global core.editor "gedit --wait --new-window"
git config --global push.default "current"
git config --global color.ui "auto"
git config --global core.pager 'less -RFX'
git config --global diff.algorithm histogram
git config --global alias.lg "log --pretty='%C(bold red)%h%C(reset) | %C(bold cyan)%d%C(reset) %s %C(bold green)(%cr)%C(reset) %C(bold yellow)[%an]%C(reset)'"
git config --global alias.lg1 "log --graph --decorate --format=format:'%C(bold blue)%h%C(reset) %C(bold yellow)%d%C(reset) %s %C(cyan)%an%C(reset) %C(bold green)(%ar)%C(reset)' --all"
git config --global alias.lg2 "log --graph --abbrev-commit --decorate --format=format:'%C(bold blue)%h%C(reset) - %C(bold green)(%ar)%C(reset) %C(white)%s%C(reset) %C(dim white)- %an%C(reset)%C(bold yellow)%d%C(reset)'"
git config --global alias.worddiff "diff --word-diff=color"
git config --global alias.amend "commit --amend -C HEAD"
git config --global alias.stash-unstaged "stash --keep-index --include-untracked"
git config --global alias.fix "commit --fixup"
git config --global rebase.autoSquash true
git config --global diff.tool meld
git config --global difftool.prompt false
```
## Visual Studio Code extensions

- [Bookmarks](https://marketplace.visualstudio.com/items?itemName=alefragnani.Bookmarks)
- [Bracket Pair Colorizer](https://marketplace.visualstudio.com/items?itemName=CoenraadS.bracket-pair-colorizer)
- [Docker](https://marketplace.visualstudio.com/items?itemName=PeterJausovec.vscode-docker)
- [Rainbow CSV](https://marketplace.visualstudio.com/items?itemName=mechatroner.rainbow-csv)

## PyCharm plugins

- [Presentation Assistant](https://plugins.jetbrains.com/plugin/7345-presentation-assistant)
- [Env File](https://plugins.jetbrains.com/plugin/7861-env-file)

# Aliases

```bash
alias gmjc="gitmoji --commit"
alias gmjl="gitmoji --list"
```

# Functions

```bash

# Example: ffmpeg_lower_volume 7years.mp4 3

ffmpeg_lower_volume(){
    inputfile=$1  # input file
    amount=$2  # amount of dBs to lower
    if [ -z "$amount" ]
    then
        $amount="5"
    fi

    ffmpeg -i $inputfile -vcodec copy -af "volume=-${amount}dB" lowered_${amount}dBs_${inputfile}
}

####################################################################
```
