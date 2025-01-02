.. include:: ../substitutions.txt

.. _aps_13ide_xrm:

APS 13-ID-E X-ray Microprobe
===============================================================

Beamline Overview
~~~~~~~~~~~~~~~~~~~~~~~

The 13-ID-E hard x-ray microprobe provides researchers resources for
microfocused x-ray fluorescence, absorption spectroscopy, and
diffraction analysis at spatial resolutions from 0.5 to 200 |micron|.


Contacts
~~~~~~~~~~~~~~

 +-----------------------+-----------------------------------+
 | Name                  | email                             |
 +=======================+===================================+
 | Matt Newville         | newville@cars.uchicago.edu        |
 +-----------------------+-----------------------------------+
 | Tony Lanzirotti       | lanzirotti@uchicago.edu           |
 +-----------------------+-----------------------------------+


Beamline specifications
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


 +---------------------------+-----------------------------------------------------------+
 | Quantity                  | Value                                                     |
 +===========================+===========================================================+
 | X-ray Source              | APS undulator, 33 mm period                               |
 +---------------------------+-----------------------------------------------------------+
 | Typical Beam Size         | 0.5 x 0.5 |micron| to 200 x 200 |micron|                  |
 +---------------------------+-----------------------------------------------------------+
 | Monochromator             | Double-Crystal Mono, LN2-cooled, 2 crystal sets           |
 +---+-----------------------+-----------------------------------------------------------+
 | Si (111) monochromator crystal set                                                    |
 +---+-----------------------+-----------------------------------------------------------+
 |   | Energy Range (keV)    | 2.3 to 28                                                 |
 +---+-----------------------+-----------------------------------------------------------+
 |   | Energy Resolution     | 1.3x10\ :sup:`-4`, typical                                |
 +---+-----------------------+-----------------------------------------------------------+
 |   | Typical Flux (Hz)     | 5x10\ :sup:`10` (2.5 keV), 5x10\ :sup:`12` (10 keV)       |
 +---+-----------------------+-----------------------------------------------------------+
 | Si (311) monochromator crystal set                                                    |
 +---+-----------------------+-----------------------------------------------------------+
 |   | Energy Range (keV)    | 4.8 to 28                                                 |
 +---+-----------------------+-----------------------------------------------------------+
 |   | Energy Resolution     | 4x10\ :sup:`-5`, typical                                  |
 +---+-----------------------+-----------------------------------------------------------+
 |   | Typical Flux (Hz)     | 1x10\ :sup:`11` (7 keV), 2x10\ :sup:`12` (10 keV)         |
 +---+-----------------------+-----------------------------------------------------------+


Supported Techniques
~~~~~~~~~~~~~~~~~~~~~~~~

 * Micro X-ray fluorescence analysis and mapping
 * Micro X-ray fluorescence tomography
 * Micro X-ray absorption spectroscopy (XAS, XANES, EXAFS)
 * Micro High-energy resolution flourescence detected (HERFD) X-ray absorption fine structure
 * Micro X-ray diffraction


Detectors
~~~~~~~~~~~~~~~~~~~~

 * XRF: Mirion/Canberra SXD-7, a 7-element silicon drift diode array
   with cyro-pulse cooling.  Xspress3 electronics are used for
   pulse-processing.  Backup detector: Hitachi ME-4 4-element silicon
   drift diode array, using Xspress3 pulse-processing electronics.

 * XRD: Eiger 1M detector, with 75x75 |micron| pixels.

 * HERFD: A custom 3-analyzer system is used for a 1-m Rowland circle
   geometry, with an Eiger 500K detector.  A variety of Si and Ge
   analyzer crystals are available.

Additional Equipment
~~~~~~~~~~~~~~~~~~~~~~~~

 * Peltier-cooled sample stage
 * Cryogenic sample stage
 * Ultraviolet light illuminator
 * Offline Sample Coordinate and Registration System (OSCAR)
 * Laboratory facilities including microscopes, bench-top SEM, fume hood, glove box.


Data Collection Software
~~~~~~~~~~~~~~~~~~~~~~~~~~~

Data collection is done with the EpicsScan application which uses
Epics, Python, and Postgresql.  This provides a Graphical User
Interface for configuring up and running X-ray Fluorescence maps,
X-ray absorption scans, and simple line scans.  All XRF maps and XAS
scans are done in "continuous" or "fly-scan" mode, where detectors are
triggered by hardware pulses from the motor controllers.



The EpicsScan application supports a set of commands or "macros" that
can be run to allow users to change X-ray energy, move to a new sample
position, and change beamline conditions.  These commands can be mixed
with scanning commands and entered into a queue to be run unattended.

A Graphical application is provided for the on-line Sample Microscope,
allowing users to move around their samples and save positions by name
that can be recalled in the application or used by the EpicsScan
software.

