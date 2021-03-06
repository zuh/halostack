
Planned features
================

This is a page listing planned, or would-be-nice-to-have, features in
a non-specifig order.  No guarantees that these will be implemented.

GUI
---

- full graphical user interface

  - help needed

    - that is, need someone else to implement GUI

Image input
-----------

- read date and time from EXIF

  - python-exif for linux, windows?
  - separate CSV file needed for TIFF and/or windows?

- use Wand instead of PythonMagick

  - provides also EXIF functionality

- possibility to give directory containing all the photos
- possibility to give image filenames/masks in config file


Image alignment
------------------

- image rotation
  
  - scipy has the functionality, but is bloated for this single use

  - search area needs adjustment?

- lens projection handling

  - idealized projection, focal length, pixel size, ...
  - ``--lens-projection rectilinear,24,1.4,...``

- phase correlation for co-location

- solar/lunar tracking based on date, time, location and lens projection


Image enhancements
------------------

- apply enhancements stack-by-stack

  - for example, several average stacks with different
    pre/postprocessing applied

  - ``-a avg.png -a avg_pre_usm.png -e usm:25,2 -a
    avg_pre_post_usm.png -e usm:25,2 -E usm:25,2 -a avg_br.png -E
    gradient,br``

- bias subtraction
- flat correction

  - for dust and vignetting removal

- when applying to single image, skip Stack

  - also remove requirement for command-line switch for a stack

Python3
-------

- Get things ready for Python3

  - replace PythonMagick with Wand
  - check other parts
