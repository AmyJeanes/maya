# Transformers Notebooks

This is a collection of notebooks powered by HuggingFace transformers:

Notebooks included:
- [Maya1 TTS Model](https://huggingface.co/maya-research/maya1) (`maya1.ipynb`)
  - The code is based on the [quick start code example](https://huggingface.co/maya-research/maya1#quick-start-generate-voice-with-emotions) modified slightly to work better in a notebook.

This repository is essentially a setup guide for HuggingFace transformers and could be repurposed to run many different things.

# First time setup

## Prerequisites

Make sure Python 3.10+ is installed on your system before running any commands.

The latest CUDA toolkit is installed (if using a Nvidia GPU): https://developer.nvidia.com/cuda-downloads

All commands must be ran in the folder of this repository e.g. `C:\_git\transformers-notebooks`

## Create virtual environment

```
python -m venv .venv
```

## Activate virtual environment

## Windows

### PowerShell

```
. .venv\Scripts\Activate.ps1
```

### Command Prompt
```
.venv\Scripts\activate.bat
```

## Install dependencies

### Install UV package manager for speed

```
pip install uv
```

Note: You might get a warning from VS Code saying the package may have been installed to the global environment. This is wrong if you have activated the virtual environment correctly, so you can ignore this warning.

### Install PyTorch

If using a Nvidia GPU for acceleration, run `nvidia-smi` in a terminal to check your CUDA version. It should be listed at the top right, e.g. `CUDA Version: 13.0`, for example:

```
> nvidia-smi
Tue Nov 25 16:17:41 2025
+-----------------------------------------------------------------------------------------+
| NVIDIA-SMI 581.80                 Driver Version: 581.80         CUDA Version: 13.0     |
+-----------------------------------------+------------------------+----------------------+
| GPU  Name                  Driver-Model | Bus-Id          Disp.A | Volatile Uncorr. ECC |
| Fan  Temp   Perf          Pwr:Usage/Cap |           Memory-Usage | GPU-Util  Compute M. |
|                                         |                        |               MIG M. |
|=========================================+========================+======================|
|   0  NVIDIA GeForce RTX 5090      WDDM  |   00000000:01:00.0  On |                  N/A |
| 30%   34C    P0             73W /  600W |   10638MiB /  32607MiB |      3%      Default |
|                                         |                        |                  N/A |
+-----------------------------------------+------------------------+----------------------+
```

If this command doesn't work or you cannot see a CUDA version then you have not installed CUDA correctly, but PyTorch can still run on CPU if you can't use an Nvidia GPU.

Go to https://pytorch.org/get-started/locally/ and pick the appropriate CUDA platform for your system e.g. CUDA 13.0 and run the install command provided, e.g. for CUDA 13.0:

```
python -m uv pip install torch torchvision --index-url https://download.pytorch.org/whl/cu130
```

### Install other dependencies

```
python -m uv pip install -r requirements.txt
```

## Usage

Open this repository folder in VSCode and open the notebook you wish to try.

Make sure the virtual environment is selected as the interpreter (top right corner). It may say `Select Kernel` if nothing is active:

![Select Kernel](images/select_kernel_1.png)

![Select Kernel](images/select_kernel_2.png)

![Select Kernel](images/select_kernel_3.png)

Instructions for each notebook will be contained within it, but essentially just run the code cells in order.

If you want to run anything on the command line, make sure to activate the virtual environment first as above.
