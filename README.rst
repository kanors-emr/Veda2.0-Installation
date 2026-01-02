.. image:: https://img.shields.io/github/v/release/kanors-emr/Veda2.0-Installation?style=flat&color=0078D4
   :target: https://github.com/kanors-emr/Veda2.0-Installation/releases/latest
   :alt: Latest Release
.. image:: https://img.shields.io/github/downloads/kanors-emr/Veda2.0-Installation/total?style=flat&color=28A745
   :target: https://github.com/kanors-emr/Veda2.0-Installation/releases
   :alt: Total Downloads
.. image:: https://img.shields.io/badge/platform-Windows-0078D6?style=flat&logo=windows
   :alt: Platform
.. image:: https://img.shields.io/badge/docs-readthedocs-8CA1AF?style=flat&logo=readthedocs
   :target: https://veda-documentation.readthedocs.io/
   :alt: Documentation

========
Veda 2.0
========

**The Complete Data Management Solution for Energy System Models**

Veda 2.0 is a powerful data handling system for `The Integrated MARKAL-EFOM System (TIMES) <https://iea-etsap.org/index.php/etsap-tools/model-generators/times>`_ — a bottom-up optimization model for energy-environment systems. Support for additional models like **OSeMOSYS** and **TEMOA** is currently in development.

Built with C#.NET and PostgreSQL, Veda 2.0 runs natively on Windows and can operate on Mac via Windows emulators.

.. image:: https://img.shields.io/badge/Watch-Tutorial_Videos-FF0000?style=flat&logo=youtube
   :target: https://www.youtube.com/playlist?list=PLED97cPMXPOm60xOKSwvmXaGIsQrjoM8Y
   :alt: YouTube Tutorials
   :align: center

----

📋 Table of Contents
====================

- `What is Veda 2.0?`_
- `Key Components`_
- `System Requirements`_
- `Installation`_
- `Post-Installation Setup`_
- `Quick Start`_
- `Licensing`_
- `Legacy Versions`_
- `Documentation`_
- `Troubleshooting`_
- `Support`_

----

What is Veda 2.0?
==================

Philosophy and Core Principles
-------------------------------

Veda 2.0 is designed around three core principles:

1. **Data-Driven Workflow**: Excel-based templates connect to a robust PostgreSQL database, enabling version control, multi-user collaboration, and data validation
2. **Transparency**: Complete visibility into model structure, data transformations, and GAMS code generation
3. **Efficiency**: Streamlined workflows from data entry to results visualization, reducing time from hours to minutes

For detailed philosophy and architecture, see the `Introduction <https://veda-documentation.readthedocs.io/en/latest/pages/introduction.html>`_.

Key Enhancements Over Legacy Veda
----------------------------------

- **No Excel Dependency**: Microsoft Excel is no longer required for Veda operations (v3+)
- **PostgreSQL Backend**: Robust database replacing Access for better performance and scalability
- **Modern Architecture**: C#.NET application with web-based interface
- **Enhanced Visualization**: Advanced charting including Sankey diagrams
- **GAMS Engine Integration**: Cloud-based model runs and distributed solving
- **Improved Performance**: Faster synchronization and result processing

Read more about `key enhancements <https://veda-documentation.readthedocs.io/en/latest/pages/introduction.html#key-enhancements-over-the-legacy-version>`_.

----

Key Components
==============

Veda 2.0 provides a comprehensive toolkit for TIMES modeling:

**Navigator**
  Hierarchical browsing of model structure with scenario management, data filtering, and synchronization. The `Navigator <https://veda-documentation.readthedocs.io/en/latest/pages/Navigator.html>`_ is your central hub for model exploration.

**VEDA Tags**
  Powerful Excel-based templating system for defining technologies, commodities, and parameters. Learn about `VEDA Tags <https://veda-documentation.readthedocs.io/en/latest/pages/VedaTags.html>`_ and transformation rules.

**Browse & Items Detail**
  Explore model elements with detailed parameter views and relationships. See `Browse <https://veda-documentation.readthedocs.io/en/latest/pages/Browse.html>`_ and `Items Detail <https://veda-documentation.readthedocs.io/en/latest/pages/Items%20detail.html>`_.

**Run Manager**
  Submit model runs, manage GAMS execution, and organize output files. The `Run Manager <https://veda-documentation.readthedocs.io/en/latest/pages/Run_Manager.html>`_ supports batch processing and GAMS Engine integration.

