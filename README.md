This repo is for reporting a bug that `node` causes a segmentation fault when running a Wasm program with [exception handling](https://github.com/WebAssembly/exception-handling) feature.

Steps to reproduce the bug:

```
$ git clone git@github.com:aheejin/node-bug-eh.git (or git clone https://github.com/aheejin/node-bug-eh.git)
$ cd node-bug-eh
$ node -experimental-wasm-eh wasm-opt.js -all -O1 test.wasm
```
