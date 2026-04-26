# Project README

## Overview
This project is a simple C application that utilizes a custom TerminalEngine library to create a terminal-based user interface. The application listens for mouse and keyboard events, updates the terminal display accordingly, and exits when the 'Q' key is pressed.

## Features
- **Mouse Interaction**: The application can detect left mouse clicks within the terminal window and change the pixel color at the click location.
- **Keyboard Interaction**: The application can detect the 'Q' key press to exit the application.
- **Cross-platform Build**: The project includes Makefiles for building on Linux, Windows, Wine (for cross-compiling to Windows), and WebAssembly.

## Project Structure
### Prerequisites
- C/C++ Compiler and Debugger (GCC, Clang)
- Make utility
- Standard development tools
- TerminalEngine.h library

## Build & Run
To build the project, navigate to the project directory and run the following command:

```sh
make -f Makefile.(os) all
```

Replace `(os)` with `linux`, `windows`, `wine`, or `web` depending on your target platform.

For a clean rebuild, use:

```sh
make -f Makefile.(os) clean
make -f Makefile.(os) all
```

To execute the built application, run:

```sh
make -f Makefile.(os) exe
```

### Additional Build Options
- **Build and Execute**: `make -f Makefile.(os) do`
- **Clean Build Artifacts**: `make -f Makefile.(os) clean`
- **Build Libraries**: For Windows, you can build the library with `make -f Makefile.windows cleanlib` followed by `make -f Makefile.windows lib`.