## TAG Grant Form Similarity

The [Technology Association of Grantmakers (TAG)](https://www.tagtech.org/) is a 501(c)(3) non-profit membership organization that promotes the power of technology to advance the goals of the philanthropic sector.

This repository contains code and steps neccesary to reproduce a list of common fields from the #fixtheform analysis. For more information, the initial press release is [here](https://www.tagtech.org/news/586811/TAG-Publishes-List-of-Common-Grant-Fields-from-FixtheForm-Analysis-.htm). You may download the latest dataset release if you are not interested in re-running the data conversion scripts.

## Requirements

1. [Github](https://desktop.github.com/)
1. Ubuntu or access to Ubuntu (e.g. within a [Docker container](https://ubuntu.com/tutorials/windows-ubuntu-hyperv-containers#1-overview))
1. [Python3.8](https://www.python.org/download/releases/3.0/) (`sudo apt install python3.8`)

## Setup

### Install required dependencies

```console
git clone https://github.com/TAG-repo/grantform-similarity.git
cd grantform-similarity
python3.8 -m venv venv && venv/bin/pip install -r requirements.txt
```

### _Quick_ How-to

1. Navigate to the cloned respository. 
1. Run the juypter notebooks on the command line.
1. The final dataset, from the initial sanitized grant fields to the set of grant fields clustered at various cutoffs as well as assigned to one of the 13 themes described in the [technical report](insert link), will be in `./data/processed`.

You can copy and paste the following,
```console
cd grantform-similarity
source venv/bin/activate
# jupyter nbconvert --execute ./notebookds/4.2-kpr-make-low-and-high-cutoff-for-task-4.ipynb
```