**Results & Reports**
  Import optimization results and create custom visualizations with interactive charts and Sankey diagrams. Explore `Results <https://veda-documentation.readthedocs.io/en/latest/pages/Results.html>`_ and `Reports <https://veda-documentation.readthedocs.io/en/latest/pages/Reports.html>`_.

**Model Info**
  Access TIMES attributes, VEDA tags reference, and model metadata. See `Model Info <https://veda-documentation.readthedocs.io/en/latest/pages/Model%20Info.html>`_.

----

System Requirements
===================

Veda 2.0 runs on Windows portables, desktops, servers, and VMs with **Windows 8 / Windows Server 2012** or above.

.. note::
   Starting from **version 3**, Microsoft Excel is no longer required for Veda operations. However, all input data still resides in Excel files.

Hardware Recommendations
------------------------

The configuration below is suitable for typical TIMES models:

+-----------+-----------------------------------+--------------------------------------------+
| Component | Minimum                           | Recommended                                |
+===========+===================================+============================================+
| **CPU**   | 4 cores (Standard/Advanced)       | 8–16 cores for larger models               |
+-----------+-----------------------------------+--------------------------------------------+
| **RAM**   | 4–8 GB for Veda                   | 32 GB (accommodates GAMS for large models) |
+-----------+-----------------------------------+--------------------------------------------+
| **HDD**   | 500 GB free space                 | 1 TB for Veda and GAMS files               |
+-----------+-----------------------------------+--------------------------------------------+

For complete requirements, see `Hardware/software requirement <https://veda-documentation.readthedocs.io/en/latest/pages/Getting%20started.html#hardware-software-requirement>`_.

----

Installation
============

There are two ways to set up Veda 2.0:

.. list-table::
   :header-rows: 1
   :widths: 20 40 40

   * - Method
     - Best For
     - Key Benefit
   * - **Localhost** *(Recommended)*
     - Most users
     - Easy upgrades, retain previous versions
   * - **Installer**
     - Clean system installation
     - Traditional setup experience

.. important::
   Two versions cannot run concurrently. Close the application before launching a different version.

Option 1: Localhost (Recommended)
---------------------------------

1. **Download prerequisites**
   
   `Download and install prerequisites <https://github.com/kanors-emr/Veda2.0-Installation/tree/master/Localhost%20Version%20Prerequisites>`_
   
   - .NET Framework 4.8
   - Visual C++ Redistributables (2015-2022 and 2017)

2. **Download Veda 2.0**
   
   `Download latest localhost version <https://github.com/kanors-emr/Veda2.0-Installation/releases/latest>`_

3. **Extract and configure**
   
   - Extract to your preferred location
   - Grant full read/write permissions to the folder
   
4. **Open firewall port**
   
   .. code-block:: powershell

      # Run as Administrator
      netsh advfirewall firewall add rule name="Veda 2.0 Localhost" dir=in action=allow protocol=TCP localport=65001

Option 2: Installer
-------------------

1. **Download installer**
   
   `Download latest installer <https://github.com/kanors-emr/Veda2.0-Installation/releases/latest>`_

2. **Prepare installation folder**
   
   - Create a folder where you wish to install
   - Grant full read/write permissions

3. **Run the installer**
   
   Execute the setup file and follow the prompts.

4. **Open firewall port**
   
   .. code-block:: powershell

      # Run as Administrator
      netsh advfirewall firewall add rule name="Veda 2.0" dir=in action=allow protocol=TCP localport=65000

📖 For detailed step-by-step instructions with screenshots, see the `installation guide <https://veda-documentation.readthedocs.io/en/latest/pages/Getting%20started.html#installation>`_ and watch the `installation video <https://youtu.be/QQzZi2_vWBs>`_.

----

Post-Installation Setup
=======================

Setting up GAMS
---------------

GAMS (General Algebraic Modeling System) is required to run TIMES models. After installing Veda 2.0:

1. Install GAMS (version 24.8 or higher recommended)
2. Configure GAMS path in Veda 2.0 settings
3. Verify solver licenses (CPLEX, CBC, or other supported solvers)

For complete GAMS setup instructions, see `Setting up GAMS <https://veda-documentation.readthedocs.io/en/latest/pages/Getting%20started.html#setting-up-gams>`_.

