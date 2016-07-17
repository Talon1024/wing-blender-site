Importing a model
=================

Wing Blender can be used to import models from Wing Commander: Prophecy/Secret
Ops.

The VISION engine has 4 types of IFF models:

1. Thruster plume models (cones).
2. Mesh-only models (debris pieces).
3. Ship/component models.
4. Model sequences (Shield models).

Wing Blender can import mesh-only models and ship models.

Obtaining a model to import
---------------------------

You need a model from Wing Commander: Prophecy/Secret Ops in order to be able
to import it with Wing Blender.

You can use [HCl](http://hcl.solsector.net)'s [treman](http://hcl.solsector.net/archive/treman1.zip) tool to extract the
models from Wing Commander: Prophecy/Secret Ops or your favourite WCP/SO mod. If treman does not run on your system, download
[CWSDPMI](http://web.archive.org/web/20150817040602/http://homer.rice.edu/~sandmann/cwsdpmi/index.html), put it in the same folder as `treman`, and run `treman` in [DOSBox](www.dosbox.com).

Simply go to File -> Import -> WCP/SO IFF Mesh File (.iff), and choose the model
you want to import.

Obtaining the textures for the models
-------------------------------------

After you extract the models from the game, you can optionally extract its
textures. Wing Blender can attempt to read textures in the same folder as the
model, or in the "mat" folder in the parent directory.

The textures can be in MAT format, in which case it will be converted to a
Blender image, or any other format that Blender can use.

In order for Wing Blender to find the textures, the textures must have filenames
that are the same as the model's texture numbers. For example, if your model
uses textures 22000, 22001, 424242, etc., The textures must be named 00022000.mat,
00022001.mat, and 00424242.mat.

Importing child object models
-----------------------------

Wing Blender can import child object models, such as the Seahawk AWACS' Radome,
or the Panther's yaw pod. However, Since Wing Blender cannot load ship files
(info files, not models), it cannot automatically determine which hardpoint
each child object should be attached (parented) to.

When you import a child object, you should parent it to the appropriate hardpoint.
