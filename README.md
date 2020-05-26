This repository contains natvis files for Qt5, as provided by Qt's Visual Studio Tools Add-In.

Debugging with Visual Studio Code
=================================

* Clone this repo or just download ``qt5.natvis.xml`` directly using [this link](https://raw.github.com/aambrosano/qt-natvis/master/qt5.natvis.xml).

* Update your launch configurations on Visual Studio Code to include this line:

    ```"visualizerFile": "/path/to/qt5.natvis.xml"```

You can find more about how to use Visual Studio Code for Qt development on [KDAB](https://kdab.com)'s website:
* [Overview](https://www.kdab.com/using-visual-studio-code-for-writing-qt-applications/)
* Technical guide: [Part 1](https://www.kdab.com/using-visual-studio-code-for-qt-apps-pt-1/)

Using Qt with a custom namespace name
=====================================

If you built or are using a custom Qt version with a customized namespace, just replace ``##NAMESPACE##`` with the namespace name in ``qt5.natvis.orig.xml`` with your favourite string manipulation tool.

For example using sed:

  ```sed s/##NAMESPACE##/mynamespace/ qt5.natvis.orig.xml > qt5.natvis.mynamespace.xml```