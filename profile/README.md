# CDP-WASM-SUITE

A collection of projects based around a WASM port of the [Composer's Desktop Project](https://www.composersdesktop.com/) - using the latest web technologies to bring a new lease of life to 40 year old software - (hopefully) making it more easily accessible and fun to use.

<img width="636" height="372" alt="cdp-web frontend" src="https://cdp-wasm-suite.github.io/shots/patch-gem.png" />

The main motivation is that offline audio processing tools like CDP are very interesting to control via natural language with LLMs. With a thin javascript orchestration layer and a virtual file system, the CDP can be very powerful for **agentic** sound design.

You can use [cdp-wasm](https://github.com/cdp-wasm-suite/cdp-wasm) on the command line via node or compatible JavaScript runtime see the [npm package](https://www.npmjs.com/package/cdp-wasm) on npm.js.

```bash
// install cdp-wasm globally
npm i -g cdp-wasm

// use the cdp modify program - speed mode 2 to transpose in.wav down 12 semitones
cdp modify speed 2 in.wav out.wav -12
```

This is much like using the original CDP (where you must cross-reference the [docs](https://www.composersdesktop.com/docs/html/cgromody.htm#SPEED) to get the command correct)

Remembering all those arguments is challenging, and when multiple programs are involved CDP can be very laborious to use like this. Many people use a [UI frontend](https://www.composersdesktop.com/interfaces.html) instead.

In cdp-wasm the javascript layer adds a curated catalog on top of the CDP programs that surfaces subprograms of CDP as ready-to-use effects and generators — each with curated parameters, ranges and defaults — and hides the multi-step plumbing (pvoc round-trips, mixfile chains, channel conforming).

```js
import { CDP, EFFECTS, applyEffect } from 'cdp-wasm';

const cdp = new CDP();
const effect = EFFECTS.find((e) => e.id === 'modify.speed');
const out = await applyEffect(cdp, effect, { semitones: -12 }, await readFile('in.wav'));
await writeFile('out.wav', out);
```

Agentic tools can also help here. You can use the [agent-skills](https://github.com/cdp-wasm-suite/cdp-wasm/#agent-skills-and-plugins) to control it from claude, codex etc.

If you prefer a UI, [cdp-web](https://cdp-web.app) is a web based frontend, which you can use in the browser. It's a [Progressive Web App](https://web.dev/explore/progressive-web-apps) so you can also install it to your desktop or your home screen on mobile. The agent-skills should also be able to create cdp-web patches.

The same UI frontend is used in the [audio plugin](https://github.com/cdp-wasm-suite/cdp-plugin/releases/tag/latest), and the [DAW Extension](https://github.com/cdp-wasm-suite/cdp-extension/releases/tag/latest).

This laborious work has largely been automated using agentic AI - so YMMV - there will be mistakes, bugs and sloppy bits. It's still WIP, being de-sloppified. Please submit issues if you find any.

For more info visit the [main website](https://cdp-wasm-suite.github.io).

Enjoy!

Oli Larkin, Berlin, 2026.
