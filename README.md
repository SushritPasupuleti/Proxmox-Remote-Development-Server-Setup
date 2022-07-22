# Proxmox Remote Development Server Setup

Setup a remote VM hosted on Proxmox that you can develop on from your local machine using Neovim or VSCode (next to no setup)

### Prerequisites

- Setup a Ubuntu VM (Preferrably Server) on Proxmox. Straight forward process of filling in the forms and continuing.

- After first install, enable qemu-guest-agent in VM settings on Proxmox side.

- Install qemu-guest-agent in the VM via `apt`.

- SSH into the server.

### Setup Dev Tools

Neovim (weapon of choice):

```bash
sudo apt install neovim
```

In some cases you may get an older version of Neovim than the current stable version. Head to [Neovim Docs](https://github.com/neovim/neovim/wiki/Installing-Neovim) to get instructions to proceed.

Setup your Config:

```bash
cd ~/.config/
mkdir nvim
cd nvim/
```

Add VimPlug (Used for Vim Plugins)

```bash
sh -c 'curl -fLo "${XDG_DATA_HOME:-$HOME/.local/share}"/nvim/site/autoload/plug.vim --create-dirs \
       https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim'
```

Populate your `init.lua`/`init.vim` and other config files here.

### Setup Node Development Environment

Install NVM:

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash
```

Reopen terminal.

Test Install:

```bash
nvim -v
```

For upgrades:

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash
```

Install Node via NVM:

Specify the version with:

```bash
nvm install x.x.x
```

Or Use LTS

```bash
nvm install --lts
```

Install Yarn (I like Yarn)

```bash
npm i -g yarn
```

### For VSCode Users

You're basically done, just setup remote session and point to your new VM. Enjoy the painfree experience 🙂.

