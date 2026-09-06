# MSCH Pointillism

Animate color-sampled dots over paper with distortion, ink bleed, grain and frame-hold controls.

[Node reference](docs/NODES.md) · [Example workflows and results](examples/README.md) · [Publishing guide](PUBLISHING.md)

![Actual demo output](examples/results/demo.png)

[Play / download the rendered demo](examples/results/demo.mp4)

## Included nodes

| Node | What it does |
|---|---|
| [Pointillism Effect (Video)](docs/NODES.md#pointillismeffect) | Scatter image-color-sampled dots across a paper-like background. |

## Installation

Clone into `ComfyUI/custom_nodes`:

```bash
git clone https://github.com/mariobilly/msch-pointillism.git
```

Open a terminal in the cloned folder and install requirements using **the same Python environment as ComfyUI**:

```bash
python -m pip install -r requirements.txt
```

Windows portable, from `ComfyUI_windows_portable`:

```powershell
.\python_embeded\python.exe -m pip install -r .\ComfyUI\custom_nodes\msch-pointillism\requirements.txt
```

Restart ComfyUI and refresh the browser. Load a JSON workflow from `examples/` and select the supplied demo input or your own media. Keep only one installed copy of each package to avoid duplicate node registrations.

## Requirements and behavior

Returns VIDEO, IMAGE frames and a dot coverage MASK. A still input is animated for the selected frame count; a batch is stylized frame by frame. Odd dimensions are trimmed for encoding. Performance depends on resolution, frame count and hardware; no universal speed claim is made.

## Documentation and examples

[docs/NODES.md](docs/NODES.md) documents every input, default, range, choice and output. [examples/README.md](examples/README.md) explains which inputs and other nodes each workflow needs and how the included results were produced.

## ComfyUI Manager

The release includes Comfy Registry metadata and a GitHub publishing action. **Publisher `mariobilly` is configured; Registry publication is pending the publishing secret and a successful publish run**. A separate [ComfyUI Manager node-list registration](https://github.com/Comfy-Org/ComfyUI-Manager/pull/3247) has been submitted; listing is pending maintainer acceptance. Git installation works independently. See [PUBLISHING.md](PUBLISHING.md).

## Validation

Imports and input schemas were checked against the local ComfyUI environment with Python 3.12.10, PyTorch 2.10 and CUDA available. Example render coverage is documented per workflow; this is not a claim of compatibility testing on every platform or of full MiniMax H3 model-generation validation.

## License

Project code: [MIT](LICENSE). Third-party assets and optional model weights keep their own licenses.
