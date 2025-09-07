# Setup

## Execute a command inside the container

```bash
podman exec -ti docker-compose-postgres_database_1 <command>
```

### Execute a shell

#### Bash

```bash
podman exec -ti docker-compose-postgres_database_1 /usr/bin/bash
```

When you first enter the container, you need to update the package lists and upgrade the installed packages:

```bash
apt-get update -y
apt-get upgrade -y
```

If needed, you can install other packages using `apt-get install <package-name>`.

```bash
apt-get install sudo -y
apt-get install curl -y
apt-get install neovim -y
```

If you want to use other shells like `fish`, you need to install them first and then you can start them by simply typing `fish` in the bash shell.

```bash
apt-get install fish -y

curl -sS https://starship.rs/install.sh | sh
echo "starship init fish | source" > ~/.config/fish/conf.d/starship.fish
```
