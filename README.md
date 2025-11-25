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
