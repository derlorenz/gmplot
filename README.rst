derLorenz' Version of gmplot
======

This library is needed to use my `PhotoMap <https://github.com/derlorenz/PhotoMap>`_  script written in Python.

Plotting data on Google Maps, the easy way. A matplotlib-like
interface to generate the HTML and javascript to render all the
data you'd like on top of Google Maps. Several plotting methods
make creating exploratory map views effortless. Here's a crash course:

::

    import gmplot

    gmap = gmplot.GoogleMapPlotter(37.428, -122.145, 16)

    gmap.plot(latitudes, longitudes, 'cornflowerblue', edge_width=10)
    gmap.scatter(more_lats, more_lngs, '#3B0B39', size=40, marker=False)
    gmap.scatter(marker_lats, marker_lngs, 'k', marker=True)
    gmap.heatmap(heat_lats, heat_lngs)

    gmap.draw("mymap.html")


Geocoding
---------

``gmplot`` contains a simple wrapper around Google's geocoding service enabling
map initilization to the location of your choice. Rather than providing latitude,
longitude, and zoom level during initialization, grab your gmplot instance with
a location:

::

    gmap = gmplot.from_geocode("San Francisco")

Plot types
----------

* Polygons with fills.
* Scatter points.
* Heatmaps.
* Pins with Infowindows

.. image:: http://i.imgur.com/dTNkbZ7.png

Misc.
-----

Original Source Code hosted on `GitHub <https://github.com/vgm64/gmplot>`_

Inspired by Yifei Jiang's (jiangyifei@gmail.com) pygmaps_ module.

.. _pygmaps: http://code.google.com/p/pygmaps/

