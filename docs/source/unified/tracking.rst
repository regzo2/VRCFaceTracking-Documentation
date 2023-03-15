================
Unified Tracking
================

Summary
=======

**Unified Tracking** is the main interface for all external modules to be able to send data to VRCFaceTracking, 
and contains all datas that VRCFaceTracking uses throughout the application. The following container outlines
what modules generally should use to send tracking data to VRCFaceTracking.


.. note::
  VRCFaceTracking is completely open-source and is fully documented with fleshed out code remarks available 
  for developers. `GitHub <https://github.com/benaclejames/VRCFaceTracking>`_.


Container
---------

.. note::
  Table does not contain the full **UnifiedTracking** container for the purposes of this doc. 
  Refer to `UnifiedTracking <https://github.com/benaclejames/VRCFaceTracking/UnifiedTracking.cs>`_.


.. _UnifiedTracking:
.. list-table:: UnifiedTracking
   :widths: 15 15 70
   :header-rows: 1

   * - Name
     - Type
     - Function

   * - EyeImageData
     - Image
     - Eye image data sent from the loaded eye module.
     
   * - LipImageData
     - Image
     - Lip / Expression image data sent from the loaded expressions module.
     
   * - Data
     - `UnifiedTrackingData <https://github.com/benaclejames/VRCFaceTracking/blob/master/VRCFaceTracking/UnifiedTrackingData.cs>`_
     - All accessible tracking data.

| * : Depricated and/or Obsolete.
