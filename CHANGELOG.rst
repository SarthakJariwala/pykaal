=========
Changelog
=========

Version 0.0.2
=============

- BUGFIX: MacOS bug where ".phd" files were not correctly loaded due to `ctypes` error in `CurveHdr`.

Version 0.0.1
=============

- Read Picoharp ".phd" files using 'read_phd()'
- Extract information from the files such curves, resolution and other instrument settings
- Plot the curves using matplotlib in the backend
