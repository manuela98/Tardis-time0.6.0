.. tardis documentation master file, created by
   sphinx-quickstart on Tue Jan  8 00:44:25 2013.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.



Tardis: Time Travel Made Easy
================================

datetime?  Where we're going, we don't need datetime.

This document describes Tardis v\ |version|.

`Tardis` is the name of the car in the movie Back to the Future. The movie deals with a lot of time travel, hence the name Tardis as a module dealing with datetimes.

`Tardis` is a library for clearing up the inconvenient truths that arise dealing with datetimes in Python. Understanding that timing is a delicate enough of a problem `tardis` hopes to provide a cleaner less troublesome solution to shifting, manipulating, generating `datetimes`.

Tardis stands on the shoulders of giants `pytz <http://pytz.sourceforge.net/>`_ and `dateutil <http://labix.org/python-dateutil>`_

`Tardis` will provide natural language improvements for manipulating time, as well as datetime abstractions for ease of use. The overall goal is to improve datetime manipulations, with a little bit of software and philosophy.

Pretty much make you a badass, time traveller.

Interface Update
^^^^^^^^^^^^^^^^
Version 0.6.0 introduces the following breaking changes:
    - `Tardis.epoch` is a property, not a function.
    - `Tardis.midnight` is a property, not a function.
    - `Tardis.naive` is a property, not a function.
    - `Tardis.timezone` is a property, not a function.

Please make sure to update your code accordingly.

Getting Started
^^^^^^^^^^^^^^^

Here is the world without a flux capacitor at your side.::

    from datetime import datetime
    import pytz

    est = pytz.timezone('US/Eastern')
    d = datetime.now(pytz.utc)
    d = est.normalize(d.astimezone(est))
    return d

Now lets warm up the `tardis`::

    from tardis import Tardis

    d = Tardis()
    d = d.shift('US/Eastern')
    return d

Look at you looking all fly. This was just a test drive checkout out what else
`tardis` can help with below.

Guide
=====

.. toctree::
    :maxdepth: 2

    license
    install
    quickstart
    interface
    contribution
    philosophy
    changelog
