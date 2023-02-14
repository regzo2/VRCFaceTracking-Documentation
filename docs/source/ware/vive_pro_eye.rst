============
Vive Pro Eye
============

.. note::

   Document under construction


Summary
============
The Vive Pro Eye provides eye gaze tracking as well as detailed eye expression tracking. It is a *built-in* eye-tracking device (no additional hardware setup required). Eye tracking data is accessed through Vive's SRanipal interface.

Setup
============

1. Follow the Vive hardware setup instructions that came the headset. Make sure that the headset cable is not damaged, and make sure to plug in the USB connection from the linkbox to a USB 3.0 port (usually *blue* internal connector tab)
2. Install the SRanipal runtime software. See the guide :ref:`sranipal setup`
3. Calibrate the eye tracking with the SRanipal Vive Pro Eye Calibration tool in SteamVR

Common Hardware Issues
========================

- A regular Vive Pro is occasionally mistaken to be a Vive Pro Eye. A Vive Pro Eye will have **light blue** rings around the front two passthrough cameras and a plastic covered IR LED ring on the inside

    .. image:: images/vpe_front.jpg
        :width: 400
        :align: center
        :alt: vpe front

    .. image:: images/vpe_inside.jpg
        :width: 400
        :align: center
        :alt: vpe inside

- The headset cable can be damaged with heavy use, especially if it gets tangled around or used with a ceiling pulley system. 
  A damaged cable *may not show tell-tale "display snow"* or even obvious physical indicators, but can affect USB connectivity of the Eye but more commonly, the Vive Facial Tracker. 
  Replacing the headset cable will often resolve "cutting out" or "fail to initialize" face and eye tracking problems. 
