Wing Blender
============

NOTE: If you're looking for Thomas Bruckner's utilities, [they can be found here](http://www.ciinet.org/kevin/tbruckner).

Wing Blender is an import/export plugin for Blender 2.65+ that allows you to
export a VISION engine ([Wing Commander: Prophecy](http://www.wcnews.com/wcpedia/Wing_Commander:_Prophecy),
[Wing Commander: Secret Ops](http://www.wcnews.com/wcpedia/Wing_Commander:_Secret_Ops))
IFF 3D model, or import a VISION engine IFF 3D model into Blender.

This means you'll be able to do most of your work in Blender, and then export
it directly to VISION engine `.IFF` format without the need to use other programs
to set or modify model metadata, such as the collision sphere, center/radius of
each LOD, or hardpoints.

This project is the successor to [OBJ2WCP](http://www.ciinet.org/kevin/java),
a poorly-written Java OBJ->XMF converter.

Features
--------

- LOD mesh support.
- Customization of collision sphere, LOD ranges, and other metadata.
  Such metadata is automatically generated if a custom value is not found.
- Detection and "translation" of numeric texture file names.
  For example, if your Blender model uses a texture file named `424242.png`,
  the exported IFF model will use `00424242.mat`.
- Import/export support for flat colour materials. If you have no valid
  (uv-mapped image) textures assigned to a material in your model, the exporter
  will treat it as a flat colour material.
- Child objects are exported along with the main object.
