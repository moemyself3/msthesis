# Pipeline for variable star detection and eclipsing binary characterization 
## Author: Moises Castillo
### UTRGV Master of Science in Physics
Master Thesis submitted on 12 Aug 2019.

<em>Accepted 14 Aug 2019.</em>

### Abstract
Stars have been observed and recorded since ancient times.
Practices of documenting brightness led to observations of variability. 
Optical CCD observations of eclipsing binary stars were made with instruments
    at UTRGV Dr. Cristina Valeria Torres Memorial Astronomical Observatory.
There are two main goals for this project.
The first goal is to create a pipeline written in python (lightcurator) that
    creates a framework for detecting variable stars.
The pipeline starts by creating a list of ccd frames written in FITS format
    of an eclipsing binary star observation.
These object frames are expected to be already reduced, but lightcurator 
    provides tools to achieve this.
The object frames are aligned and stacked to create a deepsky frame.
Astrometry is performed to find the proper positions in right ascension
    and declination of all sources in the deepsky frame.
This creates a master catalogue of stars to be monitored through the entire observation.
Source extraction is performed on each object frame to generate a catalogue 
    of stars that includes the measure of instrumental flux and the time recorded.
After converting instrumental flux to instrumental magnitude, light curves 
    are produced for every object for all frames.
Currently, lightcurator is limited to detecting cataloged variable stars from the
    General Catalogue of Variable Stars (GCVS) and the Variable Star Index (VSX).
Identification of the intended eclipsing binary system is confirmed in all cases with this method.
The second goal for this project is to extract the physical parameters of the eclipsing
    binary systems observed from the time series data computed from the pipeline.


### Compilation and installation
from [martinberoiz/docthesis](https://github.com/martinberoiz/docthesis)
To compile the LaTeX document, a makefile is provided. In Unix-like systems, type:

    $ make

This will create auxiliary files in `obj/` folder and the final pdf file in there as well.

    $ make install

simply copies the final document `thesis.pdf` at the makefile directory level.
