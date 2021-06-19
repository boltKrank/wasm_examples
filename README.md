# wasm_examples

Various code examples/implementations of WASM for testing and education

## What is WebAssembly (WASM)

WASM is made up of 2 parts: the "Glue" and the "Module"

### The module

Usually outputted as a .wasm file, this is the compiled binary of the imput language. Sicne it is pre-compiled, the performace is close to native (minus browser overheads).

### The glue

This is a massive JavaScript file that translates the tradition Javascript requests from the browser into API calls for the module. Currently it can only communicate via API and not directly (i.e. C++ DOM)

### Creating the module and glue

There are lots of tools out there that can create .wasm  module and the JavaScript glue. In this case we'll focus on Emscription, which uses Clang + LLVM to create .wasm module.

## Setting up test web server

Due to security restrictions most browsers won't let you run code off a local file, also if there is any server-side languages being used, they wont be processed when using a local copy.

Best way around this is to host the files on a simple local web server.

nginx and Apache are two popular choices, but might be overkill for this.

Python http.server is a good low-profile solution for this.

For Python 3+ the command is:

`python3 -m http.server`

## Use cases

<https://webassembly.org/docs/use-cases/>
