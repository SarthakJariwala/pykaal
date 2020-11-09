======
pykaal
======


Read, plot and analyze lifetime data. Currently, it inherently supports reading data collected
using Picoharp instruments.

Suports only Python >3.6.


Installation
============

.. code-block:: bash

    pip install pykaal

Usage
=====

.. code-block:: python

    import pykaal as kl

    # Read Picoharp .phd files
    p = kl.read_phd(filename)

    # Get number of traces
    len(p)

    # General information about the data
    print(p)

    # Get specific traces
    p.curve(0) # get the first trace

    # Get trace resolution
    p.res(0)

    # Get time-axis for the first trace
    p.t(0)

    # Plot the first trace
    p.plot(0)

    # Plot multiple traces on a matplotlib figure
    import matplotib.pyplot as plt

    fig, ax = plt.subplots()

    p.plot(0, ax=ax) # plot the first trace on axis 'ax'
    p.plot(1, ax=ax) # plot the second trace on the same axis

    # Alternatively, you can also plot the following way
    plt.plot(p.t(0), p.curve(0))

    # Plot traces without normalizing
    p.plot(0, norm=False) # default is True

    # Simple boxcar smoothening
    p.smooth(0, smooth=True, boxwidth=3) # you can also specify the 'mode', refer to numpy.convolve for more info

    # Plot with smoothening
    p.plot(0, smooth=True, boxwidth=3)


Future
======

- Lifetime analysis
