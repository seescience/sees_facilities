.. sees_facilities  documentation master file

SEES Facilities
===============================================================

.. _Synchrotron Earth and Environmental Science: https://seescience.org
.. _DOI: https://www.doi.org/
.. _Sphinx: https://www.sphinx-doc.org/

`Synchrotron Earth and Environmental Science`_ (SEES) supports a
number of facilities and resources, including beamlines, end-stations,
supoort laboratories, and software packages.  These are in constant
development, making improvements such as replacing optics and
detectors or adding analytic methods. Some of these beamlines and
facilities have descriptions published in the literature, but this is
not done uniformly, and the published decscriptions may be many years
out of date.  It is also helpful to have these tools described in a
uniform way that is kept up-to-date and can be cited in publications
to give a reliable description of the facilities as they were used in
an experiment.

Many of thes SEES beamlines will also have facility-hosted pages
advertising the capabilities of the beamline, including supported
techniques and contact information.  The challenge for these is that
they may not be uniform across facilities, and are typically short on
details.

This documentation project has two main goals:

1. provide descriptions of these facilities that are fairly uniform,
   and in a way that is relatively easy to maintain and keep
   up-to-date.
2. provide a `DOI`_ (Digital Object Identifier) for each page and
   facility description that can be used for citations, and to be able
   to update these DOIs as the facility changes.

There are several types of facilities included here, including

1. Individual end-stations and beamlines.
2. Support laboratories.
3. Data collection, visualization, and analysis software.


How to build these documents
---------------------------------

This documentation is built with `Sphinx`_, which requires Python
(version 3.9 or higher) to build. We recommend building this on a
Linux (or macOS) system or a Windows system with the *make*
development tool installed (many user accounts set up for Epics
development will have this installed).

To install the packages needed, use:

    ~> sh install_dependencies.sh

or, on Windows:

   C:/> install_dependencies.bat

With the packages installed, you should be able to build the
documention by typing:

   make

The results will be in the `_build/html` folder.

When rendered and installed, the DOIs for these documents will point
to addressed under https://public.seescience.org/


Generating Data DOIs for these pages
-------------------------------------------

Coming soon...


Status
---------------

This documentation is in the early stages of development.

Table of Contents
============================

.. toctree::
   :maxdepth: 2
   :caption: Facilities:

   APS/index.rst
   NSLS-II
   ALS
   SSRL
   Software
   ReferenceData
