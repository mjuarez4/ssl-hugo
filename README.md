# SSL Hugo Website

> The SSL website, now powered by Hugo!

[![github pages](https://github.com/LoyolaChicagoCS/ssl-hugo/actions/workflows/deploy.yml/badge.svg)](https://github.com/LoyolaChicagoCS/ssl-hugo/actions/workflows/deploy.yml)

## Table of Contents

- [SSL Hugo Website](#ssl-hugo-website)
  - [Table of Contents](#table-of-contents)
  - [About](#about)
  - [Development Requirements](#development-requirements)
  - [Deployment](#deployment)
  - [Maintenance](#maintenance)
    - [How to Update the Home Page](#how-to-update-the-home-page)
    - [How to Add People](#how-to-add-people)
    - [How to Add Publications](#how-to-add-publications)

## About

This repository contains the [Software and Systems Laboratory (SSL) website](https://ssl.cs.luc.edu)
source code.

This website is powered by the [`hugo` static site generator](https://gohugo.io) and the [Wowchemy Research Group theme](https://github.com/wowchemy/starter-hugo-research-group).

## Development Requirements

To develop this site, you will need to have installed:

- `hugo`
- `golang`
- `Python 3.10`
- [`academic`](https://pypi.org/project/academic/) Python utility

To install these with `homebrew`, run:

```shell
brew install hugo golang python@3.10
brew link python@3.10
python3.10 -m pip install --upgrade pip
python3.10 -m pip install academic
```

## Deployment

This site is deployed once per commit via GitHub Actions.

## Maintenance

> How to be a good maintainer

### How to Update the Home Page

1. Work within the [`./content/home`](content/home/)
2. Create new markdown (`.md`) files for each section of the document OR edit an existing section's `.md` file.

### How to Add People

1. Work within the [`./content/people`](content/people)
2. Copy an existing person's directory and change the name to the name of the new individual to add
3. Edit the new person's `_index.md` file and add the appropriate details
4. Replace the new person's `avatar.jpg` file with a headshot of the individual.

### How to Add Publications

1. Run the following command block

```shell
python3.10 -m venv env
source env/bin/activate
python3.10 -m pip install --upgrade pip
python3.10 -m pip install -r requirements.txt
```

1. Then run the following command, replacing `$BIB with the path to your bib file

```shell
./addPublications.bash $BIB
```
