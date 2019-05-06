# Release repository for stratix10

Montavista Software, LLC. release of stratix10. 

How to use:
==========
```
git clone --recursive https://github.com/MontaVista-OpenSourceTechnology/opencgx-intel-2.6
cd opencgx-intel-2.6
source setup.sh
```
Optionally, you can pass setup.sh a directory name to use instead of the
default "project" as follows:

```
source setup.sh <project directory>
```
Note: If you are running setup.sh under another script, you should execute it
as a shell script:

```
bash setup.sh <project directory>
source <project directory>/setup.sh
```
The kernel sources by default will be checked out locally to the sources
directory. If you would rather have bitbake do the checkout run the following
command prior to sourcing setup.sh:

```
export LOCAL_SOURCES=0
```

After running the top level setup.sh, you are ready to build. When starting
another session, you can source the setup.sh script in the project directory
to get started. This script will automatically source the environment for
the build tools stored under buildtools, and sources the 
poky/oe-init-build-env script.

directory layout:
================
```
opencgx-intel-2.6/
       project - bitbake project for the stratix10 project build
       buildtools - build tools to provide minimal build requirement for poky builds
       layers - layers for building stratix10 project
       setup.sh - project setup script
       bin - various helper applications for setting up and maintaining the release directory
```

Verfied machines: stratix10 
