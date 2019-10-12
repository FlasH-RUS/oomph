FlasH's eclipse setup
========================

Setting up the installer
------------------------
* In case you're on Windows: just download the installer from here (/eclipse-inst-64.exe) and run it.
* In case you're on a different platform:
  1. Download [eclipse installer](https://wiki.eclipse.org/Eclipse_Installer) and unpack it.
  2. Edit `eclipse-inst.ini` in the unpacked root adding the following line to the very end: `-Doomph.redirection.setups=index:/->https://raw.githubusercontent.com/FlasH-RUS/oomph/master/setups/`

Installing
---------------------------------
1. Once the installer has opened, switch to advanced mode (3-striped button at the top right corner, then "ADVANCED MODE...")
2. Follow the wizard steps, etc. :)

What's included
---------------
1. Eclipse Oxygen/Photon for Java EE developers with the following plugins excluded:
    * Data Tools
    * Remote Systems Explorer (RSE)
    * CloudFoundry support (CFT)
    * Plug-in Development Environment (PDE)
2. Lombok
3. Spring Tools Suite
4. Groovy Eclipse
5. AutoDeriv
6. Optionally - IDEA keymap

Testing
-------

Edit `eclipse-inst.ini` in the installer root directory to use local folder with files to update. E.g. `-Doomph.redirection.setups=index:/->file:/home/flash/git/oomph/setups/`

Dev notes
---------

* How to customize perspective with Oomph: https://www.ibm.com/developerworks/community/wikis/home?lang=en#!/wiki/W0c4a14ff363e_436c_9962_2254bb5cbc60/page/Setting%20perspective%20customization%20with%20Oomph
