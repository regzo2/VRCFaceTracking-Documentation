===================
Vive Facial Tracker
===================

.. note::

   Document under construction


Introduction
=============
The Vive Facial Tracker provides lower face tracking for Vive Pro and other VR headsets. 
It connects to the computer via a short, built-in USB C cable. 
Face tracking data is accessed through Vive's SRanipal interface.

Why follow this guide? 
-------------------------------
The Vive Facial Tracker is a high bandwidth USB device sensitive to poor USB connectivity, leading to a lot of "gotchas" in hardware setup.
Also, the SRanipal software is notoriously annoying to deal with. 

Software Setup
==============

.. note:: 
    Install SRanipal first *before* plugging in the Vive Facial Tracker to make your life a bit easier.

Regardless of what headset, the Vive Facial Tracker requires the computer that it connects to to have SRanipal runtime installed to be able to be used.
Follow the :ref:`sranipal setup` instructions to get this necessary software installed and ready. 

Hardware Setup
==============

Setup for the Vive Facial Tracker will be split across different types of headset "categories". 

    #. Vive Pro Series
    #. Valve Index / Other Wired VR headsets
    #. Quest / other Standalone with PC Streaming

There are some special notes for certain headsets and setup methods in the last section.

.. note:: 
    A shoddy USB connection for the Facial Tracker can lead to it getting stuck trying to update its firmware, never initializing. 
    If possible, the plug the facial tracker **directly into a USB-C port on your computer** to allow it to update (if it needs to). 


Vive Pro Series
---------------

This is by far the easiest headset(s) to setup the Vive Facial Tracker for, as it was made for these headsets. 
Follow the official Vive Facial Tracker installation instructions: https://www.vive.com/us/support/facial-tracker/category_howto/tracker.html

Once SRanipal is installed and the headset connected to the computer and powered on, SRanipal might be unresponsive for a while the Facial Tracker updates its firmware. 

Vive Pro Mounting Alternatives
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

The adhesive that comes with the Vive Facial Tracker isn't the best, and can easily fail with a knock to the headset. 
Here are some alternative mounting solutions:

#. 3D printed Mount: https://www.thingiverse.com/thing:5405617
#. Use 3M VHB Tape as adhesive replacement
#. Wrap rubber bands around the facial tracker mounting legs and whole headset (ask Azmidi...)
#. Wrap a wire around everything??? (ask PLPlolol...)

Valve Index / Wired VR Headsets
--------------------------------

The position of the Vive Facial Tracker relative to your lower face is *very important*. 
More often than not bad tracking is the result of a bad position/angle of the facial tracker. 
Getting a good 3D printed mount is essential for avoiding tracking issues on non-Vive Pro headsets. 
Ask around in the #3d-printing channel in the VRCFT discord if you need help. 

.. _Valve Index:

Valve Index
^^^^^^^^^^^

This section assume you are intending to use a USB-C female to USB-A Male USB adapter in the Index "frunk" USB 3.0 port. 

#. Get a **USB 3.0 or higher** USB-C female to USB-A Male USB adapter, such as https://smile.amazon.com/gp/product/B083XXLW77
   
    .. warning::
        This is the **#1 reason** for problems in VRCFaceTracking with Index users. 
        **DO NOT BUY THE SHORT STUBBY USB2.0 ADAPTERS**. A proper USB 3.0+ adapter will be "long"! 

#. Remove the front plate covering the frunk area of the Index. 

#. Connect the Facial Tracker to the adapter, and the adapter into the frunk USB port directly. Using a USB hub in the frunk *can* cause issues.
#. Mounting options for the Valve Index

   - https://discord.com/channels/849300336128032789/915075185328152606/987813371992748072
   - MORE TODO
   - The MidnightTech little-stub mount for the Valve Index is *not that great*... 

The Index frunk area can get quite warm, and the USB adapters can get **very hot**, making the headset heat worse. If possible, try to keep the front of the headset actively cooled, and/or add a heatsink to the USB adapter. 


Other Wired VR Headsets
^^^^^^^^^^^^^^^^^^^^^^^

Get a quality **USB 3.0 or better USB** extension. Since USB-C female extensions are rare, if you are getting a USB-C female to USB-A Male USB adapter, follow the :ref:`Valve Index` adapter instructions. 

Quest / other Standalone with PC Streaming
------------------------------------------

Using the headset as a VirtualHere USB server is a possible solution that allows for a fully wireless setup. 
VRCFT member Blackspots#0001 has a nice reddit post detailing the process for the Quest 2: https://www.reddit.com/r/Quest2/comments/xlvbc8/getting_the_vive_face_tracker_to_work_with_the/
This proceed *may* work for other similar headsets (Pico 3, Pico 4, etc.) but have not been tested. 