The microscope uses a high-resolution (5 MB) camera with a high
dynamic range.  The field of view is typically ~1 x 1 mm, but this can
be adjusted (manually).  The lighting is typcially in reflection, with
a lamp whose intensity can be adjusted, as well as the frame
integration time and gain. Lighting in transmission can be done for
samples that allow it. A user-controllable pan-tilt-zoom camera in the
hutch allows a large field of view.  The microscope image is saved
with each named position.

The sample sits with its surface at 45 degrees to the beam, and the
microscope is (approximately) normal to sample surface. Beamline staff
will set up the microscope and focus the X-ray beam so that the
focused beam is near the center of the field of view when the sample
surface is in focus. For most samples and configurations, this will be
very close, but should not be trusted to be better than 10 or even 50
|micron|. Instead, and XRF map should be made and used to select points
for further analyses.

A Graphical application, Epics XRF Control, for viewing and
investigating live XRF spectra as they are collected from the XRF
detector is provided.  This can be used to define Regions of Interests
(ROI) in the spectra, to measure count rates and check for detector
saturation, to investigate peak detection limits, and to look for
fluorescence from unexpected elements.

A Graphical application, Epics Instruments, can be used to save and
restore positions for pre-defined beamline components.  This can be
used, for example, to change slit sizes, detector distances, or the
setup of X-ray mirrors.  These settings will usually be accessible as
macro commands in the EpicsScan software.

The software for these applications can be found at
  * `epicsscan`_
  * `epicsapps`_
  * `xraylarch`_

Some introductory videos and tutorials can be found at:
  * https://www.youtube.com/playlist?list=PLgNIl_xwV_vKf83c2O7mwVtHERRK6belh

In addition, "Epics Display Screens" from an Epics Display Manager,
such as MEDM or Phoebus can be used for some very low-level
interactions with the control system. This is generally discouraged
for users, and users are encouraged to contact the beamline scientists
before using these screens.



Data Visualization and Analysis Software
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

For X-ray Fluorescence (XRF) Maps, visualization and analysis are done
with the `GSECARS XRFMap Viewer` application, which is part of the
Larch software distribution.  This provides tools for

  * visualizing Region-of-Interest maps, typically with either indidividually or as 3-color maps
  * extracting XRF spectra from regions of a map.
  * fitting XRF spectrum, including to quantities proportional to
    elemental abundances, and then applying these to make maps of abundances.

For X-ray absorption (XAS) spectra, the `Larix` application, which is
part of the Larch software package, is recommended.  This provides
tools for visualization of XANES and EXAFS spectra, including

  * XAS pre-edge subtraction and normalization.
  * energy alignment, glitch removal, merging specta, correcting
    over-absorption.
  * XANES Principal Component Analysis, Linear Combination Fitting,
    and some regression analysis to external variable.
  * XANES pre-edge peak fitting.
  * EXAFS background subtraction and Fourier transform.
  * Running Feff (including a browsable database of mineral structures
    to use) for path EXAFS modeling.
  * EXAFS fitting usig Feff Paths.

These can be downloaded at `xraylarch`_, which includes some
documentation. A series of videas for XAS analysis can be found at
https://www.youtube.com/playlist?list=PLgNIl_xwV_vK4V6CmrsEsahNCAsjt8_Be


The older `Athena` and `Artemis` applications can also be used,
especially for people who are using Windows and are already familiar
with it.


X-ray Source and Optics
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

13-ID-E uses a 2.1-m long undulator with permanent magnets and a 33-mm
period (62 pole pairs) for the X-ray source.  The undulator gap can be
varied from 10.5 mm up to 150 mm, giving X-ray energies ranging from
2.4 keV and up.

A liquid nitrogen-cooled double crystal monochromator is used to
define the energy, using either Si(111) or Si(311) crystals, at ~26 m
from the X-ray source.  This monochromator works in fixed offset mode,
with the monochromatic beam 25 mm above the white beam.  Water-cooled
slts upstream of the monochromator limit the power on the
monochromator, and typically set to 0.25 x 0.25 mm, though
occasionally adjusted from 0.05 to 0.5 mm in the vertical direction,
and between 0.1 and 1.0 mm in the horizontal direction. After the
monochromator the remaining white beam intensity is stopped in a
water-cooled copper block, with monochromatic beam passing over this
block.

The monochrmatic beam is then deflected horizontally by 2
horizontal mirrors, each 500-mm long, are pitched to 3 mrad, so
deflecting the monochromatic beam by 6 mrad, each. The 12 mrad
deflection separates this branch from the other branch (for 13-ID-C
and 13-ID-D), to give sufficient working space in the 13-ID-E
end-station.  The mirrors are polished to be very flat so that they
preserve the horizontal divergence of the source.

Since X-ray mirrors have high reflectivity for X-ray eneergeis only
up to some "critical energy" that depends on the denisty of the
reflecting material, these mirrors have separate coatings of platinum
and rhodium as well as bare silicon.  This ultimately limits the
beamline to an upper energy limit of about 28 keV.

