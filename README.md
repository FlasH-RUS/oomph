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
1. Follow the wizard steps, etc. :)
1. After installation you may still need to do several manual steps like:
    * Switch perspective to "Dev" (which is anyway set to default already).
    * Switch keyboard layout to IntelliJ (Preferences -> General -> Keys) even if you've selected it during setup.

What's included
---------------
1. Eclipse Oxygen/Photon/2018-09/2018-12/2019-03/2019-06/2019-09 for Java EE developers with the following plugins excluded:
    * CloudFoundry support (CFT)
    * Plug-in Development Environment (PDE)
1. Lombok support (asks for lombok.jar during setup anyway)
1. Spring Tools Suite
1. Optionally - IDEA keymap

Testing
-------

Edit `eclipse-inst.ini` in the installer root directory to use local folder with files to update. E.g. `-Doomph.redirection.setups=index:/->file:/home/flash/git/oomph/setups/`

Dev notes
---------

* Perspective customization:
    1. Customize your perspective.
    1. Export Eclipse preferences to epf file: File -> Export -> Preferences.
    1. Open epf file and find the perspective key: `/instance/org.eclipse.ui.workbench/<perspective name>_1_e4persp`.
    1. Convert key value to plain XML:
        * Unescape. E.g. using https://www.freeformatter.com/java-dotnet-escape.html
        * Minify. E.g. with Atom.
    1. Save the same key with plan XML as value in Oomph setup.
