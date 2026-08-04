# CDP-WASM-SUITE

A collection of projects based around a WASM port of the [Composer's Desktop Project](https://www.composersdesktop.com/)

This work has largely been automated using agentic AI - so YMMV. It's still WIP. Please submit issues if you find any.

The main motivation is that offline audio processing and especially CLI tools are very interesting to control via natural language with LLMs. With a thin javascript orchestration layer and a virtual file system, the CDP can be ideal for **agentic** sound design.

**Use it on the command line via node or compatible JavaScript runtime [see cdp-wasm on NPM](https://www.npmjs.com/package/cdp-wasm)**

```
npm i -g cdp-wasm
cdp modify speed 2 in.wav out.wav -12
```

**Or use the [agent-skills](https://github.com/cdp-wasm-suite/cdp-wasm/#agent-skills-and-plugins) to control it from claude, codex etc.**

**Or use the cdp-web ui, in the browser, on a mobile device, in an audio plugin, or in a DAW Extension.**

<img width="636" height="372" alt="gem" src="https://cdp-wasm-suite.github.io/shots/patch-gem.png" />

For more info visit the [main website](https://cdp-wasm-suite.github.io).
