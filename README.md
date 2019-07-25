# data8_platform
Provide basic starting points for setting up a useful local data8 environment


This repo can be found at [https://deculler.github.io/data8_platform/](https://deculler.github.io/data8_platform/)


Build python3.6 based data8 configuration as a virtual env


This will include a large suite (leave off the -y if you want to confirm)

`conda create -n data8 python=3.6 -y anaconda`

Activate it

`conda activate data8`

Install the datascience Tables package in your environment

`pip install datascience`

Or to build it from an environment.yml

```
conda env create -f environment.yml
conda activate data8
```