Backup and Restore
------------------

Regular backups are essential for protecting your model data:

- **Backup**: Export Veda database and Excel files regularly
- **Restore**: Import from previous backups when needed
- **Version Control**: Track changes and rollback if necessary

Learn more about `Backup and Restore <https://veda-documentation.readthedocs.io/en/latest/pages/Getting%20started.html#backup-and-restore>`_ procedures.

Updating Veda 2.0
-----------------

**Localhost Version**: Simply extract the new version to a different folder. Keep previous versions available.

**Installer Version**: Run the new installer, which will upgrade the existing installation.

See `Updating <https://veda-documentation.readthedocs.io/en/latest/pages/Getting%20started.html#updating>`_ for detailed upgrade procedures.

----

Quick Start
===========

After installation:

1. **Launch Veda 2.0** from the installation directory
2. **Obtain a trial license** — `Request trial license <https://veda-documentation.readthedocs.io/en/latest/pages/License%20operations.html#trial-license>`_
3. **Load a sample model** or import your existing TIMES model
4. **Explore the tutorials** — `Watch on YouTube <https://www.youtube.com/playlist?list=PLED97cPMXPOm60xOKSwvmXaGIsQrjoM8Y>`_

**Next Steps**

- Review the `Start Page <https://veda-documentation.readthedocs.io/en/latest/pages/Start%20page.html>`_ components and workflow
- Learn about `Navigator <https://veda-documentation.readthedocs.io/en/latest/pages/Navigator.html>`_ for model management
- Understand `VEDA Tags <https://veda-documentation.readthedocs.io/en/latest/pages/VedaTags.html>`_ for data templates
- Explore the `Run Manager <https://veda-documentation.readthedocs.io/en/latest/pages/Run_Manager.html>`_ for model execution

For migrating from legacy Veda-FE/BE, consult the `Migration Guide <https://veda-documentation.readthedocs.io/en/latest/pages/Migration.html>`_.

----

Licensing
=========

Available License Types
-----------------------

Veda 2.0 offers flexible licensing options:

- **Trial License**: 30-day full-featured evaluation
- **Academic License**: Discounted rates for universities and research institutions
- **Standard License**: Single-user professional use
- **Advanced License**: Enhanced features with multi-scenario support
- **Multi-User/Department (MUD) License**: Team licenses with concurrent user management

For complete details on licensing, pricing, and regulations, see:

- `Licensing <https://veda-documentation.readthedocs.io/en/latest/pages/introduction.html#licensing>`_ overview
- `Pricing <https://veda-documentation.readthedocs.io/en/latest/pages/introduction.html#pricing>`_ structure
- `License Agreement <https://veda-documentation.readthedocs.io/en/latest/pages/License%20Agreement.html>`_ terms
- `License Operations <https://veda-documentation.readthedocs.io/en/latest/pages/License%20operations.html>`_ guide

To activate or manage your license, see `Activate/Deactivate License <https://veda-documentation.readthedocs.io/en/latest/pages/License%20operations.html#activate-deactivate-license>`_.

----

Legacy Versions
===============

Previous major versions are available for users who need them:

.. list-table::
   :header-rows: 1
   :widths: 20 40 40

   * - Version
     - Release Type
     - Download
   * - **v4.2.1.0**
     - Latest stable (19 Oct 2025)
     - `v4.2.1.0 <https://github.com/kanors-emr/Veda2.0-Installation/releases/tag/v4.2.1.0>`_
   * - **v3.2.2.0**
     - Final v3.x release (17 Nov 2024)
     - `v3.2.2.0 <https://github.com/kanors-emr/Veda2.0-Installation/releases/tag/v3.2.2.0>`_
   * - **v2.20.2.1**
     - Final v2.x release (18 Dec 2023)
     - `v2.20.2.1 <https://github.com/kanors-emr/Veda2.0-Installation/releases/tag/v2.20.2.1>`_
   * - **v1.255.1.1**
     - Final v1.x release
     - Available in Older versions folder

For complete release history with changelogs, see `Version History <https://veda-documentation.readthedocs.io/en/latest/pages/version_history.html>`_ (50+ releases documented).

----

Documentation
=============

Comprehensive documentation is available at `veda-documentation <https://veda-documentation.readthedocs.io/>`_:

