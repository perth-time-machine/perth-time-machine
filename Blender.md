# Introduction
This document contains information relevant to Blender.

# Useful Add-ons
- Plane from image
- Contruction Lines
- Import fspy Project

# Workflows
## Kerbs
For a block where one edge is an angle, extrude that edge manifold. If you grab the handle it will extrude parallel.

Where the angle and straight kerbs meet, extrude normals.

## Terrain
Decimate the terrain mesh.

On the appropriate map, draw lines, rectangles etc with Construction Lines

## Buildings
### fspy
Open the reference image in fspy. Set up so that the axes and origin all intersect.

Import fspy into Blender.

### Symmetrical building
If two-way symmetrical, then you can just delete half the model and mirror over the required axis. If it's 4-way symmetrical you might need to move the model origin point by setting the 3D cursor to where you want the origin (e.g. via selecting a vertex), then in object mode go to Object > Set Origin > Origin to 3D Cursor.

### Cutting curves into faces
Draw a bezier (etc) curve exactly where you want it. It will be a curve object. Reduce number of vertices if needed. Convert it to a mesh. 

In edit mode, select the object you want to cut the curve into. Control click the curve (so it selects it second), then Mesh > Knife Project.

## General Tips
### Move 3D cursor to vertex
Go to edit mode > select the vertex > Shift + s > Cursor to Active

### Set object origin
Move the 3D cursor where needed > object mode > mesh > object > set transform > origin to 3D cursor

### Simplify
Can do this from Mesh > Cleanup

### Flipping an object
's' to scale, then set 1 / -1 as appropriate on each axis. Make sure object origin is set appropriately.

### Curve resolution / number of vertices
Select curve > object mode > Object Data Properties in right pane (for curves this has a curve icon) > Active spline > Resolution U

### UV unwrap see selected faces in original model
There's a sync toggle, which is a button with diagonal arrows in each direction

## One-Time Blender Terrain / Map Setup
These are historical notes for reference.

### Sketchup
Start in Sketchup to create the overall terrain and basic map. This is more effectice (but more expensive!) than doing via osm in Blender.

In Sketchup, use the PlaceMaker extension to create a geosurface for the desired area. This is a geolocated plane with basic satellite imagery.

In the PM dialog, select the plane, add map (not satellite) imagery and terrain (separate items). This will cost about $90. It will add two tags - a plane with a map on it and the actual terrain.

Export to obj twice, each time only showing one or the other tags.

### Blender

Import each obj exported from Sketchup, you will end up with two separate meshes / objects in your file. Sort them into appropriate collections

Now import any extra maps e.g. sewer maps. Import as plane : File > Import > Images as Planes. Note you need to enable the addon first for that.

They will be tiny at first. Scale them up, rotate them etc until they match the flat map. This is a labourious process.



