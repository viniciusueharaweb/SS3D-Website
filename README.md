# RE:SS3D Website

**This is the website for the RE:SS3D project, located at <https://ss3d.space>.**

Release: [![Build Status](https://travis-ci.org/RE-SS3D/Website.svg?branch=release)](https://travis-ci.org/RE-SS3D/Website)

Develop: [![Build Status](https://travis-ci.org/RE-SS3D/Website.svg?branch=develop)](https://travis-ci.org/RE-SS3D/Website)

Devblog: [![Build Status](https://travis-ci.org/RE-SS3D/Website.svg?branch=devblog)](https://travis-ci.org/RE-SS3D/Website)

## Requirements

- [jekyll](https://jekyllrb.com/docs/installation/)
- [rmagick](https://github.com/rmagick/rmagick)

## Local Setup

### On Linux

Linux is the simplest as it's what these technologies are designed for. Especially ubuntu:

    sudo apt install libmagickwand-dev
    gem install jekyll bundler rmagick
    git clone https://github.com/RE-SS3D/Website
    cd Website
    bundle

### On Windows

On windows you need to use [WSL - Ubuntu](https://www.microsoft.com/en-nz/p/ubuntu-1804-lts/9n9tngvndl3q?rtc=1&activetab=pivot:overviewtab). The instructions below are based on the [jekyll WSL instructions](https://jekyllrb.com/docs/installation/windows/) and [rmagick install instructions](https://github.com/rmagick/rmagick).

Once ubuntu is downloaded, open up powershell or command prompt, or directly open ubuntu (and skip the first line).

    bash
    sudo apt update -y && sudo apt upgrade -y
    sudo apt-add-repository ppa:brightbox/ruby-ng
    sudo apt-get update
    sudo apt install ruby2.5 ruby2.5-dev build-essential dh-autoreconf libmagickwand-dev
    sudo gem update
    sudo gem install jekyll bundler rmagick
    sudo bundle install

Enter each line one by one, the whole process might take a while.
You can confirm jekyll is installed by entering:

    jekyll -v

Finally, whenever you want to run the website, open bash and navigate to the folder in which this repo is cloned,
then follow the next section.

*Hint: you can easily open ubuntu at a desired folder by opening the folder, shift-right clicking on an empty section in the folder with nothing selected, and selecting 'Open PowerShell window here', then typing `bash` into the prompt.*

## Running local website

    bundle exec jekyll serve

Add:

- `--watch` for automatically rebuilding site for any changes.
- `--host 0.0.0.0` to make server listen on all IPs, to allow for mobile testing.
- `--future` if you are testing a blog post with a date in the future.

Website should be accessible at <http://localhost:4000/>

## Creating the Devblog

A template for the devblog's .md file exists at [./_drafts/devblog-format.md](./_drafts/devblog-format.md), that you can fill in with details. A checklist regarding the process of the devblog can be found [on our management board](https://trello.com/c/jLB9dKJH).
