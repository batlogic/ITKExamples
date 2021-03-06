Watershed Image Filter
======================

.. index::
   single: WatershedImageFilter

Synopsis
--------

This example illustrates how to segment an image using the watershed method.

Results
-------

.. figure:: BrainProtonDensitySlice.png
  :scale: 50%
  :alt: Input image

  Input image

.. figure:: SegmentWithWatershedImageFilterTest02Baseline.png
  :scale: 50%
  :alt: Segmented image

  Segmented image


Code
----

C++
...

.. literalinclude:: Code.cxx
   :lines: 18-

Python
......

.. literalinclude:: Code.py
   :lines: 1, 18-


Classes demonstrated
--------------------

.. breathelink:: itk::WatershedImageFilter
