.. _Unified Expressions:

===================
Unified Expressions
===================

.. note::

   Document under construction

Summary
=======

**Unified Expressions** is an open source face expression standard that can used by avatars. 
It is both fully compatible with and based on many existing face tracking shapes such as 
``ARKit`` / ``PerfectSync``, ``SRanipal``, ``FACS``, and others.

.. note::
  These do not include parameter *specific* optimizations which can be found on :ref:`Avatar Parameters`, 
  only available shapes for modelling on an avatar are listed here.


Unified Expressions Overview
================================

| :ref:`Why use Unified Expressions`
| :ref:`Unified Expressions Best Practices`
| :ref:`Unified Expressions Shapes`


.. _Why use Unified Expressions:

Why use Unified Expressions? 
--------------------------------

**Unified Expressions** is a fully envolved face expression standard that avatars can use directly for 
creating face tracking shapes. It is able to use shapes designed for other tracking standards and 
provide tracking transformations to work with different shape standards such as ``ARKit`` and ``SRanipal``. 

**VRCFaceTracking** uses **Unified Expressions** as the bridge between tracking interfaces and avatars to allow 
for a huge amount of tracking customization, specialization, and backwards compatibility for many existing avatars.

Building an avatar for **Unified Expressions** also means that you will only have to build a single set of shapes 
for an avatar that will work nearly identically across different face tracking devices and interfaces. 
**Unified Expressions** shapes are untied to any device or interface implementation.


.. _Unified Expressions Best Practices:

Unified Expressions Best Practices
--------------------------------------

**Unified Expressions** is similar to most other facial expression standards available, though with many additional
transformed expression shapes provided that allow avatars to highly specialize or even optimise for particular
:ref:`Avatar Setup`. Generally avatars should try correlate to the provided shapes for the best and most accurate
tracking results.

Creators who wish to use **Unified Expressions** on their avatars will find that there are many tracked shapes
available for use for avatar face tracking. **Unified Expressions** has many *Blended* shapes that can be used 
to simplify, combine, or alleviate both shape creation and offer more simplified tracking. Creators should 
familiarize with all available shapes and decide what shapes work best with avatars.


.. _Unified Expressions Shapes:

Unified Expressions Shapes
==============================

This sections contains documentation for all currently implemented **Unified Expressions** 
shapes available for use in **VRCFaceTracking** on avatars.

Generally avatars should try to base their expression shapes on the base **Unified Expressions** shapes, and 
combine into *Blended* shapes afterward. Depending on the desired tracking or expression shapes available on an 
avatar, there are :ref:`Unified Expressions Blended Shapes` that combine or simplify many of the base 
shapes into more compact and simplified shapes.

.. _Unified Expressions Base Shapes:

Unified Expressions Base Shapes
-------------------------------

The following tables contain all base shapes that are used on avatars and as the basis of **VRCFaceTracking**'s 
avatar parameters.

.. note::
  For **VRCFaceTracking** specific avatar parameters, refer to :ref:`Avatar Parameters`.

..
  .. list-table:: Example Shape Table
    :widths: 25 50 25
    :header-rows: 1

    * - Name
      - Function
      - Reference

    * - JawOpen
      - Opens the jaw bone to reveal the inside of the mouth.
      - .. image:: images/unified/jaw_open_1.png

  .. list-table:: Example Blended Shape Table
    :widths: 25 25 25 25
    :header-rows: 1

    * - Name
      - Function
      - Basis
      - Reference

    * - MouthOpen
      - Parts both lips.
      - MouthUpperUpLeft,
        MouthUpperUpRight,
        MouthLowerDownLeft,
        MouthLowerDownRight,
      - Picture reference (Lips part).

    * - MouthX
      - Moves the lips left to right.
      - MouthUpperLeft,
        MouthUpperRight,
        MouthLowerLeft,
        MouthLowerRight,
      - 2 Picture references (left, right).

