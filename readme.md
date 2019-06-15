**Enabling WSL**

```
	# Press Win+r
	# Write "powershell"
	# Press Ctrl+Shift+Enter for Administrator PowerShell

	# Execute this command:
	Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

**Installing WSL**

Go to the Microsoft Store and install "Ubuntu"

Simply clone this repo and download it as .zip

**Basic setup of WSL**

```bash
	# Run bash.bat and execute:
	sudo apt update
	sudo apt upgrade
```

**Installing node**

```bash
# First run bash.bat

# Download nodejs
wget https://nodejs.org/dist/v10.16.0/node-v10.16.0-linux-x64.tar.xz

# Unpack the archive to home dir
unp node-v10.16.0-linux-x64.tar.xz

# Start the text editor
nano .bashrc

# This is optional for .bashrc, to remove all the ugly WSL NT /mnt paths
PATH="/usr/local/sbin"
PATH=$PATH":/usr/local/bin"
PATH=$PATH":/usr/sbin"
PATH=$PATH":/usr/bin"
PATH=$PATH":/sbin"
PATH=$PATH":/bin"
PATH=$PATH":/usr/games"
PATH=$PATH":/usr/local/games"

# Add this line where you want, e.g. at bottom:
PATH="/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games"
PATH=`pwd`"node-v10.16.0-linux-x64/bin":$PATH

# Exit nano via `Ctrl+x` and `y`
```

