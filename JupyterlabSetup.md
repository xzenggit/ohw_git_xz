
## Install Anaconda
* Download [Miniconda](https://conda.io/miniconda.html) or [Anaconda](https://www.anaconda.com/download/) 
* Install Anaconda (assume the downloaded package is namaed anaconda)
  * chmod +x anaconda
  * ./anaconda

## Setup Jupyterlab remote access
* generate configruation file: jupyter notebook --generate-config
* set password: jupyter notebook password
* Set SSL for Encrypted Communication if needed: openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout mycert.pem -out mycert.pem
* Do the following in .jupyter/jupyter_notebook_config.py ([Reference](https://agent-jay.github.io/2018/03/jupyterserver/)):
```
# Set options for certfile, ip, password, and toggle off
# browser auto-opening
c.NotebookApp.certfile = u'/absolute/path/to/your/certificate/mycert.pem'
c.NotebookApp.keyfile = u'/absolute/path/to/your/certificate/mycert.pem'
# Set ip to '*' to bind on all interfaces (ips) for the public server
c.NotebookApp.ip = 'your ip address'
c.NotebookApp.password = u'sha1:bcd259ccf...<your hashed password here>'
c.NotebookApp.open_browser = False

# It is a good idea to set a known, fixed port for server access
c.NotebookApp.port = 9999
```
* Start Jupyterlab : jupyter lab
* Copy the address xxxxxxxxxxxxxx from output and paste it in your webbrowser.
```
 The Jupyter Notebook is running at:
 xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```
## Setup your own environment
* create  env_xxx.yml file like:
```
name: testevn
channels:
 - conda-forge
dependencies:
 - python=3.6
 - numpy
 - pip:
  - pyjokes
 ```
 * install the environment: conda env create -f env_xxx.yml
 * activate the environment: conda activate testenv
 * install the new kernal environment: conda activate testenv; ipython kernel install --user --name testenv
 * list all environment: conda env list
 
 
 
