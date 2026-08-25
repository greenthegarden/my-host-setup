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
- [fastfetch](https://github.com/fastfetch-cli/fastfetch): System information
- [dust](https://github.com/bootandy/dust): Manage disk space
- [tealdeer](): 
- [uv](https://docs.astral.sh/uv/getting-started/installation/): Python and dependency management
- [pi.dev](https://pi.dev/): Agent harness
- [herdr](https://herdr.dev/): Agent runtime

See https://github.com/alebcay/awesome-shell and https://github.com/agarrharr/awesome-cli-apps.

## Generating SSH keys

Generate a key using

```sh
ssh-keygen -t ed25519 -f ~/.ssh/id_ed25519_<use> -C "origin and where key is used"
```

Add to `~/.ssh/config`.

### SSH for Github

```sh
ssh-keygen -t ed25519 -f ~/.ssh/id_ed25519_github -C "user@host"
```

Add following to `~/.ssh/config`,

```bash
Host github.com
	Hostname github.com
	PreferredAuthentications publickey
	IdentityFile ~/.ssh/id_ed25519_github
```

## Packeage Replacements

| Command | Replacement |
| ------- | ----------- |
| du      | duf         |
| cat     | bat         |
| find    | fd          |
| grep    | ripgrep     |
| ls      | eza         |
| ls      | yazi        |
| man     | tealdeer    |
| top     | btop        |

