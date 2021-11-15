## TAG Grant Form Similarity

The [Technology Association of Grantmakers (TAG)](https://www.tagtech.org/) is a 501(c)(3) non-profit membership organization that promotes the power of technology to advance the goals of the philanthropic sector.

This repository contains code and steps neccesary to reproduce a list of common fields from the #fixtheform analysis. For more information, the initial press release is [here](https://www.tagtech.org/news/586811/TAG-Publishes-List-of-Common-Grant-Fields-from-FixtheForm-Analysis-.htm).

## Requirements

1. [Github](https://desktop.github.com/)
1. Linux or access to Linux (e.g. within a [Docker container](https://ubuntu.com/tutorials/windows-ubuntu-hyperv-containers#1-overview))
1. [Python3](https://www.python.org/download/releases/3.0/) (with [venv](https://docs.python.org/3/library/venv.html))

## Setup

### Install required dependencies

```console
git clone https://github.com/TAG-repo/grantform-similarity.git
cd grantform-similarity
python3 -m virtualenv venv && venv/bin/pip install -r requirements.txt 
```
