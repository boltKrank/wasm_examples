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

## Usage examples:

- [C++ Hello World!](cpp_hello_world/cpp_hello_world.md)
