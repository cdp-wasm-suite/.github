# CDP-WASM-SUITE

A collection of projects based around a WASM port of the [Composer's Desktop Project](https://www.composersdesktop.com/)

This work has largely been automated using agentic AI. I plan to humanize aspects of it as I go. Please submit issues if you find any.

The main motivation is that offline audio processing and especially CLI tools are very interesting to control via natural language with LLMs.

Via WASM and a virtual file system, the CDP can be ideal for **agentic** sound design.

usage via node [see cdp-wasm on NPM](https://www.npmjs.com/package/cdp-wasm):

```
npm i -g cdp-wasm
cdp modify speed 2 in.wav out.wav -12
```

Or use the claude-code plugin to get started straight away.
```
/plugin marketplace add cdp-wasm-suite/cdp-wasm
/plugin install cdp-sound-design@cdp-wasm
```

Or use the cdp-web ui, in the browser, on a mobile device, in an audio plugin, or in a DAW Extension.

<img width="636" height="372" alt="gem" src="https://github.com/user-attachments/assets/07d58869-5be2-4cb4-b91e-91ff585ea4e0" />

-> https://cdp-wasm-suite.github.io
