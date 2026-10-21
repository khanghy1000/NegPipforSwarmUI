# NegPip for SwarmUI

Adds a **Use NegPip** toggle to SwarmUI so you can use negative weights inside your *positive* prompt.

## Requirements

SwarmUI with the ComfyUI backend (standard setup). The required Comfy node packs are installed automatically as installable features:

- [ComfyUI-ppm](https://github.com/pamparamm/ComfyUI-ppm) for SD1, SDXL, Anima, MOSS Image
- [ComfyUI-krea2-negpip](https://github.com/blue-pen5805/ComfyUI-krea2-negpip) for Krea 2

## Supported models

SD1, SDXL, Anima, Krea 2, and MOSS Image. On MOSS Image, regular prompt weighting such as `<weight[2]:word>` is also enabled. Nunchaku models are not supported, and other incompatible models are skipped without error.

## Install

1. Clone this repository into `SwarmUI/src/Extensions/NegPipforSwarmUI/`.
2. Restart SwarmUI.

## Usage

Open the **NegPip** parameter group in the generation sidebar and enable **Use NegPip**, then write negative weights in the positive prompt:

```text
a photo of a <weight[-1.5]:yellow> cat.
```

The extension inserts the NegPip node between the model/CLIP loaders and the rest of the workflow. Leave the toggle off and generation behaves exactly as normal.

## Updating / Uninstalling

Use `Server` -> `Extensions` (or `git pull` in this folder) and restart SwarmUI to apply. To uninstall, delete the `NegPipforSwarmUI` folder and restart.

## Credits

- [ComfyUI-ppm](https://github.com/pamparamm/ComfyUI-ppm) by [pamparamm](https://github.com/pamparamm).
- [ComfyUI-krea2-negpip](https://github.com/blue-pen5805/ComfyUI-krea2-negpip) by [blue-pen5805](https://github.com/blue-pen5805).
- The original extension by <b>Hugs288</b>.

Report issues at <https://github.com/khanghy1000/NegPipforSwarmUI/issues>.
