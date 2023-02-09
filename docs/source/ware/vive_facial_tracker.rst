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

.. _SRanipal Setup:

SRanipal Setup
==============

.. note:: 
    Install SRanipal first *before* plugging in the Vive Facial Tracker to make your life a bit easier.

Regardless of what headset, the Vive Facial Tracker requires the computer that it connects to to have SRanipal runtime installed to be able to be used.
There are three methods of installing SRanipal, listed here from most official to least.

#. Install Vive Console (avaliable on Steam or Vive website)
#. Use the VRCFT Mirror installer of SRanipal v1.3.1.1 
#. Use the v1.3.6.5 zip of SRanipal in #file-share

SRanipal support for the Vive Facial Tracker basically hasn't been updated since v1.3.1.1. Version 1.3.2.0 introduced a performance bug that would cause an unreasonable amount of CPU usage by the runtime, with no
other notable difference from v1.3.1.1. There have been newer versions of SRanipal corresponding with fixes and features for the Vive Focus 3, so these newer versions are **not necessary** over 1.3.1.1.
In fact, any version over version 1.3.6.8 will be incompatible with non-Vive Pro headsets, as a check was added to SRanipal initialization for the existence of a Vive Pro headset connected to the PC on startup in later versions. 
Version 1.3.6.5 is not *known* to have any notable benefits over v1.3.1.1. Some users have reported less resource utilization / better performance as compared to v1.3.1.1, but such claims are not verified. 

Thus: 

    - Vive Pro series users should generally use options 1 or 2, with option 3 as an alternative.
    - Most other users should use option 2, with option 3 as an alternative.


Installing Via Vive Console 
---------------------------

#. It is recommended to install Vive Console via Steam: https://store.steampowered.com/app/1635730/VIVE_Console_for_SteamVR/
#. After install, run Vive Console once to let it's internal installers run. You never need to run Vive Console again. 

   - An alternative is to go to the Vive Console install location(``Steam\steamapps\common\VIVEDriver\App\SRanipal``) and simply run the driver installer in that folder, and never touch Vive Console. 
   - Vive Console does take up a lot of space (~1.6Gb), so copying the SRanipal folder out, then uninstalling Vive Console is another avenue. 

Installing Via v1.3.1.1 Installer
---------------------------------

#. Download the SRanipal v1.3.1.1 installer: https://drive.google.com/file/d/16Qbl2NKHCBK_8osIDu0o1-03WFiDxtMX/view?usp=sharing
#. Run the installer and follow the installer process

.. wasn't there a mirror on Ben's server somewhere 

**Important:** The installer for v1.3.1.1 is has a known failure point during installation: **Error 1001**

    .. image:: images/vive_installer_error_1001.png
        :width: 500
        :align: center
        :alt: vpe front

In case you encounter this error when attempting to install SRanipal v1.3.1.1, you can either

#. Ignore the warning message, pull computer power so the installer doesn't uninstall anything, and use v1.3.1.1 anyways because Error 1001 is meaningless, or
#. Attempt :ref:`uninstalling sranipal` and seeing if it installs correctly after
#. Install SRanipal via one of the other options (Vive Console or the v1.3.6.5 zip)

Installing Via v1.3.6.5 .zip
-----------------------------

#. Download the SRanipal v1.3.6.5 .zip: https://discord.com/channels/849300336128032789/915075185328152606/1017600042837753906
#. Unzip the folder and run ``DriverInstaller.msi``

.. _Uninstalling SRanipal:

Uninstalling SRanipal
---------------------

In case SRanipal seems to have some issues (especially after having mixed different versions) and the SRanipal installer seems to be unable to uninstall SRanipal, follow these instructions from Vive Admin C.T.: 
https://forum.htc.com/topic/5642-sranipal-getting-started-steps/?do=findComment&comment=46845

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
