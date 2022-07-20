# Proxmox Remote Development Server Setup

Setup a remote VM hosted on Proxmox that you can develop on from your local machine using Neovim or VSCode (next to no setup)

### Prerequisites

- Setup a Ubuntu VM (Preferrably Server) on Proxmox. Straight forward process of filling in the forms and continuing.

- After first install, enable qemu-guest-agent in VM settings on Proxmox side.

- Install qemu-guest-agent in the VM via `apt`.

- SSH into the server.

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

