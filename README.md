# ohw_git_xz
This is a repository for Oceanhackweek notes.


## Git tutorial

* Download code: git clone repo_address
* See history: git log
* Check status: git status
* Add changes: git add README.md
* Add change logs: git commit -m "some changing message"
* Push changes to repo: git push origin master
* See difference between current status and last commit: git diff
* See difference after git add commends: git diff --staged
* See remote repo address: git remote -v
* Add collaborators: Settings -> Collaborators
* Get latest updates from repo:git pull origin master
* Remove origin at local: git remote rm origin
* Add your own copy of the original repo: git remote add upstream the_original_repo
* Add your own forked copy: git remote add origin your_fork_repo
* Check branches list: git remote -v
* Pull from your forked repo: git pull origin master
* Pull from original repo: git pull upstream master


Git tutorials: 
* https://swcarpentry.github.io/git-novice/
* https://www.atlassian.com/git/tutorials

## Conda notes

Conda commands:
* conda info
* conda list

Create conda environment:
* create environment.yml file like:
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
* install the environment: conda env create -f environment.yml
* activate the environment: conda activate testenv
* install the new kernal environment: conda activate testenv; ipython kernel install --user --name testenv
* list all environment: conda env list

## AWS cloud computing

* sudo apt update
* sudo apt upgrade
* install aws commandline: sudo apt install awscli
* list all buckets: aws s3 ls
* make a bucket: aws s3 mb s3://ohwxzenggit
* sync a bucket: aws s3 sync s3://oceanhackweek2018 s3://ohwxzenggit


## Useful websites

* OOI website: www.oceanobservatories.org
* OOI Arrays: http://ooi.visualocean.net/
* Jupyterhub: https://jupyterhub.oceanhackweek.org/hub/home
* Oceanhackweek tutorials: https://github.com/oceanhackweek/ohw2018_tutorials
* OOI Data Workshops: https://github.com/ooi-data-review/2018-data-workshops
* library to build batch requests: https://github.com/kerfoot/uframe-m2m
* IOOS: https://ioos.us
* IOOS code demos: http://ioos.github.io/notebooks_demos/code_gallery/
* Altair tutorial (data visulization): https://github.com/altair-viz/altair-tutorial
* Anothe data portal: https://cchdo.ucsd.edu
* For notebooks: https://mybinder.org

## ideas
* 3D plots with Bokeh to show all data for certain OOI site (e.g. Poineer Array)
* Time series analysis (implimentation)
* Predict ocean chemical variables from physical variables.

## Pangeo tutorials
* Xarray tutorial: https://github.com/jhamman/xarray_tutorial
* Use binder.pangeo.io to open the above url.

## Project notes

### Setup conda environments first

* create ohw_env_ml.yml file
* install the environment: conda env create -f ohw_env_ml.yml
* activate the environment: source activate ohw_env_ml

### About OOI data QC
* https://oceanobservatories.org/quality-control/









