# Symbiflow-Magic
This repository contains a makefile to easily install Symbiflow for the Xilinx 7 Series boards.

## Getting Started
Simply clone the repository and `cd` into it. Then run:
```bash
make
```
It will install `conda` and all other Symbiflow dependencies in the `INSTALL_DIR` path which is in a user's directory rather than system's directory. The default path for installation is:
`~/opt/symbiflow`

After running the `make` command activate your conda environment as follow:
```bash
conda activate $FPGA_FAM
```
Enjoy! now you can use Symbiflow to build completely opensource Arty A7 bitstreams :)

## Quick test
Just to ensure if everything is set-up correctly. Clone the symbiflow-examples repository and change directory into it:
```bash
git clone https://github.com/SymbiFlow/symbiflow-examples.git
cd symbiflow-examples
```

Then move to the `xc7` folder that contains examples for the Xilinx 7 series FPGAs.
```bash
cd xc7
```
Finally run:
```bash
TARGET="arty_35" make -C counter_test
```
__Note:__ Make sure you are inside your conda environment before calling the above command. You will see `(xc7)` written on the left side of your terminal indicating you are inside the environment.

After the command runs you will find the resulting files in the `counter_test/build/arty_35/` folder. 

To deactivate the conda environment run:
```bash
conda deactivate
```

