# Setting up Emscription

This tool converts LLVM (see <https://llvm.org/>) to JavaScript. Takes the bytecode generated from C++ and compiles that into Javascript which can then be run via a browser.

Emscripten can convert any language that uses LLVM into WebAssembly. Other languages include (although not as complete as C++):

- Ruby
- Python
- Haskell
- Rust
- D
- PHP
- Lua

## Emscripten download instructions

*NOTE: Python 3.6+ is required.*

<https://emscripten.org/docs/getting_started/downloads.html>

## Usage examples

- [C++ Hello World!](cpp_hello_world/cpp_hello_world.md)

### Mac install steps

#### Fetch the latest version of the emsdk (not needed the first time you clone)

git pull

##### Download and install the latest SDK tools

./emsdk install latest

##### Make the "latest" SDK "active" for the current user. (writes .emscripten file)

./emsdk activate latest

#### Activate PATH and other environment variables in the current terminal

source ./emsdk_env.sh
