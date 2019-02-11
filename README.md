# cptMikky's various NixOS goodies

This repo contains random short-hands and wrappers which make using NixOS a bit more convenient.

## `pac` and `pcs`

Wrappers around `nixos-rebuild` and `nix-env` which make package search (`pcs`) and declarative installation (`pac`) easier.

For `pac` to work a `.nix` file dedicated to package and program installation should exist, preferably in `/etc/nixos` which is included from `/etc/nixos/configuration.nix`. `pac` lets you edit the file, checks for changes and allows you to apply such changes right away.

`pcs` wraps around `nix-env`. It caches the output of `nix-env -qaP` and allows you to quickly and easily search through this cache.

## aliases

Several convenience aliases are created:

```
alias nrs='sudo nixos-rebuild switch'
alias sss='sudo su -'
alias s='sudo systemctl --no-pager'
alias us='systemctl --no-pager --user'
alias grst='git fetch; git reset --hard origin/master'
```
