========================
VRCFaceTracking Program
========================

.. note::

   Document under construction

VRChat has no native implementation of Vive' SRanipal software needed to interface with the Facial Tracker nor Vive Pro Eye, or any other face tracking interface, 
which means there must be an intermediary software accessing the face tracking data and sending it to VRC via OSC.
VRCFaceTracking fulfills this role as the intermediary, creating a standard face-tracking parameter set for use with VRChat avatars. 

Download the latest version here: https://github.com/benaclejames/VRCFaceTracking/releases/latest

.. _Using VRCFaceTracking:

Using VRCFaceTracking 
=====================

TODO

To use VRCFT, make sure to enable OSC in VRChat. 
VRCFaceTracking will automatically set OSC to "Enabled" if it detects that it wasn't already, but you can (and should) also enable it manually. 

Changing the OSC IP and Ports
------------------------------

Use ``--osc=[output port]:[ip address]:[input port]`` launch argument.

For example: ``--osc=9000:127.0.0.1:9100`` is the common option when using VRCFaceTracking with :ref:`VRChatOSCRouter`. 

To set this permanently, create a shortcut to the VRCFaceTracking program, right-click the newly-created shortcut and open "Properties", and add the line to the shortcut "Target". 
Make sure to maintain a space between the flags and what was in the box already, and keep the flags outside of the quotation marks of the file path if they exist.

.. image:: ware/images/vrcft_shortcut_example.png
   :width: 300
   :align: center
   :alt: vrcft shortcut example

VRCFaceTracking "Housekeeping" 
==============================

There are occasionally small things good to be aware of when using face tracking with VRCFT and VRChat. 

.. _Unblocking Downloaded Dynamic Link Libraries:

Unblocking Downloaded Dynamic Link Libraries (.dlls)
-----------------------------------------------------

#. Right-click on the .dll file, open "Properties"
#. Down at the bottom of the Properties window check the checkbox option for 'Security' to "Unblock". 

.. note:: 

   If you don't see a checkbox to "Unblock", then it was not blocked automatically by Windows and you can safely continue.

.. _Reset OSC Config:

Resetting VRChat OSC Configs
-----------------------------

Until VRChat releases the `"OSC Query" update <https://ask.vrchat.com/t/developer-update-2-september-2022/13470#oscquery-9>`_ to VRChat (`currently in closed beta <https://github.com/vrchat-community/osc/issues/143#issuecomment-1304419543>`_),
VRCFaceTracking will rely on the static OSC config .json to know what parameters to send. This configuration file is **never** updated automatically, it must be reset manually to force VRC to generate an up-to-date version. 

There are two ways of resetting the configs:

#. Using the OSC Radial Menu (In-game)

   #. While in VRC, open the Radial Menu.
   #. Navigate to Options -> OSC 
   #. Make sure that "Enabled" is set to True (white bar on the right side). Setting this will cause an avatar refresh. 

#. Deleting the .json files 

   #. Navigate to your AppData folder. You can get to ``AppData\Roaming`` by typing ``%appdata%`` into the search bar in the Windows Start Menu, or in the address bar of any Explorer window. 
   #. Go to ``..\AppData\LocalLow\VRChat\VRChat\`` and delete the OSC folder.
   #. Restart VRC or refresh your avatar (by resetting or swapping avatar)


Common Problems and How to Solve Them
======================================

- **VRCFaceTracking isn't starting at all**

   - Cause: VRCFaceTracking is likely trying to access a module library (.dll) that is blocked by Windows Security. 
   - Solution: :ref:`unblocking downloaded dynamic link libraries`

- **VRCFaceTracking is crashing when I join a world / change avatars** 

   - Cause: VRCFaceTracking failed to parse an invalid avatar OSC config.
   - Solution: Clear out your VRChat Avatar OSC folder. See :ref:`reset osc config`

Don't see your problem here? Make sure to check the pages specific to your hardware setup. 
If you still cannot find an answer to your specific problem, create a help request in the #setup-help-forum in the `VRCFT Discord <https://discord.gg/Fh4FNehzKn>`_.