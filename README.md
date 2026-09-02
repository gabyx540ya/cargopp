# cargopp

A lightweight package manager and build tool template for C++ projects, heavily inspired by Rust's Cargo and powered by CMake.

## Features
- **Easy Installation**: One command to install it globally.
- **Fast Project Creation**: Generate a fully configured C++20 project boilerplate with a clean `CMakeLists.txt` and `src/main.cpp`.
- **Seamless Build & Run**: Automates CMake generation, compilation, and execution without writing multi-line commands.

## Installation

### Option 1: One-Line Ultra Fast Install (Recommended)
Open your terminal and paste this single command to download, install globally, and clean up automatically:
```bash
curl -fsSL https://githubusercontent.com -o cargopp && chmod +x cargopp && sudo ./cargopp install && rm cargopp
```

### Option 2: Standard Git Clone
If you prefer to keep the source code locally, clone the repository and run the installer manually:
```bash
git clone https://github.com
cd cargopp
sudo ./cargopp install
```
*(Once installed via Git, you can safely delete the cloned folder if you want).*

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
