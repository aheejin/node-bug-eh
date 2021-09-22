This repo is for reporting a bug that [Node](https://nodejs.org/en/) causes a segmentation fault when running a Wasm program with [exception handling](https://github.com/WebAssembly/exception-handling) feature.

[Node v16.9.1](https://nodejs.org/en/) was used.

Steps to reproduce Node segmentation fault:
```
$ git clone https://github.com/aheejin/node-bug-eh.git
$ cd node-bug-eh/node
$ node -experimental-wasm-eh wasm-opt.js -all -O1 test.wasm
```

Steps to run `d8` shell from [v8](https://github.com/v8/v8). This seems to run successfully.
```
$ git clone https://github.com/aheejin/node-bug-eh.git
$ cd node-bug-eh/d8
$ d8 -experimental-wasm-eh wasm-opt.js -- -all -O1 test.wasm
```