A moveable view-screen with a phosphor and CCD camera can be placed in
the monochromatic beam, just downstream of mirrors, and is used to
assist setting up the monochromator and mirrors.  A second beam
positio monitor is at 42 m from the source.  This is made from a set
of thin metal foils (typically 1 |micron| thick) that are placed in the
beam.  4 photodiodes are used to record the fluoreecence from the
metal foils, and can be used to stabize the beam position in both
horizontal and vertical directions.

The X-ray beam is in vacuum until it enters the 13-ID-E endstation,
where it exits vacuum through a beryllium window.  To protect the
beryllium, a modest vacuum is maintained, with a Kapton window in air
protecting the vacuum. The monochromatic beam is focused to the sample
position with a set of Kirkpatrick-Baez mirrors (one focusing
vertically, followed by one focusing horizontally).  These mirrors are
pitched at angles varying from 2 to 6 mrrad, with 3 mrad commonly.
These mirrors have a rhodium metal coating, as well as bare silicon, A
set of slits is used to define the beam hiting the mirrors, typically
set between 200x200 and 400x400 |micron|, depending on the pitch of the
mirrors, and the desired flux. After the slites, a set of attenuators
and a small lead sheet can be placed in the beam to block or reduce
the beam intensity.  An ion chamber is placed between the attenuators
and mirrors, with the volume from Kapton exit-window to end of the
mirrors kept in a helium environment to allow the soft X-rays down to
2.4 keV to travel to the sample.

The sample stage generally sits in air or in a helium environment.


Sample Mounting and Environments
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Most samples are analyzed at ambient conditions, either in air or in a
helium enclosure for work at low X-ray energy (typically, below 3.5
keV).

A variety of sample holders can be used to mount 3 or 6 one-inch round
sample mounts or "pucks", as it typical for many geological thin- or
thick-sections.

There are also several sample holders available for mounting
petrographic slides and polished thin-sections.  For such mounts, we
strongly recommend using clean quartz instead of boro-silicate glass
to avoid background signals from Ca, Ti, Fe, As, and many other
elements.

For both 1-inch rounds and slides, the sample holders are on magnetic
mounts that can readily be mounted and re-mounted on the beamline.
These can also be mounted on an offline microscope at the beamline.
This allows users to find and save locations for analysis prior to
analysis (or while other measurements are being made).  The saved
locations can then be automatically transferred to the beamline sample
stage, with typical accuracies of 100 |micron| or less.

Grains mounted on fibers for XRD or XRF tomography are supported.  We
recommend quartz fibers.

Samples extracted by focussed ion-beam (FIB) milling and mounted onto
TEM grids can also be mounted. Using Cu grids will make it nearly
impossible to analyze elements above the Cu K-edge (8980 eV).

A cryogenic stage using liquid nitrogen, and similar to a Linkam cold
stage is available.  This can keep a sample at -180 C or colder.  A
cold stage is available that can keep a sample at -10 to -20 C, though
this is rarely used.  For both of these, one sample is mounted at a
time, and changing samples can take tens of minutes to an hour.

For analysis of radioactive samples, or any samples where uranium (at
any concentration or isotope) is a main element of interest,
containment of potential radiation from the sample will need to be
considerd.  This often means using a few separate layers of Kapton
between the sample and the outside world.  To be clear, while APS
Health Physics group does recognize that there are non-hazardous
levels of uranium, and some samples need no containment, they are
always the ones who decide what containment - and training - is needed
for such samples.

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Typical Paragraph for a publication
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The following includes typical descriptions of the beamline that can
be added to a paper. This is probably more than you need, so feel free
to edit or select portions of this for main text or supplemental
informations as appropriate, or ask the beamline staff for guidance.

This work used the X-ray microprobe at beamline 13-ID-E at the
Advanced Photon Source, Argonne National Laboratory. A double crystal
Si(111) monochromator was used to select the desired X-ray energy from
an APS undulator. This beam was focused to 1x1 |micron| using
Kirkpatrick-Baez mirrors, with typical monochromatic fluxes of 10\ :sup:`12`
Hz.

X-ray Fluorescence (XRF) maps were collected by continuously scanning
the sample back and forth in beam, triggering detectors to collect
full XRF spectra every 5 ms and 0.5 |micron|. ROI maps were made by summing
fixed energy bins in the XRF spectra for each pixel.

X-ray Diffraction (XRD) maps were collected along with the XRF maps,
triggering to colect and XRD image with each pixel in XRF map.

X-ray Absorption spectra (XAS/XANES/EXAFS) were collected by scannning
the energy of the monochromator and undulator together across the Fe K
edge (near 7110 eV).  The energy was scanned continuously but binned
to simulate a classic XAS stepscan, with steps of 2 eV below the edge
(7020 to 7100 eV), 0.1 eV steps across the edge (7070 to 7120 eV) and
steps in wavenumber k of 0.05 Ang^1 above the edge (7120 to 7670 eV),
with 1 sec between bins, so that each XAS scan took 7 to 8 minutes.

High-Energy Resolution Flourescence Deteected (HERFD) XAS was
collected with a 3-analyzer system.


Related Support Laboratories
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

  * SEM
  * off-line microscope
