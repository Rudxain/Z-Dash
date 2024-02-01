# Z-Dash

This is intended to deviate from some of RobTop's design decisions, since I don't agree with them. It's also intended to fix his "non undo-able" mistakes.

There will be emphasis on sight-readability and accessibility, from the very start.

This game won't have main levels/maps. It's just a platform for making and playing.

I'll try my best to make modding/resource-packs as friendly as possible, providing APIs. The first implementations will be unstable, until the community reaches a consensus.

The map file-format will be easily machine-readable. I can't guarantee the format will be stable, so a "bridge" interface may be needed to ensure any user-land programs continue working indefinitely.

The game will be offline (serverless). So creators/artists will have to share their maps using social-media platforms, or other cloud-hosting services. This also means there are no "featured" nor "officially rated" levels/maps. Creators & players are entirely responsible for properly rating their maps (this will be included in the metadata), and the community will decide which maps deserve to be "featured".

The game will be distributed as a Wasm PWA, so it'll be cross-platform, with minimal development cost, but slightly slower than a native app (don't worry, I'll use WebGL in the future)

Difficulties & scores. f(n) = 4^n - 1:

0. Safe Auto, 0: No matter what you do, you can't die.
1. Unsafe Auto, \[1, 3]: If you click, you might die.
2. Easy \[4, 15] ("Easy" to "Normal")
3. Medium \[16, 63] ("Hard" to "Harder")
4. Hard \[64, 255] ("Harder" to "Medium-Demon")
5. Extreme \[256, 1023] ("H.D." to "E.D.")

Scores will be one of the only things to use fixed-precision float arithmetic. This guarantees the "resolution" of each difficulty-range is the same for all difficulties