.. list-table::
   :widths: 25 50 25
   :header-rows: 1

   * - Name
     - Function
     - Reference

   * - EyeLookOutRight
     - Right eye looks outwards.
     - .. image:: images/jawopenexample.gif
     
   * - EyeLookInRight
     - Right eye looks inwards.
     - 
     
   * - EyeLookUpRight
     - Right eye looks up.
     - 
     
   * - EyeLookDownRight
     - Right eye looks down.
     - 
     
   * - EyeLookOutLeft
     - Left eye looks outwards.
     - 
     
   * - EyeLookInLeft
     - Left eye looks inwards.
     - 
     
   * - EyeLookUpLeft
     - Left eye looks up.
     - 
     
   * - EyeLookDownLeft
     - Left eye looks down.
     - 

   * - 
     - 
     - 

   * - EyeClosedRight
     - Closes the right eyelid.
     -
     
   * - EyeClosedLeft
     - Closes the right eyelid.
     - 
     
   * - EyeDilationRight
     - Dilates the right eye pupil
     - 
     
   * - EyeDilationLeft
     - Dilates the left eye pupil
     - 
     
   * - EyeConstrictRight
     - Constricts the right eye pupil
     - 
     
   * - EyeConstrictLeft
     - Constricts the left eye pupil
     - 

   * - EyeSquintRight
     - Squeezes the right eye socket muscles.
     - 
     
   * - EyeSquintLeft
     - Squeezes the left eye socket muscles.
     - 
     
   * - EyeWideRight
     - Right eyelid widens beyond relaxed.
     - 
     
   * - EyeWideLeft
     - Left eyelid widens beyond relaxed.
     - 


.. list-table::
   :widths: 25 50 25
   :header-rows: 1

   * - Name
     - Function
     - Reference

   * - BrowPinchRight
     - Right eyebrow pulls inwards and down.
     - .. image:: images/jawopenexample.gif
     
   * - BrowPinchLeft
     - Left eyebrow pulls inwards and down.
     - 
     
   * - BrowLowererRight
     - Outer right eyebrow pulls down.
     - 
     
   * - BrowLowererLeft
     - Outer Left eyebrow pulls down.     
     - 
     
   * - BrowInnerUpRight
     - Inner right eyebrow pulls up.
     - 
     
   * - BrowInnerUpLeft
     - Inner left eyebrow pulls up.
     - 
     
   * - BrowOuterUpRight
     - Outer right eyebrow pulls up.
     -
     
   * - BrowOuterUpLeft
     - Outer left eyebrow pulls up.
     - 


.. list-table::
   :widths: 25 50 25
   :header-rows: 1

   * - Name
     - Function
     - Reference

   * - NasalDilationRight
     - Right side nose's canal dilates.
     - .. image:: images/jawopenexample.gif

   * - NasalDilationLeft
     - Left side nose's canal dilates.
     - 
     
   * - NasalConstrictRight
     - Right side nose's canal constricts.
     - 

   * - NasalConstrictLeft
     - Left side nose's canal constricts.
     -


.. list-table::
   :widths: 25 50 25
   :header-rows: 1

   * - Name
     - Function
     - Reference

   * - CheekSquintRight
     - Raises the right side cheek.
     - .. image:: images/jawopenexample.gif

   * - CheekSquintLeft
     - Raises the left side cheek.
     - 
     
   * - CheekPuffRight
     - Puffs the right side cheek.
     - 

   * - CheekPuffLeft
     - Puffs the left side cheek.
     -
       
   * - CheekSuckRight
     - Sucks in the right side cheek.
     - 

   * - CheekSuckLeft
     - Sucks in the left side cheek.
     -


.. list-table::
   :widths: 25 50 25
   :header-rows: 1

   * - Name
     - Function
     - Reference

   * - JawOpen
     - Opens jawbone.
     - .. image:: images/jawopenexample.gif

   * - JawRight
     - Pushes jawbone right.
     - 

   * - JawLeft
     - Pushes jawbone left.
     - 
     
   * - JawForward
     - Pushes jawbone forwards.
     - 
     
   * - JawBackward :sup:`1`
     - Pulls jawbone backwards
     - 
     
   * - JawClench :sup:`1`
     - Flexes jaw muscles.
     - 

   * - JawMandibleRaise :sup:`1` :sup:`2`
     - Raises jawbone.
     - 

