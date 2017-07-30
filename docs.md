---
layout: page
title: Package Documentation
---

# What is Project Retina?
Scientists often take measurements of cell densities across the rear surface of the eye (the retina), to better understand how an animal's vision works, changes, develops, or evolves.

This project was started in 2013 to
- improve the statistical rigor of analyses
- enhance replicability of published retinal mapping research
- reduce the barrier to entry of this research field.

# Getting Started:

## 1. Install on your computer

##### Mac
[Install R 3.1.2](http://cran.r-project.org/bin/macosx/ "Mac OS X")  
[Install Xcode](https://itunes.apple.com/us/app/xcode/id497799835?mt=12#)  

Run commands line by line in the Terminal:
```bash
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
brew install gtk+
export PKG_CONFIG_PATH=/usr/X11/lib/pkgconfig:$PKG_CONFIG_PATH
brew install caskroom/cask/brew-cask
brew cask install xquartz
xcode-select --install
```

##### Windows
[Install R 3.1.2](http://cran.r-project.org/bin/windows/base/ "Windows")
[Install RTools](http://cran.r-project.org/bin/windows/Rtools/ "Windows")

##### Linux
```bash
sudo apt-get -y build-dep libcurl4-gnutls-dev
sudo apt-get -y install libcurl4-gnutls-dev
sudo apt-get -y install libglu1-mesa-dev
sudo apt-get -y install r-base-core r-base r-cran-rgl libgtk2.0-dev
```



## 2. Set up packages in R
```R
install.packages(c("cairoDevice", "RGtk2", "devtools", "retistruct"), type="source")
install.packages('devtools')
devtools::install_github('briancohn/retina')
devtools::install_github('bcohn12/retina')
```
## 3. Run a demo to make a map!
```R
library(retina)
retinaplot(Pmol_753)
```
