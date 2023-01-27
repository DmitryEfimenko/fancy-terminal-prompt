# Fancy Terminal Prompt
Settings and steps to enable fancy terminal prompt for Windows Terminal

Steps from [this video](https://youtu.be/AK2JE2YsKto).

## Step 1: Install nerd fonts
1. Download font from [nerdfonts.com](https://www.nerdfonts.com/). For example, JetBrainsMono Nerd Font
2. Extract archive
3. Select all font files > Right click > Install for all users

## Step 2: Setup Starship on Windows

1. Install following [Instructions](https://starship.rs/guide/#%F0%9F%9A%80-installation) for Windows - (using MSI installer is the easiest)
2. `code $PROFILE`
3. Add this at the end:
   ```sh
   $ENV:STARSHIP_CONFIG = "$HOME\.starship\starship.toml"
   $ENV:STARSHIP_DISTRO = "者 xcad"
   Invoke-Expression (&starship init powershell)
   ```
4. `code $HOME\.starship\starship.toml`
5. Paste contents of Startship config file and save
6. Restart Terminal

## Step 3: Setup Startship on WSL2 Linux

1. Install following [Instructions](https://starship.rs/guide/#%F0%9F%9A%80-installation) for Linux
2. `vim ~/.bashrc`
3. Add this at the end:
   ```sh
   eval "$(starship init bash)"
   ```
4. `source ~/.bashrc`
5. `mkdir -p ~/.config && touch ~/.config/starship.toml`
6. `vim ~/.config/starship.toml`
7. Paste contents of Startship config file and save
