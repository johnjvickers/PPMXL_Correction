

======
PPMXL Correction
======

This is python code of the method presented in the paper "A Global Correction to PPMXL Proper Motions" from Vickers+2016.

The method recenter.recenter(ra, dec, j) returns proper motion corrections, in mas/yr (NOT deg/yr!) for the columns "pmra (Proper Motion in RA*cos(delta))" and "pmde (Proper Motion in Dec)" from the ppmxl.main database on the VO (TAP address: http://dc.zah.uni-heidelberg.de/__system__/tap/run/tap)

Dependencies
------------

- numpy
- scipy
- pyfits (for the test files)


Tests
-----

Make sure the above dependencies are installed. In the PPMXL_Correction directory, run:

$ python recenter.py

This should create a new file named vc_qso_recentered.fit

$ diff vc_qso_recentered.fit vc_qso_recentered_original.fit

Should show the rubric file, and the file created on your machine are identical.
