# C++ Hello World! WASM Example

This example uses Emscripten

Installation instructions are in main README file

The command `emcc hello.c -s WASM=1 -o hello.html`  will be execuited to convert hello.c to the Javascript equivalents.

Once this one was run, 3 new files were generated:

hello.html
hello.js
hello.wasm

NOTE: The HTML file relies on a web server to present it. Opening it directly in a static browser will most likely not work.

NOTE: the .wasm file contains all the binaries that couldn't be ported to JavaScript.

TODO: Trace HTML, JS and WASM files to see what was generated and reverse-engineer possible methodologies.