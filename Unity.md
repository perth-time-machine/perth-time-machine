# Introduction
This document contains information relevant to Unity.

## Import from Blender
Note you have to bake the materials / textures for Unity import to work, otherwise Unity can't create the materials.

https://blender.stackexchange.com/questions/131622/how-bake-cycles-material-to-pbr-texture-in-2-80/131628#131628

https://blendermarket.com/products/simplebake---simple-pbr-and-other-baking-in-blender-2

Control + A to apply transforms e.g. rotation before exporting.

Export FBX. Make sure appropriate objects are selected.

From export settings : Transform > Apply Transform


## VR
Create new project in latest Unity version.

Add the latest version of SteamVR Plugin.

Go to Edit > Project Settings > XR Plug-in Management > tick OpenVR Loader.

Add a Player prefab to the scene and delete the default camera.
