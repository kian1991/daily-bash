# Kian's Bash Script Collection

This is a collection of bash scripts that I have written to automate various tasks. I have written these scripts to make my life easier. If you can make use of them, feel free to use them.

## Scripts

# `webimg`

A bash script to compress and convert images to WebP format efficiently.


## **Prerequisites**

- The script requires 'imagemagick' to be installed on the system.

```bash
sudo apt-get install imagemagick
```

or on **macOS**

```bash
brew install imagemagick
```


## **Features**

- Supports batch processing with patterns like `*.jpg`.
- Handles file names with spaces.
- Configurable compression quality, scale, and lossless mode.
- Option to overwrite original files or keep them.


## **Usage**

```bash
./webimg [-s scale] [-q quality] [-x] [-f] [-v] <file_pattern>
```

### **Options**

- `-s`: Scale percentage (default: 100).
- `-q`: Quality percentage (default: 60).
- `-x`: Overwrite original files.
- `-f`: Force overwrite without prompt.
- `-v`: Enable verbose output with a compression summary.



# `create-rtw`

A bash script to create a new React project with TypeScript using Vite, pre-configured with Tailwind CSS, and some additional cleaning and setup steps for an optimized development environment.


## **Features**

- Automates the setup of a React + TypeScript project with Vite.
- Installs and configures **Tailwind CSS**, **PostCSS**, and **Autoprefixer**.
- Sets up a clean project structure by removing unnecessary files and adding a simple starting point.
- Integrates **Prettier** with a Tailwind CSS plugin for auto-sorting utilities.
- Creates a minimalistic starting `App` with Tailwind styling.


## **Usage**

### **Run the script**
```bash
./create-rtw <project-name>
```

If `<project-name>` is not provided, the script will prompt you to enter a project name.



# `copy-xterm-info`

A bash script to synchronize the terminal capability database (`termcap`) with a remote host.


## **Features**

- Transfers the terminal capability settings (`infocmp`) from the local machine to a remote host.
- Uses `ssh` to securely send the configuration.
- Simplifies ensuring terminal compatibility when working with remote systems.


## **Usage**

```bash
./termcap-sync <hostname>
```

### **Arguments**

- `<hostname>`: The hostname or IP address of the remote system to which the terminal capabilities should be synchronized.


## **Prerequisites**

- SSH access to the remote host is required.
- The `infocmp` and `tic` commands must be available on both the local and remote systems.

