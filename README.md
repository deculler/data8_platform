# data8_platform
Provide basic starting points for setting up a useful local environment like that
used in [Data 8](https://data8.org)

The web page for [this repo](https://github.com/deculler/data8_platform) can be found at [https://deculler.github.io/data8_platform/](https://deculler.github.io/data8_platform/)

# Basic Data8 Virtual Environment

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

# Basic Data8 Docker container

The [Dockerfile](Dockerfile) builds a container with [datascience](https://github.com/data-8/datascience) layered over [jupyter/scipy-notebook](https://jupyter-docker-stacks.readthedocs.io/en/latest/using/selecting.html)

Assming that you have docker installed, you can run this with

```
docker run -p 8888:8888 dculler/data8:basic
```

The first time it will cache the container.  When it starts up you'll see something like:

```
http://(565821d7f504 or 127.0.0.1):8888/?token=a404bc0c2afbb285736c490afba69946d7c2ae44eb3dcdbf
```
You can also just do:

```
http://localhost:8888/?token=<token_as_above>
```
Once the server is running, you can just open the URL:

`http://localhost:8888` to conect back to it.

The [RollingDice.ipynb](https://github.com/deculler/data8_platform/blob/master/RollingDice.ipynb)
notebook is in the `work` folder, so you can give that try to test
things out.  You are now running in a virtual machine provided by the
Docker container.  You can use the `upload` button to upload notebooks to
your container.  To download out of the container, select the desired notebook(s)
and click `Download`.



