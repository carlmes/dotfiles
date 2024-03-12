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

## MacBook Configuration

Script to examine all defaults:

```sh
▶ cat defaultdiff.sh                             
#!/bin/bash

BASE=/tmp/defaults.a
DIFF=/tmp/defaults.b

defaults read > $BASE
while sleep 1; do
    defaults read > $DIFF
    diff -u $BASE $DIFF
    mv $DIFF $BASE
done
```

## Homebrew Stuff

Currently installed brew components:

```sh
▶ brew leaves -r
ant
argocd
atomicparsley
certbot
cmark
coreutils
curl
excel-compare
ffmpeg
git
gobject-introspection
gradle
helm
hyperkit
iperf3
jenv
jmeter
jq
kubernetes-cli
kustomize
libdvdcss
libomp
libressl
maven
mkvtoolnix
mosh
node
openconnect
openjdk@11
quarkusio/tap/quarkus
skopeo
source-to-image
tektoncd-cli
vpn-slice
wget
yamllint
yt-dlp
```

