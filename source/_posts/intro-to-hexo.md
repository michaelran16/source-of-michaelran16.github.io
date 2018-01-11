---
title: Intro to Hexo
date: 2001-01-01 16:11:25
tags:
---

This is an introduction to Hexo blogging framework, used for self references.

# First word

## Public repo and master branch

For GitHub pages deployment, you have to push the __public folder__ of Hexo to the __master branch__ of "yourname.github.io" repo in your GitHub account. 

Make sure the repo name is correct. And "yourname" must match the GitHub account name. 

After "hexo deploy", the changes should be reflected within 5 seconds.

## Config the git URL

Now edit your _config.yml

You must put in the git SSH url in config file.

# Workflow

    hexo init yourname.github.io
    cd 
    npm install
    hexo server
    npm install hexo-deployer-git --save
    vi _config.yml
    hexo generate --watch
    hexo deploy

Specifically, after you update a post, run the following:

    hexo g
    hexo d
    Or
    hexo s

https://gist.github.com/btfak/18938572f5df000ebe06fbd1872e4e39

## Handle Images

Put all your images in "source/images" folder. Put all markdown file in "source/images" folder. Then your image insertion sync looks like this:

    ![](/images/e7a396ad9c53636766c6d89aa840f60d.jpg)

Look like this: ![](/images/e7a396ad9c53636766c6d89aa840f60d.jpg)

## Apply themes

Pick a theme online, for example this one: https://github.com/stkevintan/hexo-theme-material-flow

Then run the following:

    cd /your_blog_dir/
    # install dependencies
    npm i -S hexo-generator-search hexo-generator-feed hexo-renderer-less hexo-autoprefixer hexo-generator-json-content
    # download source
    git clone https://github.com/stkevintan/hexo-theme-material-flow themes/material-flow

Lastly, change the value of theme to material-flow in _config.yml

## Hexo commands abbreviation

    hexo n == hexo new
    hexo g == hexo generate
    hexo s == hexo server
    hexo d == hexo deploy

# The official Hello World

Welcome to [Hexo](https://hexo.io/)! This is your very first post. Check [documentation](https://hexo.io/docs/) for more info. If you get any problems when using Hexo, you can find the answer in [troubleshooting](https://hexo.io/docs/troubleshooting.html) or you can ask me on [GitHub](https://github.com/hexojs/hexo/issues).

## Quick Start

### Create a new post

``` bash
$ hexo new "My New Post"
```

More info: [Writing](https://hexo.io/docs/writing.html)

### Run server

``` bash
$ hexo server
```

More info: [Server](https://hexo.io/docs/server.html)

### Generate static files

``` bash
$ hexo generate
```

More info: [Generating](https://hexo.io/docs/generating.html)

### Deploy to remote sites

``` bash
$ hexo deploy
```

More info: [Deployment](https://hexo.io/docs/deployment.html)
