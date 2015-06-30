# Guitester
Testing platform for eucaconsole - the graphical user interface of eucalyptus. 

## Introduction

Guitester is a testing framework for eucaconsole implemented with python selenium bindings. To use the framework you will need an instance of [Local](https://github.com/eucalyptus/guitester/wiki/Launching-local-Selenium-WebDriver-server) or [Remote Selenium Webdriver](https://github.com/eucalyptus/guitester/wiki/Setting-up-Remote-Selenium-Webdriver,-VNC-server-and-Firefox-on-Centos-6).


## Configuring your environment

### On Centos 6

`yum check ipython`

 `yum -y install ipython git`

 `sudo easy_install selenium`

 `git clone https://github.com/eucalyptus/guitester`

### On Mac

You need to install python and selenium. 

To install python you can use Homebrew with the following command:
`$ ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)" `
[Help](http://docs.python-guide.org/en/latest/starting/install/osx/)

`easy_install selenium`

It is a general best practice to use Virtualenv to create your environment:

`sudo easy_install virtualenv`

`virtualenv guitester_env`

`cd guitester_env/bin; source activate`





## Getting started

`git clone https://github.com/eucalyptus/guitester`

`cd guitester/guitester`

`ipython`

`from guitester.guiec2 import GuiEC2`

for local webdriver:

`tester = GuiEC2(<console URL>)`

for remore webdriver:

`tester = GuiEC2(<Remote Webdriver i.e. "http://10.111.80.115:4444/wd/hub">,<console URL>)`

This will launch a copy of firefox browser and open eucaconsole.

By typing `tester.` and tabbing out you can see all command options.
