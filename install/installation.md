# Anaconda and Miniconda

Anaconda and Miniconda are two popular distributions for the Python programming language and its associated packages and tools. While Anaconda comes pre-installed with a vast collection of packages for data science, machine learning, and scientific computing, Miniconda provides a minimal installation that allows you to install only the packages you need.

## Installing Anaconda

Anaconda is a free, open-source distribution that includes Python, the conda package manager, and a collection of pre-installed packages for data science, machine learning, and scientific computing. Here's how you can install Anaconda on your system:

1. Visit the official Anaconda website: https://www.anaconda.com/products/distribution
2. Download the Anaconda installer for your operating system (Windows, macOS, or Linux).
3. Run the installer and follow the on-screen instructions.
4. (Optional) During the installation process, you can choose to add Anaconda to your system's PATH environment variable. This will allow you to use conda commands from any directory in your terminal or command prompt.
5. After the installation is complete, you may need to restart your terminal or command prompt for the changes to take effect.
6. To verify the installation, open your terminal or command prompt and type `conda --version`. If the installation was successful, you should see the version of Conda displayed.

## Installing Miniconda

Miniconda is a lightweight, minimal installer for the Conda package manager. It does not come pre-installed with any packages, but it allows you to create a minimal base environment and then install only the packages you need for your specific project. Here's how you can install Miniconda:

1. Visit the official Miniconda website: https://docs.conda.io/en/latest/miniconda.html
2. Download the Miniconda installer for your operating system (Windows, macOS, or Linux).
3. Run the installer and follow the on-screen instructions.
4. (Optional) During the installation process, you can choose to add Miniconda to your system's PATH environment variable. This will allow you to use conda commands from any directory in your terminal or command prompt.
5. After the installation is complete, you may need to restart your terminal or command prompt for the changes to take effect.
6. To verify the installation, open your terminal or command prompt and type `conda --version`. If the installation was successful, you should see the version of Conda displayed.

Once you have installed either Anaconda or Miniconda, you can start using the `conda` package manager to create new environments, install packages, and manage your Python installations and packages.

For more detailed instructions and troubleshooting, please refer to the official Anaconda and Miniconda documentation.


## Installing Miniconda and PyTorch (Only for Mac users)

1. Go to the official Miniconda website: https://docs.conda.io/en/latest/miniconda.html

2. Download the Miniconda installer for your Mac computer.

3. After installing Miniconda, we will first install Jupyter, which is a code editor that we will use in this course. Open your terminal and run the following command:

```
conda install -y jupyter
```

4. Now, let's create our environment from a YAML file (a file that contains instructions for setting up the environment). Depending on your Mac's processor and whether you have a NVIDIA CUDA GPU or not, run one of the following commands:

- **For Mac M1/M2 processors**: `conda env create -f torch-conda.yml`
- **For NVIDIA CUDA GPU**: `conda env create -f torch-cuda.yml`
- **For CPU only (no GPU)**: `conda env create -f torch.yml`

5. To start using this new environment, you need to activate it by running the following command:

```
conda activate torch
```

6. Next, we need to register our PyTorch environment. Make sure you have activated the `torch` environment by running the `conda activate torch` command. Then, run the following command to register the environment:

```
python -m ipykernel install --user --name pytorch --display-name "Python 3.11 (torch)"
```

7. Testing your Environment: You can now start Jupyter Notebook by running the following command:

```
jupyter notebook
```

8. In the Jupyter Notebook, you can run the following code to check that you have the expected versions of the packages installed:

```python
import torch
print(f"PyTorch version: {torch.__version__}")

import numpy
print(f"NumPy version: {numpy.__version__}")
```

This code will print the versions of PyTorch and NumPy that are installed in your environment. If you see the expected versions, then your environment is set up correctly.

By following these simple steps, you should be able to install Miniconda and PyTorch on your Mac, create and activate the necessary environment, and start using Jupyter Notebook for your work.
