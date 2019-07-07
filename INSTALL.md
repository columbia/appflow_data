# AppFlow installation guide

Install dependencies
====================

* Install packages.

    `apt install libleptonica-dev tesseract-ocr libtesseract-dev xdotool imagemagick pip3`

* Install an android emulator, such as Genymotion.


Install python libs
====================

* Install required python libraries.

    `pip3 install scikit-learn scikit-image websocket-client tesserocr progressbar pyyaml selenium`

Notice: tesserocr may not be available on windows.

System Config
=============

* Copy *src/config.py.default* to *src/config.py* and customize it.
* Edit *etc-<category>/params.txt* to suit your needs.

Device setup
============

* Create a virtual device, install ARM translation layer, and GApps.

* Run

    `scripts/setup.sh <device serial>`

  to setup device.

Test
====

* Run

    `src/cui.py <app name> --serial <device serial>`

  to test. Check the screenshots in `tmp/` to verify that the screen capture feature is working.

Collect APKs
============

* Put apk files in *apks/*.

Make directories
================

* Make some temprary directories.

    `mkdir stat tmp model-<category>`
