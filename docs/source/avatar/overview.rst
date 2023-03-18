================================
Avatar Face Tracking Overview
================================

.. note::

   Document under construction


Summary
=======

This page will go over everything needed to use face tracking 
on avatars using **VRCFaceTracking**, including creating face 
tracking shapes, creating animation setups, and Platform-specific 
cases such as **VRChat**.


Overview
========

For using face tracking:

#. :ref:`using vrcfacetracking`
#. :ref:`Avatars`

For setting up face tracking on avatars:

#. :ref:`Avatar Setup`

.. _Avatars:

Avatars
=======

Avatars are the digital bodies that users inhabit on various 
virtual platforms such as **VRChat**, **ChilloutVR**, and **Neos**.
Generally avatars have a level of customization and control of expression 
on these platforms, and **VRCFaceTracking** allows face tracking interfaces such 
as the Vive Pro Eye, Vive Facial Tracker, and Quest Pro to control avatar 
expressions.

Avatars generally will need to be setup to use **VRCFaceTracking**, 
though there may be some avatars already come with full or 
*partial* **VRCFaceTracking** support.


.. note::
   Avatars with *partial* **VRCFaceTracking** support generally either
   have face tracking shapes included on the avatar mesh and require 
   the user to setup :ref:`Avatar Parameters` and animations or 
   are using non-face tracking shapes with :ref:`Avatar Parameters`
   setup to animate them.


.. note::
   Avatar creators will generally clearly label an avatar's level of 
   support for **VRCFaceTracking**, or if they have face tracking 
   shapes (``SRanipal``, ``AR52/ARKit/PerfectSync``, ``Meta Quest FACS``, or 
   ``Unified Expressions`` are very commonly associated).
