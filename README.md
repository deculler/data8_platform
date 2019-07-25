# data8_platform
Provide basic starting points for setting up a useful local environment like that
used in [Data 8](https://data8.org)

The web page for [this repo](https://github.com/deculler/data8_platform) can be found at [https://deculler.github.io/data8_platform/](https://deculler.github.io/data8_platform/)

Build python3.6 based data8 configuration as a virtual env

To build it from an environment.yml

```
conda env create -f environment.yml
conda activate data8
```

To do it manually.
(This will include a large suite (leave off the -y if you want to confirm)

`conda create -y -n data8 python=3.6 pip anaconda jupyterlab`

Activate it

`conda activate data8`

Install the datascience Tables package in your environment

`pip install datascience`

To try it out in the local directory

`jupyter notebook`

Once it opens up in your browser, open `RollingDice.ipynb`.  It shows some
simple use of datascience Tables, complete with interactive widgets.

To remove your data8 environment

`conda env remove --name data8`
