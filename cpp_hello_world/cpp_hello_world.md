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

*TODO: Trace HTML, JS and WASM files to see what was generated and reverse-engineer possible methodologies.*

To use an HTML template to produce a more simplified output (not the default Emscription one), run the following command:

`emcc -o hello2.html hello.c -O3 -s WASM=1 --shell-file html_template/shell_minimal.html`

NOTE this has to be run in the same directory as the hello2.c and html_template/shell_minital.html files.

TODO: remove all extra HTML padding so that the output is a simple HTML with just connections to the .wasm module

Minimal command: `emcc -o hello3.html hello.c -O3 -s WASM=1 --shell-file html_template/shell_minimal_mk2.html`

The file specified by --shell-file must have the {{{ SCRIPT }}} tag in it, and the file after -o must be a .html file. This {{{ SCRIPT }}} tag is replaced by a link to the JS file.

NOTE: Due to limitations of Windows - I'll use Ubuntu 18.04 WSL for compilation and testing.