# Anaconda and Miniconda Installation Guide

## Table of Contents

1. [Introduction](#introduction)
2. [Installing Anaconda](#installing-anaconda)
   - [Windows](#windows)
   - [macOS](#macos)
3. [Installing Miniconda](#installing-miniconda)
   - [Windows](#windows-1)
   - [macOS](#macos-1)
4. [Creating a New Environment](#creating-a-new-environment)
5. [Testing Your Environment](#testing-your-environment)


## Introduction

Anaconda and Miniconda are two popular distributions for the Python programming language and its associated packages and tools. This guide will walk you through the installation process for both distributions, as well as the steps to create and test a new environment.

Anaconda comes pre-installed with a vast collection of packages for data science, machine learning, and scientific computing, making it a great choice for those working in these fields. Miniconda, on the other hand, provides a minimal installation that allows you to install only the packages you need, which can be beneficial for users with limited disk space or specific project requirements.

> **Note:** Depending on your use case and preferences, you may choose to install either Anaconda or Miniconda. Anaconda is a more comprehensive solution, while Miniconda offers a lightweight and customizable option.

## Installing Anaconda

Anaconda is a free, open-source distribution that includes Python, the conda package manager, and a collection of pre-installed packages for data science, machine learning, and scientific computing.

### Windows

1. Visit the official Anaconda website: https://www.anaconda.com/products/distribution
2. Download the Anaconda installer for Windows.
3. Run the installer and follow the on-screen instructions.
4. (Optional) During the installation process, you can choose to add Anaconda to your system's PATH environment variable. This will allow you to use conda commands from any directory in your terminal or command prompt.
5. After the installation is complete, you may need to restart your terminal or command prompt for the changes to take effect.
6. To verify the installation, open your terminal or command prompt and type `conda --version`. If the installation was successful, you should see the version of Conda displayed.

### macOS

1. Visit the official Anaconda website: https://www.anaconda.com/products/distribution
2. Download the Anaconda installer for macOS.
3. Run the installer and follow the on-screen instructions.
4. (Optional) During the installation process, you can choose to add Anaconda to your system's PATH environment variable. This will allow you to use conda commands from any directory in your terminal.
5. After the installation is complete, you may need to restart your terminal for the changes to take effect.
6. To verify the installation, open your terminal and type `conda --version`. If the installation was successful, you should see the version of Conda displayed.

## Installing Miniconda

Miniconda is a lightweight, minimal installer for the Conda package manager. It does not come pre-installed with any packages, but it allows you to create a minimal base environment and then install only the packages you need for your specific project.

### Windows

1. Visit the official Miniconda website: https://docs.conda.io/en/latest/miniconda.html
2. Download the Miniconda installer for Windows.
3. Run the installer and follow the on-screen instructions.
4. (Optional) During the installation process, you can choose to add Miniconda to your system's PATH environment variable. This will allow you to use conda commands from any directory in your terminal or command prompt.
5. After the installation is complete, you may need to restart your terminal or command prompt for the changes to take effect.
6. To verify the installation, open your terminal or command prompt and type `conda --version`. If the installation was successful, you should see the version of Conda displayed.

### macOS

1. Visit the official Miniconda website: https://docs.conda.io/en/latest/miniconda.html
2. Download the Miniconda installer for macOS.
3. Run the installer and follow the on-screen instructions.
4. (Optional) During the installation process, you can choose to add Miniconda to your system's PATH environment variable. This will allow you to use conda commands from any directory in your terminal.
5. After the installation is complete, you may need to restart your terminal for the changes to take effect.
6. To verify the installation, open your terminal and type `conda --version`. If the installation was successful, you should see the version of Conda displayed.

## Creating a New Environment

After installing Anaconda or Miniconda, you can create a new environment for your project. This will allow you to manage packages and dependencies separately from your base installation.

1. Open your terminal or command prompt.
2. Run the following command to create a new environment named `torch`:

```
conda create --name torch
```

3. To activate the new environment, run:

```
conda activate torch
```

You can now install any packages you need for your project within this environment without affecting your base installation.

## Testing Your Environment

To ensure that your environment is set up correctly, you can run the following commands:

1. Start Jupyter Notebook by running:

```
jupyter notebook
```

2. In the Jupyter Notebook, you can run the following code to check the versions of the packages installed:

```python
import sys
print(f"Python version: {sys.version}")

import numpy
print(f"NumPy version: {numpy.__version__}")
```

If you see the expected versions of Python and NumPy, your environment is set up correctly.

Please refer to the official documentation of these package managers for more
