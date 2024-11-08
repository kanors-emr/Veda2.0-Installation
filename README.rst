Veda2.0 is a data handling system for The Integrated MARKAL-EFOM System (TIMES) - a bottom-up optimization model for energy-environment systems. We are in the process of enabling support for other models like OSeMOSYS and TEMOA.

It is a Windows application (C#.NET/PostgreSQL). We don't have many users on Mac, but it can work under Windows emulators.

`YouTube videos <https://www.youtube.com/playlist?list=PLED97cPMXPOm60xOKSwvmXaGIsQrjoM8Y>`_

Hardware/software requirement
=============================
Veda2.0 works on Windows portables, desktops, servers, and VMs, with Windows 8/Windows server 2012 or above. Microsoft Excel is no longer a prerequisite for Veda operations, starting version 3, but all input data resides in Excel files. Hardware needed depends on the size and complexity of models,
but here is a configuration suitable for typical TIMES models under Veda2.0:

* CPU: Minimum 4 cores are recommended for STANDARD and ADVANCED licenses. 8 - 16 would be desirable for working with larger models.
* RAM: 4-8 GB is enough for Veda, but GAMS needs more RAM for larger models. 32 GB would accomodate most models.
* HDD: 500GB - 1TB free space for Veda and GAMS files.

Installation
=============

There are two ways to setup Veda2.0. Localhost is the preferred approach as version upgrades are much easier and the previous version can be retained. Two versions cannot be used concurrently though - the application should be closed before launching a different version.

* Localhost: This just needs to be extracted

  * `Download and install prerequisites. <https://github.com/kanors-emr/Veda2.0-Installation/tree/master/Localhost%20Version%20Prerequisites>`_
  * `Download localhost. <https://github.com/kanors-emr/Veda2.0-Installation/releases/download/v4.0.0.0/Veda2.0_localhost_4.0.0.0.7z>`_
  * Give full read and write permissions to the folder where it is extracted.
  * Open port 65001.
        
* Installer: This is a setup executable

  * `Download installer. <https://github.com/kanors-emr/Veda2.0-Installation/releases/download/v4.0.0.0/Veda2.0.Setup.4.0.0.0.exe>`_
  * Create a folder where you wish to install and give it full read and write permissions.
  * Open port 65000.

For detailed installation instructions, `see documentation. <https://veda-documentation.readthedocs.io/en/latest/pages/Getting%20started.html#installation>`_

Final release of major version 2.20
===================================
  * `Download <https://github.com/kanors-emr/Veda2.0-Installation/releases/tag/v2.20.2.1>`_

Links
=====
.. raw:: html

    <ul>
    <li><a href="https://veda-documentation.readthedocs.io/en/latest/pages/Getting%20started.html#installation" target="_blank">Installation video</a></li>
    <li><a href="https://veda-documentation.readthedocs.io/en/latest/pages/Getting%20started.html#licensing" target="_blank">Getting a trial license </a></li>
    <li><a href="https://veda-documentation.readthedocs.io/en/latest/pages/Migration.html#migrating-to-veda-2-0" target="_blank">Migrating to Veda 2.0</a></li>
    <li><a href="https://veda-documentation.readthedocs.io/en/latest/pages/version_history.html" target="_blank">Version history</a></li>
    <li><a href="http://veda-documentation.rtfd.io/" target="_blank">Documentation </a></li>
    <li><a href="https://www.kanors-emr.org/Veda2Users/Index.html" target="_blank">Veda users around the World </a></li>
    </ul>

