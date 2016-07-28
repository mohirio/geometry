# geometry

geometry is a minimal zsh prompt theme.

![geometry](screenshots/geometry.png)

I started chopping away at [Avit](https://github.com/robbyrussell/oh-my-zsh/blob/master/themes/avit.zsh-theme) until I ended up with something minimal and inspired on [Pure](https://github.com/sindresorhus/pure).

What it does:

- display current git branch
- display colored time since last commit
- display state (clean/dirty) of the repo
- display arrows indicating if you need to pull, push or if you are mid-rebase
- set the terminal title to current command and directory
- display the number of git conflicts and total conflicts (optional)
- make you the coolest hacker in the whole Starbucks

Much like [Pure](https://github.com/sindresorhus/pure), geometry adds a different marker
if the last command result is different from `0`. It also sets the title to
`[command @] directory`. Check the title and marker here:

![title_marker](screenshots/title_marker.png)

## Installing

### antigen

Just add `antigen bundle frmendes/geometry` to your `.zshrc`.

### oh-my-zsh

Move `geometry.zsh` to `$HOME/.oh-my-zsh/custom/themes/geometry.zsh-theme` and
set `ZSH_THEME="geometry"` in your `.zshrc`.

### Dependencies

The symbol for rebasing comes from a [Powerline patched font](https://github.com/powerline/fonts). If you want to use it, you're going to need to install one from the font repo. The one used in the screenshots is Roboto Mono. You can also try to [patch it yourself](https://github.com/powerline/fontpatcher).

Alternatively, change the symbol by setting the `GIT_REBASE` variable, in
`geometry.zsh` to a different value.

### Options

You can optionally have the prompt display both the number of files with
conflicts as well as the total number of conflicts by setting the
`PROMPT_GEOMETRY_GIT_CONFLICTS` variable to true. This option uses `grep` and
`ag` with the latter being a [much faster alternative](http://geoff.greer.fm/ag/).
**If you don't have `ag` installed, this might slow your prompt down**.
