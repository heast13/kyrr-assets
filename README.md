# kyrr-assets

Mirrors of the files [kyrr](https://github.com/heast13/kyrr) downloads or
builds with, so they stay available whatever happens to their original
homes. Every file is unchanged; kyrr checks each one against the SHA256 in
its source before using it. Nothing in this repository is meant to be used
on its own.

## Releases

### `models-1`: dictation models

Downloaded by the kyrr app (after [heast13/kyrr-models](https://huggingface.co/heast13/kyrr-models)
on Hugging Face, which has the same files and a model card).

| Files | Model | License |
|---|---|---|
| `de-primeline-u8.*` | primeLine AI's [parakeet-primeline](https://huggingface.co/primeline/parakeet-primeline), based on NVIDIA parakeet-tdt-0.6b-v3, converted for kyrr with [`tools/export-primeline`](https://github.com/heast13/kyrr/tree/main/tools/export-primeline) | [CC-BY-4.0](https://creativecommons.org/licenses/by/4.0/) |
| `en-unified.*` | NVIDIA [parakeet-unified-en-0.6b](https://huggingface.co/nvidia/parakeet-unified-en-0.6b), ONNX int8 by the [sherpa-onnx](https://github.com/k2-fsa/sherpa-onnx) project | NVIDIA Open Model License, copy in `en-unified.NVIDIA-Open-Model-License.pdf` |

Licensed by NVIDIA Corporation under the NVIDIA Open Model License.

### `build-1`: build inputs

Fetched by kyrr's `scripts/fetch-assets.py` (before the original sources).

| Files | What | License |
|---|---|---|
| `dpdfnet*_48khz_hr.onnx`, `dpdfnet*_48khz_hr.weights.f32` | DPDFNet models by [Ceva](https://github.com/ceva-ip/DPDFNet), from the [HushMic](https://github.com/Fovty/HushMic) v0.10.2 release | Apache-2.0, `LICENSE-Apache-2.0.txt` |
| `onnxruntime-win-x64-1.27.0.zip` | [ONNX Runtime](https://github.com/microsoft/onnxruntime) 1.27.0 by Microsoft, as released | MIT, license and notices inside the archive |
| `sherpa-onnx-v1.13.8-win-x64-static-MT-Release-no-tts-lib.tar.bz2` | [sherpa-onnx](https://github.com/k2-fsa/sherpa-onnx) 1.13.8 static libraries without text-to-speech, as released | Apache-2.0, `LICENSE-Apache-2.0.txt` |
| `de.wav`, `en.wav` | test clips from sherpa-onnx's `asr-models` release | Apache-2.0, `LICENSE-Apache-2.0.txt` |

A new version of any file goes into a new release (`models-2`, `build-2`, …);
published releases stay as they are, because kyrr versions link to them.
