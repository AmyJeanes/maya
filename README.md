# Maya voice model

This is a sample notebook setup to try out the Maya1 TTS model from https://huggingface.co/maya-research/maya1

# First time setup

Make sure all commands are ran in the folder of this repository e.g. `C:\_git\maya`

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

## Install PyTorch

Run `nvidia-smi` in a terminal to check your CUDA version. It should be listed at the top right, e.g. `CUDA Version: 13.0`, for example:

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

Go to https://pytorch.org/get-started/locally/ and pick the appropriate CUDA platform for your system e.g. CUDA 13.0 and run the install command provided, e.g. for CUDA 13.0:

```
pip install torch torchvision --index-url https://download.pytorch.org/whl/cu130
```

## Install dependencies

```
pip install -r requirements.txt
```

## Usage

Open this repository folder in VSCode and open `main.ipynb`

Make sure the virtual environment is selected as the interpreter (top right corner). It may say `Select Kernel` if nothing is active:

![Select Kernel](images/select_kernel_1.png)

![Select Kernel](images/select_kernel_2.png)

![Select Kernel](images/select_kernel_3.png)

Then run the cells in order to generate audio.

The generated audio files will be displayed and optionally saved in the `output` folder.

If you want to run anything on the command line, make sure to activate the virtual environment first as above.
