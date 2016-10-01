.. _doc_instancing:

Instancing
==========

Rationale
---------

Having a scene and throwing nodes into it might work for small projects,
but as a project grows, more and more nodes are used and it can quickly
become unmanageable. To solve this, Godot allows a project to be
separated in several scenes. This does not work the same way
as in other game engines, it's quite different, so please do
not skip this tutorial!

A scene is a collection of nodes organized as a tree, 
where they can have only one single node as the tree root.

.. image:: /img/tree.png

In Godot, a scene can be created and saved to disk. As many scenes
can be created and saved as desired. While editing a scene, 
other scenes can be instanced as part of it:

.. image:: /img/instancing.png

In the above picture, Scene B was added to Scene A as an instance. It
may seem weird at first, but at the end of this tutorial it will make
complete sense!

Instancing, step by step
------------------------

To learn how to do instancing, let's start with downloading a sample
project: :download:`instancing.zip </files/instancing.zip>`.

Unzip this scene in any place of your preference. Then, add this scene to
the project manager using the 'Import' option:

.. image:: /img/import-2.1.png

Simply browse to inside the project location and open the "engine.cfg"
file. The new project will appear on the list of projects. Edit the
project by using the 'Edit' option.

This project contains two scenes "ball.scn" and "container.scn". The
ball scene is just a ball with physics, while container scene has a
nicely shaped collision, so balls can be thrown in there.

.. image:: /img/tutorial-instancing-scene-container-2.1.png

Open the container scene, select the root and click the instancing button!

.. image:: /img/tutorial-instancing-container-instance-root-2.1.png

Select the ball scene (ball.scn), the ball should appear in the origin
(0,0), move it to the center of the scene, like this:

.. image:: /img/tutorial-instancing-container-ball-instanced-2.1.png

Press Play and Voila!

.. image:: /img/playinst.png

The instanced ball fell to the bottom of the pit.

A little more
-------------

There can be as many instances as desired in a scene, just try
instancing more balls, or duplicating them (Ctrl-D or duplicate button):

.. image:: /img/tutorial-instancing-container-balls-instanced-2.1.png

Then try running the scene again:

.. image:: /img/instmanyrun.png

Cool, huh? This is how instancing works.

Editing instances
-----------------

Select one of the many copies of the balls and go to the property
editor. Let's make it bounce a lot more, so look for the bounce
parameter and set it to 1:

.. image:: /img/tutorial-instancing-container-bounce-2.1.png

A revert button appears, pressing the revert button will restore the
property to the value set in the original scene. Even if a property is 
modified in the original scene, the custom value will always overwrite it. 

Conclusion
----------

Instancing seems handy, but there is more to it than it meets the eye!
The next part of the instancing tutorial should cover the rest...
