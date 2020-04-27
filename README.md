# cfDNApipe

[![Build Status](https://travis-ci.org/pages-themes/minimal.svg?branch=master)](https://travis-ci.org/pages-themes/minimal) [![Gem Version](https://badge.fury.io/rb/jekyll-theme-minimal.svg)](https://badge.fury.io/rb/jekyll-theme-minimal)

cfDNApipe(<u>C</u>ell <u>F</u>ree <u>DNA</u> <u>Pipe</u>line) is an integrated pipeline for analyzing [cell-free DNA](https://en.wikipedia.org/wiki/Circulating_free_DNA) WGBS/WGS data. It contains many cfDNA quality control and feature extration algorithms. Also we collected some useful cell free DNA references and provide them [here](https://honchkrow.github.io/cfDNAReferences/).

The whole pipeline was established based on processing graph principle. Users can use the inside integrated pipeline for WGBS/WGS data as well as build their own analysis pipeline from any intermediate data like bam files. The main functions are as the following picture.

![cfDNApipe Functions](./cfDNApipe_picture1.jpg)

## Section 1: Installation Tutorial

### Section 1.1: System requirement
The popular WGBS/WGS analysis softwares are released on Unix/Linux system, based on different program language, like Bowtie2/Bismark and picard. Therefore, it's very difficult to rewrite all the software in one language. Fortunately, [conda](https://docs.conda.io/en/latest/)/[bioconda](http://bioconda.github.io/) program collected many prevalent python mudules and bioinformatics software, so we can install all the dependencies through [conda](https://docs.conda.io/en/latest/)/[bioconda](http://bioconda.github.io/) and arrange pipelines using python.

We recommend using conda environment and python >= 3.6. If you did not install conda before, please follow [this tutorial](https://docs.conda.io/projects/conda/en/latest/user-guide/install/) to install conda first.

After installation, you can create a new virtual environment for cfDNA analysis. Virtual environment management means that you can install all the dependencies in this virtual environment and delete them easily by removing this virtual environment.

you can create a new virtual environment using the following command:

```shell
# create a conda environment named cfDNApipe with python3.6
conda create -n cfDNApipe python=3.6
# enetr the environment
conda activate cfDNApipe
```

### Section 1.2: Install Dependencies
Please download this repository and put it in your working directory.

```shell
git clone https://github.com/Honchkrow/cfDNApipe.git
```

Then, run the following command and following the instrucion to install the dependencies.

```shell
cd cfDNApipe
chmod +x sysCheck
./sysCheck
```

If your computer fulfills the requirement, you will see the following message.

```shell
The environment configuration is done!
```

### Section 1.3: Install cfDNAipe
Install cfDNApipe module.

```shell
pip install ./dist/cfDNApipe-0.0.4.tar.gz
```
