# jello-jdlls

Community JDLL packages for the Jello platform.

| Package | Description |
|---------|-------------|
| [ava](ava/) | AVA-style unit testing for Jello projects |
| [motive](motive/) | PLPlot-backed snapshot graphing for observability |
| [ripple](ripple/) | Kiss FFT / STFT signal processing for audio and time series |
| [hush](hush/) | Real-time speech denoising (RNNoise) |
| [oracle](oracle/) | ONNX Runtime inference — load models, run tensors |
| [crucible](crucible/) | AI experiment playground — pipelines, metrics, domain helpers |

Each package is a standalone Jello project with `jello.json`, `src/`, and `jdll/`. Sibling dependencies are resolved via `package_paths` in `jello.json` (typically `".."` for this workspace). Local overrides may still live under `{app}/packages/{name}/`, or install to `JELLO_LIB_PATH/{name}/{version}/`.
