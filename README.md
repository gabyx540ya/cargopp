# cargopp

A lightweight package manager and build tool template for C++ & C projects, inspired by Rust's Cargo and powered by CMake.

The goal is to simplify common C++&C workflows such as:
* Creating new C++&C projects
* Configuring projects with CMake
* Building projects
* Running executables
* Managing common development workflows

## Features
- **Easy Installation**: One command to install it globally.
- **Fast Project Creation**: Generate a fully configured C++20 project boilerplate.
- **Seamless Build & Run**: Automates CMake generation, compilation, and execution without writing multi-line commands.


## Prerequisites

Before installing `cargopp`, ensure your system has the following tools installed:

- **OS**: linux(debian/ubuntu, redhat)
- **Build System**: `cmake` (>= 3.16)
- **Compiler**: A C++20 compatible compiler (`g++` >= 10 or `clang`)
- **Downloader**: `curl` (for one-line installation)


## Installation

You can install `cargopp` using one of the two options below:

### Option 1: One-Line Ultra Fast Install (Recommended)
Open your terminal and paste this single command to download, install globally, and clean up automatically:

```bash
curl -fsSL https://raw.githubusercontent.com/gabyx540ya/cargopp/main/src/lib/linux/ubuntu_debian/install -o install && chmod +x install && sudo ./install
```

*💡 Note: If `curl` is not installed on your Ubuntu/Debian system, you can install it by running:*
```bash
sudo apt update && sudo apt install curl -y
```

---

## Usage

### 1. Create a new C++ project
To generate a new project structure, run:
```bash
cargopp new my_project
```
This will automatically create a folder containing:
- `src/main.cpp` (a simple "Hello, C++!" template)
- `CMakeLists.txt` (pre-configured with C++20 standards and strict compiler warnings `-Wall -Wextra -Wpedantic`)
- An empty `build/` directory.

### 2. Build your project
Navigate to your project root folder and build it using CMake automatically:
```bash
cd my_project
cargopp build
```

### 3. Run your program
To automatically build and execute your binary file, provide the target name (usually your project name) to the run command:
```bash
cargopp run my_project
```

---

## Commands Reference

| Command | Argument | Description |
| :--- | :--- | :--- |
| `cargopp install` | *None* | Installs the script globally into `/usr/local/bin` (Requires `sudo`). |
| `cargopp new` | `<project_name>` | Generates a new C++ template folder. |
| `cargopp build` | *None* | Generates and runs the CMake build pipeline inside `./build`. |
| `cargopp run` | `<program_name>` | Re-builds and executes the binary from `./build/`. |

---
## License
This project is open-source. Feel free to use, modify, and distribute it!
