# sees_facilities
Sphinx documentation for SEES facilities, end stations, support
laboratories, software, and other resources.

This documentation is built with Sphinx, which requires Python
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