**Getting Started**

.. list-table::
   :widths: 40 60
   :header-rows: 0

   * - `Introduction <https://veda-documentation.readthedocs.io/en/latest/pages/introduction.html>`_
     - Philosophy, architecture, versions, and pricing
   * - `Getting Started <https://veda-documentation.readthedocs.io/en/latest/pages/Getting%20started.html>`_
     - Installation, GAMS setup, backup/restore
   * - `License Operations <https://veda-documentation.readthedocs.io/en/latest/pages/License%20operations.html>`_
     - Activate, deactivate, and manage licenses
   * - `Migration Guide <https://veda-documentation.readthedocs.io/en/latest/pages/Migration.html>`_
     - Migrating from Veda-FE/BE to Veda 2.0

**Core Features**

.. list-table::
   :widths: 40 60
   :header-rows: 0

   * - `Navigator <https://veda-documentation.readthedocs.io/en/latest/pages/Navigator.html>`_
     - Model browsing, scenarios, and SYNC operations
   * - `VEDA Tags <https://veda-documentation.readthedocs.io/en/latest/pages/VedaTags.html>`_
     - Excel templating system and transformation rules
   * - `Run Manager <https://veda-documentation.readthedocs.io/en/latest/pages/Run_Manager.html>`_
     - GAMS execution, batch runs, GAMS Engine
   * - `Results <https://veda-documentation.readthedocs.io/en/latest/pages/Results.html>`_
     - Result import and visualization
   * - `Reports <https://veda-documentation.readthedocs.io/en/latest/pages/Reports.html>`_
     - Custom charts and Sankey diagrams

**Additional Resources**

.. list-table::
   :widths: 40 60
   :header-rows: 0

   * - `📺 Video Tutorials <https://www.youtube.com/playlist?list=PLED97cPMXPOm60xOKSwvmXaGIsQrjoM8Y>`_
     - Complete YouTube playlist with step-by-step guides
   * - `🌍 Veda Users Map <https://www.kanors-emr.org/Veda2Users/Index.html>`_
     - Global community of Veda users
   * - `📜 Version History <https://veda-documentation.readthedocs.io/en/latest/pages/version_history.html>`_
     - Detailed changelog for all releases
   * - `📋 Notes <https://veda-documentation.readthedocs.io/en/latest/pages/Notes.html>`_
     - Best practices and Veda conventions

----

Troubleshooting
===============

Common Issues and Solutions
---------------------------

If you encounter problems, consult the `Troubleshooting <https://veda-documentation.readthedocs.io/en/latest/pages/Troubleshooting.html>`_ guide:

- **Deadlock Detected**: Database locking issues
- **Excel Exceptions**: Excel integration problems
- **GAMS Engine Credentials**: Configuration errors
- **PostgreSQL Issues**: Database installation/uninstallation

For uninstallation, see `Uninstallation <https://veda-documentation.readthedocs.io/en/latest/pages/Getting%20started.html#uninstallation>`_ and `Uninstalling Postgres <https://veda-documentation.readthedocs.io/en/latest/pages/Troubleshooting/Uninstalling%20Postgres.html>`_.

----

Support
=======

Need help? Multiple support channels available:

.. list-table::
   :widths: 30 70
   :header-rows: 0

   * - **📚 Documentation**
     - `Complete user guide and reference <https://veda-documentation.readthedocs.io/>`_
   * - **🎥 Video Tutorials**
     - `YouTube playlist <https://www.youtube.com/playlist?list=PLED97cPMXPOm60xOKSwvmXaGIsQrjoM8Y>`_
   * - **🐛 Bug Reports**
     - `GitHub Issues <https://github.com/kanors-emr/Veda2.0-Installation/issues>`_
   * - **💬 ETSAP Community**
     - `IEA-ETSAP Forum <https://iea-etsap.org/>`_
   * - **🔒 Data Privacy**
     - `Privacy Policy <https://veda-documentation.readthedocs.io/en/latest/pages/Privacy%20policy.html>`_
   * - **📄 License Terms**
     - `License Agreement <https://veda-documentation.readthedocs.io/en/latest/pages/License%20Agreement.html>`_

For commercial support, training, and consulting services, contact `KanORS-EMR <https://www.kanors-emr.org/>`_.

----

*Copyright © 2020 KanORS-EMR*
