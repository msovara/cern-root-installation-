# Installing ROOT in a Python Virtual Environment on LENGAU


## 1. Access LENGAU and Connect via SSH
- First, sign in to **LENGAU** and establish an SSH connection to the **dtn** node.

## 2. Initialize Conda (if needed)
- Ensure your **base Conda environment** is initialized:
  - If it is initialized, you should see `(base)` next to your user ID.  
  - This means your `.bashrc` file has been modified to load Conda automatically.
- If Conda is not initialized, follow the steps in the [CHPC Python Guide](https://wiki.chpc.ac.za/guide:python?s[]=*python*).

## 3. Prepare the Shell and Load Required Modules
- Purge any loaded modules and load the **BIOMODULES** module:
  ```bash
  module purge
  module add chpc/BIOMODULES

## 4. Create a New Conda Environment with ROOT
- Use the following command to create a new Conda environment named `root_env` with ROOT preinstalled:
  ```bash
  conda create -n root_env root -c conda-forge
- The installation time may vary; it typically takes 3–5 minutes.

## 5. Verify the Installation
- List all available environments to confirm the path to your new environment:
  ```bash
  conda info --envs
- Check if the ROOT package was installed by listing the installed packages
  ```bash
  conda list
  
## 6. Activate the ROOT Environment
- Activate the root_env environment using:
  ```bash
  conda activate root_env

 ## 7. Launch ROOT
- Start ROOT with the following command:
  ```bash
  root

## 8. Deactivate the Environment
- When done, deactivate the environment with:
  ```bash
  conda deactivate

This guide ensures a smooth installation of ROOT using a Conda-managed virtual environment on LENGAU. If you encounter any issues, feel free to reach out for support: msovara@csir.co.za
