# My Host Setup

Guide to follow to set up consistent systems.

## Based Configuration

Use https://github.com/radleylewis/zsh as a base

### Fonts

Install nerd font using

```sh
wget -P ~/.local/share/fonts https://github.com/ryanoasis/nerd-fonts/releases/download/v3.5.1/FiraMono.zip \
&& cd ~/.local/share/fonts \
&& unzip FiraMono.zip \
&& rm FiraMono.zip \
&& fc-cache -fv
```

## Configuring Git

Use the following to set git configuration

```sh
git config --global init.defaultBranch main
git config --global user.name <surname, firstname>
git config --global user.email <email>
```

Check settings using

```sh
git config --list
```

## Additional Tools

- [autin](https://atuin.sh/): Shell history
- [uv](https://docs.astral.sh/uv/getting-started/installation/): Python and dependency management
- [pi.dev](https://pi.dev/): Agent harness
- [herdr](https://herdr.dev/): Agent runtime
