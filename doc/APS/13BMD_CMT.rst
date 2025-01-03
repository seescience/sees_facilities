.. include:: ../substitutions.txt

.. _aps_13bmd_cmt:

APS 13-BM-D Computed MicroTomography
==============================================================

Beamline Overview
~~~~~~~~~~~~~~~~~~~~~~~

The 13-BM-D station uses monochromatic and white X-ray beams from a bending magnet
for X-ray Imaging and Computed MicroTomography measurements.



Contacts
~~~~~~~~~~~~~~


 +-----------------------+-----------------------------------+
 | Name                  | email                             |
 +=======================+===================================+
 | Mark Rivers           | rivers@cars.uchicago.edu          |
 +-----------------------+-----------------------------------+



Beamline specifications
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


 +---------------------------+-----------------------------------------------------------+
 | Quantity                  | Value                                                     |
 +===========================+===========================================================+
 | X-ray Source              | APS bending magnet                                        |
 +---------------------------+-----------------------------------------------------------+
 | Monochromator             | Double-Crystal Mono, water-cooled, Si(111)                |
 +---+-----------------------+-----------------------------------------------------------+
 |   | Energy Range (keV)    | 4.5 to 100                                                |
 +---+-----------------------+-----------------------------------------------------------+
 |   | Energy Resolution     | 1.3x10\ :sup:`-4`, typical                                |
 +---+-----------------------+-----------------------------------------------------------+
 |   | Typical Flux (Hz)     | 1x10\ :sup:`9` (10 keV)                                   |
 +---+-----------------------+-----------------------------------------------------------+
 |   | Typical Beam Size     | 15 x 5 (H x V) |micron| to 50 x 4 (H x V) mm              |
 +---+-----------------------+-----------------------------------------------------------+



Supported Techniques
~~~~~~~~~~~~~~~~~~~~~~~~

 * X-ray Computed Micro Tomography
 * High-pressure diamond anvil cell (see :ref:`aps_13bmd_dac`)
 * High-pressure multi-anvil press (see :ref:`aps_13bmd_lvp`)

Detectors
~~~~~~~~~~~~~~~~~~~~

  * FLIR USB and 10G cameras


Additional Equipment
~~~~~~~~~~~~~~~~~~~~~~~~

 * 250-ton multi-anvil press with DIA, deformation DIA, rotational Drickamer, T-cup tooling
 * Diamond anvil cell with on-line Brillouin spectroscopy
 * Laser Raman system online and in support laboratory; VIS and NIR spectroscopy online and in support lab
 * Laser Ultrasonic System in support lab
 * Sample preparatinon (laser cutting, micromanipulator, polishing, etc.)


Data Collection Software
~~~~~~~~~~~~~~~~~~~~~~~~~~~

Data collection is done with the Epics, IDL, and Python.



Data Visualization and Analysis Software
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Data visualization is done with the Epics, IDL, and Python.

X-ray Source and Optics
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

13-BM-D uses a portion of the APS bending magnet fan.  White beam can be used for X-ray
diffraction measurements with the multi-anvil press.  A combination of filters (aluminum
and copper) and vertically deflecting mirror can be used for "pink beam" that can be used
for imaging measurements in the multi-anvil press, or for tomography.  Monochromatic beam
from the double-crystal monochromator can also be used for imaging measurements in the
multi-anvil press.



Sample Mounting and Environments
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

  deformation DIA

  rotational Drickamer

  T-cup tooling


Making tooling for high pressure measurements.


Acoustic measurements?


Typical Paragraph for a publication
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The following includes typical descriptions of the beamline that can
be added to a paper. This is probably more than you need, so feel free
to edit or select portions of this for main text or supplemental
informations as appropriate, or ask the beamline staff for guidance.

This work used the beamline 13-BM-D at the Advanced Photon Source, Argonne National Laboratory.


Related Support Laboratories
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

  * Tooling
  * Acoustic measurements
