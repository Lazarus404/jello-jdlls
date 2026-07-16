# Jello JDLL's

Jello packages, most of them bindings to a native library through a `.jdll`. Each one is its own repository, included here as a submodule.

These JDLL's were vibe-coded based on my own personal interests as an experiment for my programming language - [Jello](https://github.com/Lazarus404/jello-lang) - as a means to experiment and test Jello's capabilities. They also work as a good starting point for an extension repo.

| Package | Description |
|---------|-------------|
| [wordtree](https://github.com/Lazarus404/wordtree) | Editable UTF-8 text ropes, on librope |
| [ripple](https://github.com/Lazarus404/ripple) | Real FFTs and short-time Fourier transforms, on Kiss FFT |
| [hush](https://github.com/Lazarus404/hush) | Real-time speech denoising, on RNNoise |
| [motive](https://github.com/Lazarus404/motive) | Snapshot charts as PNG or SVG, drawn by PLplot |
| [oracle](https://github.com/Lazarus404/oracle) | ONNX Runtime inference: load a model, run tensors through it |
| [oracle-train](https://github.com/Lazarus404/oracle-train) | ONNX Runtime training: train steps, checkpoints and inference export |
| [crucible](https://github.com/Lazarus404/crucible) | An experiment playground: pipelines, metrics, and tabular, audio and RTP helpers |
| [gel](https://github.com/Lazarus404/gel) | 2D windows, input, graphics and audio, on CSFML |
| [wobblertc](https://github.com/Lazarus404/wobblertc) | WebRTC peers on libpeer: WHIP and MQTT signalling, audio, video and data channels |
| [snack](https://github.com/Lazarus404/snack) | Keyboard input: terminal raw mode, the Windows console and Linux evdev |
| [vocaleyes](https://github.com/Lazarus404/vocaleyes) | Speech output: a fast echo path and neural voice synthesis |
| [docbrown](https://github.com/Lazarus404/docbrown) | Markdown export and one-way cloud sync, through Pandoc and rclone |
| [switchboard](https://github.com/Lazarus404/switchboard) | Wi-Fi provisioning: NetworkManager through nmcli |

## Using a package

Add it to your project's `jello.json` and fetch it:

```json
"dependencies": {
  "wordtree": {"github": "Lazarus404/wordtree", "tag": "0.1.0"}
}
```

```sh
jelloc deps.get
```

A package with a native library is then built with its `build.sh`, for example
`packages/wordtree/build.sh`; its README names the library it needs and how to install it.

## Working on the packages

Clone with `--recursive`. Packages that use a sibling, such as oracle-train on oracle, find it
through `"package_paths": [".."]` in their `jello.json`. Each package's tests run with its
`./test.sh`, on [degust](https://github.com/Lazarus404/degust) and `std.testing`.
