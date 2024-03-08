# Carl's dotfiles

Forked from: https://github.com/geerlingguy/dotfiles

My configuration. Minimalist, but helps save a few thousand keystrokes a day. I use macOS, so I can only guarantee they'll work on a Mac, but I use some of these dotfiles on various linux servers, and they seem to be pretty flexible.

You may also be interested in my [Mac Development Ansible Playbook](https://github.com/geerlingguy/mac-dev-playbook), which configures a Mac from scratch using Ansible, and incorporates the installation and updating of a set of dotfiles like this one.

## Installing on a new MacOS System

Your dotfiles can be replicated on a new system like:

```sh
$ git clone --bare <git-repo-url> $HOME/.dotfiles
$ alias dotfiles='/usr/bin/git --git-dir="$HOME/.dotfiles/" --work-tree="$HOME"'
$ dotfiles checkout
$ dotfiles config --local status.showUntrackedFiles no
```

## References

* [geerlingguy's dotfiles](https://github.com/geerlingguy/dotfiles)
* [Trevor's dotfiles](https://github.com/strangiato/dotfiles)
* [Tracking dotfiles directly with Git](https://wiki.archlinux.org/title/Dotfiles)

## License

MIT / BSD
