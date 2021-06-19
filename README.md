# wasm_examples

Various code examples/implementations of WASM for testing and education

## Emscripten

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

## Setting up test web server

Due to security restrictions most browsers won't let you run code off a local file, also if there is any server-side languages being used, they wont be processed when using a local copy.

Best way around this is to host the files on a simple local web server.

nginx and Apache are two popular choices, but might be overkill for this.

Python http.server is a good low-profile solution for this.

For Python 3+ the command is:

`python3 -m http.server`