| :sup:`1` : These shapes are currently unused by most interfaces (though they are anatomically based), intended for future compatibility.
| :sup:`2` : These shapes are generally not necessarily physically possible.


.. list-table::
   :widths: 25 50 25
   :header-rows: 1

   * - Name
     - Function
     - Reference

   * - LipSuckUpperRight
     - Upper right lip part tucks in the mouth.
     - .. image:: images/jawopenexample.gif
     
   * - LipSuckUpperLeft
     - Upper left lip part tucks in the mouth.
     - 
     
   * - LipSuckLowerRight
     - Lower right lip part tucks in the mouth.
     - 
     
   * - LipSuckLowerLeft
     - Lower left lip part tucks in the mouth.
     - 
       
   * - LipSuckCornerRight :sup:`1`
     - Right lip corner folds into the mouth.
     - 
     
   * - LipSuckCornerLeft :sup:`1`
     - Left lip corner folds into the mouth.
     -
       
   * - 
     - 
     -
          
   * - LipFunnelUpperRight
     - Upper right lip part pushes into a funnel.
     - 
     
   * - LipFunnelUpperLeft
     - Upper left lip part pushes into a funnel.
     - 
       
   * - LipFunnelLowerRight
     - Lower right lip part pushes into a funnel.
     - 
     
   * - LipFunnelLowerLeft
     - Lower left lip part pushes into a funnel.
     -
               
   * - LipPuckerUpperRight
     - Upper right lip part pushes outward.
     - 
     
   * - LipPuckerUpperLeft
     - Upper left lip part pushes outward.
     - 
       
   * - LipPuckerLowerRight
     - lower right lip part pushes outward.
     - 
     
   * - LipPuckerLowerLeft
     - lower left lip part pushes outward.
     -
            
   * - 
     - 
     -
          
   * - MouthUpperUpRight
     - Upper right part of the lip pulls up.
     -
               
   * - MouthUpperUpLeft
     - Upper left part of the lip pulls up.
     -

   * - MouthLowerDownRight
     - Lower right part of the lip pulls up.
     -
               
   * - MouthLowerDownLeft
     - Lower left part of the lip pulls up.
     -
               
   * - MouthUpperDeepenRight
     - Upper right lip part pushes in the cheek.
     -
               
   * - MouthUpperDeepenLeft
     - Upper left lip part pushes in the cheek.
     -
            
   * - 
     - 
     -

   * - MouthUpperRight
     - Moves upper lip right.
     -
     
   * - MouthUpperLeft
     - Moves upper lip left.
     -

   * - MouthLowerRight
     - Moves lower lip right.
     -
     
   * - MouthLowerLeft
     - Moves lower lip left.
     -
            
   * - 
     - 
     -

   * - MouthCornerPullRight
     - Right lip corner pulls diagnally up and out.
     -
     
   * - MouthCornerPullLeft
     - Left lip corner pulls diagnally up and out.
     -

   * - MouthCornerSlantRight
     - Right corner lip slants up.
     -
     
   * - MouthCornerSlantLeft
     - Left corner lip slants up.
     -
                 
   * - 
     - 
     -
     
   * - MouthFrownRight
     - Right corner lip pulls down.
     -
     
   * - MouthFrownLeft
     - Left corner lip pulls down.
     -

   * - MouthStretchRight
     - Stretches the right side lips outwards.
     -
     
   * - MouthStretchLeft
     - Stretches the left side lips outwards.
     -
                      
   * - 
     - 
     -
     
   * - MouthDimpleRight
     - Right lip corner is pushed backwards.
     -
     
   * - MouthDimpleLeft
     - Left lip corner is pushed backwards.
     -
                           
   * - 
     - 
     -

   * - MouthRaiserUpper
     - Raises and pushes out the upper mouth.
     -
     
   * - MouthRaiserLower
     - Raises and pushes out the lower mouth.
     -

   * - MouthPressRight
     - Right side lips press and flatten together.
     -
     
   * - MouthPressLeft
     - Left side lips press and flatten together.
     -
     
   * - MouthTightenerRight
     - Right side lips squeeze together horizontally.
     -
     
   * - MouthTightenerLeft
     - Left side lips squeeze together horizontally.
     -

