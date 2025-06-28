---
title: "Working without Sudo in Unix Terminal"
seoTitle: "Unix Terminal Tips: Work Without Sudo"
seoDescription: "Learn to work on Unix without sudo access by using tools like `uv` and `eget` for package installation and dotfile management."
datePublished: Fri Jun 27 2025 19:33:55 GMT+0000 (Coordinated Universal Time)
cuid: cmcf7nb5x000009jr39ntf0r0
slug: working-without-sudo-in-unix-terminal
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1751052823557/ee3c78ca-ae02-4eca-b475-d4e5db16dc4c.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1751052626514/d528b157-1462-4217-84a1-fd6706ed5e2c.png
tags: unix, terminal, shell, sudo, unixcommands

---

Many times when we are connecting to a remote server via ssh, or using a Linux machine without sudo access i.e. you are not `root`, it is just painful that you cannot install packages which make your terminal workflow easier.  
Yes, I am talking about JUST TERMINAL! This article does not deal with anything outside of terminal! And in the current era, if you still live in the plain old Default `GNOME terminal` or `Terminal.app`, you are living under a rock.

So picture this scenario again. You ssh into your machine, you do not have ssh. You are toooo used to working with your snazzy shell with plugins, **Neovim** or Emacs(seriously?), Terminal Multiplexer like Tmux, etc. powered with `fzf`, `zoxide`, `yazi`, `lazygit`, `eza` and much much more!!! But all these require some package manager to install with, but there does not exist any! You do not have sudo access or get it(for some reason). What should I do?

Here are some solutions I discovered myself because I like, as what they say in Hindi, “jugaad”(meaning workaround fix).  
Note that, the solutions become more better as the number increases. By the end of this, you can almost replicate your terminal workflow as it is in your local machine, WITHOUT SUDO!

## Solution 1: Easy Way Out! But less se\*y… 😴

Well, the easiest way out is, SSH through your IDE like VS Code. This is quite convenient for more users nd they like this way quite a lot, cause you have all your customizations and AI powered tools pre-installed in local VS Code instance. Install some more plugins on remote and you are done! Easy right!

But wait, the shell of the VS Code sucks! It is the plain old `sh` or `bash`(you would just hope atleast bash exists). And this may not be possible for all machines since you would need a VS code installation on the other side too. So let’s see what we can do about this.

## Solution 2: Configuring you Shell yourself! 💪

