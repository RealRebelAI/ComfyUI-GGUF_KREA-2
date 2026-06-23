# ComfyUI-GGUF - KREA-2 GGUF Support
GGUF Quantization support for native ComfyUI models

This node set literally just adds the KREA-2 architecture to the unet loader so you can utilize my ggufs. ill keep it updated so i can push new models more frequently.



![Comfy_Flux1_dev_Q4_0_GGUF_1024](https://github.com/user-attachments/assets/70d16d97-c522-4ef4-9435-633f128644c8)

Note: The "Force/Set CLIP Device" is **NOT** part of this node pack. Do not install it if you only have one GPU. Do not set it to cuda:0 then complain about OOM errors if you do not undestand what it is for. There is not need to copy the workflow above, just use your own workflow and replace the stock "Load Diffusion Model" with the "Unet Loader (GGUF)" node.

## Installation

> [!IMPORTANT]  
> Make sure your ComfyUI is on a recent-enough version to support custom ops when loading the UNET-only.

To install the custom node normally, git clone this repository into your custom nodes folder (`ComfyUI/custom_nodes`) and install the only dependency for inference (`pip install --upgrade gguf`)

```
git clone https://github.com/RealRebelAI/ComfyUI-GGUF_KREA-2.git
```

To install the custom node on a standalone ComfyUI release, open a CMD inside the "ComfyUI_windows_portable" folder (where your `run_nvidia_gpu.bat` file is) and use the following commands:

```
git clone https://github.com/city96/ComfyUI-GGUF ComfyUI/custom_nodes/ComfyUI-GGUF_KREA-2.git
.\python_embeded\python.exe -s -m pip install -r .\ComfyUI\custom_nodes\ComfyUI-GGUF_KREA-2\requirements.txt
```