| :sup:`1` : These shapes are currently unused by most interfaces (though they are anatomically based), intended for future compatibility.


.. list-table::
   :widths: 25 50 25
   :header-rows: 1

   * - Name
     - Function
     - Reference

   * - TongueOut
     - Sticks the tongue out of the mouth.
     - .. image:: images/jawopenexample.gif

   * - 
     - 
     -

   * - TongueUp
     - Points the tongue up.
     - 
     
   * - TongueDown
     - Points the tongue down.
     -

   * - TongueRight
     - Points the tongue right.
     -
     
   * - TongueLeft
     - Points the tongue left.
     -
          
   * - 
     - 
     -
 
   * - TongueRoll
     - Morphs tongue into a 'hotdog' shape.
     -
      
   * - TongueBendDown :sup:`1`
     - Tongue arches up then down.
     -
           
   * - TongueCurlUp :sup:`1`
     - Tongue arches down then up.
     -
           
   * - TongueSquish :sup:`1`
     - Tongue narrows and thicker.
     -
           
   * - TongueFlat :sup:`1`
     - Tongue widens and thins.
     -
               
   * - 
     - 
     -
 
   * - TongueTwistRight :sup:`1`
     - Tongue tip rotates right.
     -
      
   * - TongueTwistLeft :sup:`1`
     - Tongue tip rotates left.
     -


.. list-table::
   :widths: 25 50 25
   :header-rows: 1

   * - Name
     - Function
     - Reference

   * - SoftPalateClose
     - Closes the back of the throat in the mouth.
     - .. image:: images/jawopenexample.gif
      
   * - ThroatSwallow
     - Pulls the Adam's Apple upwards (to swallow).
     -
      
   * - 
     - 
     - 
      
   * - NeckFlexRight
     - Flexes the right neck muscle.
     -
      
   * - NeckFlexLeft
     - Flexes the left neck muscle.
     -

| :sup:`1` : These shapes are currently unused by most interfaces (though they are anatomically based), intended for future compatibility.

.. _Unified Expressions Blended Shapes:

Unified Expressions Blended Shapes
----------------------------------
 
The following shapes are intended to simplify and blend together the :ref:`Unified Expressions Base Shapes` 
above. Creating shapes for these *Blended* shapes instead can be used to simplify shape 
creation, optimise avatars for specific face tracking setups, or allow an avatar to exhibit certain 
tracking behaviors.

The following shapes also are categorized by what their general expression functionality is based on.

.. All of the following shapes are pulled from https://github.com/benaclejames/VRCFaceTracking/blob/Quest-Pro/VRCFaceTracking/Params/Expressions/UnifiedExpressionsMerger.cs
   Specifically parameters that directly blend the shapes together (if a parameter uses two or more parameters on the pos/neg)


.. note::
  **Unified Expressions** as a standard is intended to be as flexible as possible for avatar creation. 
  Many shapes may be able to be discretionally mixed and matched together that are not otherwise 
  listed here. The listed shapes below also have direct tracking transformations available in 
  **VRCFaceTracking**.


.. note::
  These shapes do not include parameter *specific* optimizations which can be found on 
  :ref:`Avatar Parameters`, though the shapes listed here are closely tied with specific 
  **VRCFaceTracking** :ref:`Avatar Parameters`.


  .. list-table:: Eyebrow Blended Expressions
   :widths: 25 50 25
   :header-rows: 1

   * - Name
     - Function
     - Reference

   * - BrowsDownRight
     - Pulls the right eyebrow down and in.
     - 

   * - BrowsDownLeft
     - Pulls the left eyebrow down and in.
     - 
     
   * - BrowsDown
     - Pulls the eyebrows down and in.
     - 
  
.. list-table:: Mouth Open Expressions
   :widths: 25 50 25
   :header-rows: 1

   * - Name
     - Function
     - Reference

   * - MouthUpperUp
     - Raises the upper lips.
     - 
     
   * - MouthLowerDown
     - Lowers the lower lips.
     - 
          
   * - MouthOpen
     - Parts the lips evenly.
     - 