Now, here are some gift default Linux provides you. `Curl` and `Vi(m)`. So Step 1, we install [`uv`](https://docs.astral.sh/uv/). This is in general a new, super fast and much loved replacement of `pip`. Good news, we can install this with a simple curl request as mentioned in the installation instructions. Just run -

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

Great! Now, there exists a lot of python wrapper installations for various tools which I will list below.

1\. [Bing-su/pip-binary-factory](https://github.com/Bing-su/pip-binary-factory). Truly a gift. This repository has a lot of good languages/tools. I will highlight some of them.

* `lazygit-py` - Installs [lazygit](https://github.com/jesseduffield/lazygit) for you using simply `uv tool install lazygit-py`. Wow!
    
* `yazi-bin` - Install [yazi](https://github.com/sxyazi/yazi) for you with `uv tool install yazi-bin`. You can just clone your yazi plugins and more which doesn’t require sudo & you are done. Amazing!
    
* `fzf-bin` - Install [fzf](https://github.com/junegunn/fzf) with simply `uv tool install fzf-bin`. You can also [setup-shell-integration](https://github.com/junegunn/fzf?tab=readme-ov-file#setting-up-shell-integration) and much more, which you would know previously. Fantastic!
    
* `rustup-init-bin` - Install `rustup-init` command which when you run, installs `rustup` and hence all other rust toolchains like `cargo`, `clippy`, `rustc`, etc. This means now you have all possibly rust based tools which you can install! I will expand more on this in a later section! Rustyyy!!!
    

What else can be done from this repo? Apart from downloading all other which you might need which exists, you can always ask the repo owner to make one for you. I did, for [`yazi-bin #1`](https://github.com/Bing-su/pip-binary-factory/issues/1).

2\. [tmux-python/libtmux](https://github.com/tmux-python/libtmux) - Same method, install `tmux` with this. Done! Installing tmux plugins and configurations requires no plugins whatsoever. We are set with a multiplexer now.

Great! But what about Shell?? Well sad news, most shell needs `sudo` for installation. You have `bash` or `tcsh` usually preinstalled, but nothing more. Our beloved `zsh`, `fish` can’t be installed through this method. But I have a solution for you, in **Solution 3** Section! You can find some shells which can be installed without sudo, now that you have `uv` and `cargo`(and even `zig` if you notice carefully).

I would recommend using [`nushell`](https://github.com/nushell/nushell) which you can install using `cargo` with - (Check out the [Installations](https://www.nushell.sh/book/installation.html#build-from-crates-io-using-cargo) guide.)

```bash
cargo install nu --locked
```

`nushell` is fast, has inbuilt autocomplete, syntax-highlighting and honestly, get to know it better cause it is a really really good shell(might even become your favorite, though for me its `zsh` xD).

3\. [Pypi](https://pypi.org) and [crates.io](https://crates.io) - Now that you have `uv` and `cargo`, you have all access to all sorts of packages from these websites. Maybe you will discover more secrets of this world which I didn’t find!

### Text-Editing and Editors

What about Text-editor? You can use `nano`,`vim`, with simple `vimrc` customizations(if you don’t have one, search the web or AI for one), and its plugins can be installed. But what about the infamous `neovim`, `emacs`, `micro` or `helix`? Well good news, you can build from source for all of them without sudo. I will highlight on how to install `neovim` with instructions, for others please check the links -

* [`emacs`](https://www.gnu.org/software/emacs/manual/html_node/efaq/Installing-Emacs.html)
    
* [`helix`](https://docs.helix-editor.com/master/building-from-source.html)
    
* `micro` can be installed with `uv tool install micro-editor`, again by above mentioned repo.
    
* `Neovim` - Let’s see the instructions on how to build this from source -
    

```bash
# Step 1. Git clone the Repo
git clone https://github.com/neovim/neovim.git
cd neovim

# Step 2. Build
make CMAKE_BUILD_TYPE=Release
make CMAKE_INSTALL_PREFIX=$HOME/local/nvim install

# And you are done. Find the path where `nvim` executable is present
# And make an alias in ~/.bashrc(or your shellrc).
alias nvim="$HOME/local/nvim/bin/nvim"
```

And you should be done. See the above link provided for more options and information. You can also use your favorite neovim plugin manager get LSP running and you are good to go! Check out an even easier way to install neovim in the below section.  
We have managed now to make a full fledged terminal ready for work as your usual one. With this much power, we can live nicely now!

But I am not done yet, I have more things to show you!!!

## Solution 3: eget prebuilt binaries! ⚡💪

Well, I found this amazing repository [**eget**](https://github.com/zyedidia/eget)**.** This installs prebuilt binaries from Github very easily. Yes! Even without `eget`, you can install prebuilt binaries from repositories and install commands. But `eget` makes it so much easier to install binaries from GitHub, you don’t have to find them/get confused which one to download.

You can download `eget` using `uv tool install eget-py` or from source as mentioned in [README.md](https://github.com/zyedidia/eget?tab=readme-ov-file#from-source) -

```bash
git clone https://github.com/zyedidia/eget
cd eget
make build # or go build (produces incomplete version information)
```

Now you can simply install `neovim` with `eget neovim/neovim` and select the binary you want to install based on your system, and you are done! That’s it! So much easier. You can install binaries of `tmux`, `fzf`, and so many more whoever has them. Some examples as mentioned in the repository and some added by me include -

```bash
eget zyedidia/micro --tag nightly
eget jgm/pandoc --to /usr/local/bin
eget junegunn/fzf
eget neovim/neovim
eget ogham/exa --asset ^musl
eget --system darwin/amd64 sharkdp/fd
eget BurntSushi/ripgrep
eget -f eget.1 zyedidia/eget
eget zachjs/sv2v
eget https://go.dev/dl/go1.17.5.linux-amd64.tar.gz --file go --to ~/go1.17.5
eget --all --file '*' ActivityWatch/activitywatch

eget sharkdp/bat --to ~/.local/bin
eget charmbracelet/glow
```

Now you have `exa`, `ripgrep`, `golang`, `micro`(text-editor), `bat` and possibly many many more, directly in your path(using appropriate flags). Since you do not have sudo access, best way to put any executable in your path is to use `~/.local/bin` PATH. So any typical command will look like -

```bash
eget repo_author/repo_name --to ~/.local/bin
```

That’s it. This is much faster and more reliable than building from source. You can fetch new binaries from time to time, and it will replace the file. Make a `binaries.sh` file containing the list of all that you want, run `eget` on them to `~/.local/bin`, and you are done! You can simply manage your binaries too and update them with latest version easily. Here is one for you -

```bash
#!/bin/bash

# Ensure ~/.local/bin exists
mkdir -p ~/.local/bin

# Base packages to install with standard eget
BASE_PACKAGES=(
    "zyedidia/micro --tag nightly"
    "jgm/pandoc"
    "junegunn/fzf"
    "neovim/neovim"
    "BurntSushi/ripgrep"
    "charmbracelet/glow"
    "sharkdp/bat"
    "tmux/tmux"
)

# Special packages with custom flags
SPECIAL_PACKAGES=(
    ["oyejorge/gojq"]="--pre-release"
    ["zyedidia/eget"]="-f eget.1"
    ["ogham/exa"]="--asset ^musl"
    ["sharkdp/fd"]="--system darwin/amd64"
    ["zachjs/sv2v"]=""
)

# Install base packages
for pkg in "${BASE_PACKAGES[@]}"; do
    echo "Installing $pkg..."
    eget $pkg --to ~/.local/bin
done

# Install special packages
for pkg in "${!SPECIAL_PACKAGES[@]}"; do
    flags="${SPECIAL_PACKAGES[$pkg]}"
    echo "Installing $pkg..."
    eget $pkg $flags --to ~/.local/bin
done

# Handle more complex ones separately
eget https://go.dev/dl/go1.17.5.linux-amd64.tar.gz --file go --to ~/go1.17.5
echo "Installing go..."
# And more such if any

echo "All installations complete!"
```

You can run this from time to time, make a cronjob for it, to run every week and you are working with the latest stuff! You can provide `—upgrade-only` flag to just upgrade them too. There exists more ways to go about this for sure. But I think for a regular user this is good enough. All these solutions should provide you enough power to customize your shell even more.

### Shell Instructions

But again, what happened to `zsh`, `fish` and other shells? Well I found the perfect solution for `zsh`.

4\. [romkatv/zsh-bin](https://github.com/romkatv/zsh-bin) - Yes, I found one for zsh. You can simply curl request as mentioned in README or `eget romkatv/zsh-bin` and you are done! Yippeee. ZSH Exists! You can now use your zsh power!

Similarly you may find such repo’s for other shells you use. However for `fish`, I coudn’t find a good workaround. You can install the executable from releases of the official repo [fish-shell](https://github.com/fish-shell/fish-shell) using `eget`, but that is a but not straightforward. Check out the [Installation](https://github.com/fish-shell/fish-shell?tab=readme-ov-file#getting-fish) instructions for more information. One thing you can try is to build your fish in a similar environment as your remote machine using sudo, push it to releases of your Github dotfiles repository(or any other) and simply `eget` from there. This is not recommended and may not work. I tried on my Linux Ubuntu 22.04 instances and it worked. Maybe for you too.

There is still a disadvantage that your new shell can’t be default. Sorry, that strictly needs `sudo` to use `chsh` for changing default shell. Although one temporary fix it to add your shell initialization in your default shell profile script, to run your favorite shell when you enter. Although this is just a “jugaad”.

Here is a tip for you all to manage all your dotfiles and binaries so that this management does not become a headache.

## Managing dotfiles

You can manage your `dotfiles` using GNU Stow, this works great in both Linux and MacOS. Of course you can build it from source. To save your dotfiles, make `~/dotfiles/config_dir/config_file` and simply -

```bash
stow ~/dotfiles/config_dir
```

This will create a symlink to `~/config_dir/config_file` path. For more information visit the official documentations. But in short, for most of your `~/.config/confif_dir/config_file` files, store it as `~/dotfiles/config_dir/.config/config_dir/config_file` and stow using the above command. And you are done. One place for all your configs. You can make `~/dotfiles` a git repo and push your configs on GitHub for cloning it everywhere, even in the no-sudo machine you are working on.

## Summary

When you can't use sudo to install packages on a remote server or a restricted Unix machine, don't worry—there are some clever workarounds to recreate your favorite terminal setup. You can install the `uv` tool via curl, which makes it easy to download packages like `lazygit`, `fzf`, `yazi`, and `tmux`. If you're looking for a shell replacement, give `nushell` a shot—it's a great option that doesn't need sudo. You can also build apps like Neovim and Emacs from source if you're up for it. The `eget` tool is a lifesaver for grabbing prebuilt binaries from GitHub without needing sudo. And don't forget to use GNU Stow to manage and transfer your dotfiles easily. With these tricks, you'll have a powerful terminal setup without needing any admin privileges. Now go show off to your all your dev friends, that your simple remote machine is more capable than their native ones, all created without sudo!