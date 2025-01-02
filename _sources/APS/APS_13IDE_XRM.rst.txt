.. aps_13ide_xrm

APS 13-ID-E X-ray Microprobe
===============================================================


Beamline Overview
~~~~~~~~~~~~~~~~~~~~~~~

The 13-ID-E hard x-ray microprobe provides researchers resources for
microfocused x-ray fluorescence, absorption spectroscopy, and
diffraction analysis at spatial resolutions from 500 nm to 50 microns.


Contacts
~~~~~~~~~~~~~~~~~~~~


 +-----------------------+-----------------------------------+----------------+
 | Name                  | email                             | phone          |
 +-----------------------+-----------------------------------+----------------+
 | Matt Newville         | newville@cars.uchicago.edu        | 630-327-7411   |
 +-----------------------+-----------------------------------+----------------+
 | Tony Lanzirotti       | lanzirotti@uchicago.edu           | 630-252-0433   |
 +-----------------------+-----------------------------------+----------------+

Supported Techniques
~~~~~~~~~~~~~~~~~~~~~~~~

 * Micro X-ray fluorescence analysis and mapping
 * Micro X-ray fluorescence tomography
 * Micro X-ray absorption spectroscopy (XAS, XANES, EXAFS)
 * Micro High-energy resolution flourescence detected (HERFD) X-ray absorption fine structure
 * Micro X-ray diffraction


X-ray Source and Optics
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


13-ID-E uses a 2.4 m undulator with permanent magnets and a 33-mm
period (70 pole pairs) for the X-ray source.  This undulator is the
upstream device in the canted straight-section for sector 13 with
another undulator as the source for 13-ID-C and 13-ID-D, and a canting
magnet with a 1 mrad deflection between the two undulators. The
undulator gap can be varied to change the peak X-ray energy produced,
with the smallest gap of 10.5 mm, giving X-ray energies ranging from
2.4 keV and up.

A high-heatload liquid nitrogen-cooled double crystal monochromator is
used to define the energy, using either Si(111) or Si(311) crystals,
at ~26 m from the X-ray source.  This monochromator works in fixed
offset mode, with the offset putting the monochromatic beam 25 mm
above the white beam.  The main rotation axis uses an high-torque
direct-drive motor with an air bearing and ferrofluid vacuum seal. An
optical encoder with a resolution of ~100 nrad is used to measure the
angle.

Water-cooled slts upstream of the monochromator are used to limit the
power on the monochromator, and typically set to 0.25 x 0.25 mm,
though occasionally adjusted from 0.05 to 0.5 mm in the vertical
direction, and between 0.1 and 1.0 mm in the horizontal direction.

After the monochromator the remaining white beam intensity is stopped
in a water-cooled copper block, with monochromatic beam passing over
this block. The two canted beams are separated by 1 mrad, and need to
be futher separated. Two horizontally deflecting mirror, each 500-mm
long, are pitched to 3 mrad, so deflecting the monochromatic beam by 6
mrad, each. This total of 12 mrad additional separation gives
sufficient space between the two beams in the end-station.

Because X-ray mirrors have high reflectivity for X-ray eneergeis only
up to some "critical energy" that depends on the denisty of the
reflecting material, the mirror


Detectors
~~~~~~~~~~~~~~~~~~~~

 * XRF: Mirion/Canberra SXD-7, 7-element silicon drift diode array
   with cyro-pulse cooling.  Xspress3 electronics are used for
   pulse-processing.  Backup detector: Hitachi ME-4 4-element silicon
   drift diode array, using Xspress3 pulse-processing electronics.

 * XRD: Eiger 1M detector, with 75x7f micron pixels.

 * HERFD: A custom 3-analyzer system is used for a 1-m Rowland circle
   geometry, with an Eiger 500K detector.  A variety of Si and Ge
   analyzer crystals are available.


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
stage, with typical accuracies of 100 microns or less.

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


Data Collection Software
~~~~~~~~~~~~~~~~~~~~~~~~~~~

D

Data Visualization Software
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
an APS undulator. This beam was focused to 1x1 microns using
Kirkpatrick-Baez mirrors, with typical monochromatic fluxes of 10^12
Hz.

X-ray Fluorescence (XRF) maps were collected by continuously scanning
the sample back and forth in beam, triggering detectors to collect
full XRF spectra every 5 ms and 500 nm. ROI maps were made by summing
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


X-ray Source and Optics (long)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

13-ID-E uses a 2.4 m undulator with permanent magnets and a 33-mm
period (70 pole pairs) for the X-ray source.  This undulator is the
upstream device in the canted straight-section for sector 13 with
another undulator as the source for 13-ID-C and 13-ID-D, and a canting
magnet with a 1 mrad deflection between the two undulators. The
undulator gap can be varied to change the peak X-ray energy produced,
with the smallest gap of 10.5 mm, giving X-ray energies ranging from
2.4 keV and up.

A high-heatload liquid nitrogen-cooled double crystal monochromator is
used to define the energy, using either Si(111) or Si(311) crystals,
at ~26 m from the X-ray source.  This monochromator works in fixed
offset mode, with the offset putting the monochromatic beam 25 mm
above the white beam.  The main rotation axis uses an high-torque
direct-drive motor with an air bearing and ferrofluid vacuum seal. An
optical encoder with a resolution of ~100 nrad is used to measure the
angle.

Water-cooled slts upstream of the monochromator are used to limit the
power on the monochromator, and typically set to 0.25 x 0.25 mm,
though occasionally adjusted from 0.05 to 0.5 mm in the vertical
direction, and between 0.1 and 1.0 mm in the horizontal direction.

After the monochromator the remaining white beam intensity is stopped
in a water-cooled copper block, with monochromatic beam passing over
this block. The two canted beams are separated by 1 mrad, and need to
be futher separated. Two horizontally deflecting mirror, each 500-mm
long, are pitched to 3 mrad, so deflecting the monochromatic beam by 6
mrad, each. This total of 12 mrad additional separation gives
sufficient space between the two beams in the end-station.

Because X-ray mirrors have high reflectivity for X-ray eneergeis only
up to some "critical energy" that depends on the denisty of the
reflecting material, the mirror has coatings of Pt and Rh as well as
bare Si that can be selected to reject higher harmonics of the
monochromator and undulator.
