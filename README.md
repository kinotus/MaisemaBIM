# MaisemaBIM
Alternative versions of MaisemaBIM vegetation models. Dataset contains simple trees bush, hedge and perennial plant 3D models.

## Original data
- MaisemaBIM system information (in Finnish) from BuildingSmart Finland: https://wiki.buildingsmart.fi/fi/04_Julkaisut_ja_Standardit/maisema-bim
- Models are available https://drive.buildingsmart.fi/s/5sznpNbYjcbmJb3

## What is wrong with the originals?
- Closed old formats are used, not ready for web-3D.
- FBX as ASCII, Blender wont read it.

## What is different from the originals?
- Ready to use Blender and GLB-files
- Visualization versions available (folder suffix VIS - they contain only trunk and canopy (root volumes deleted)

## Process
- Convert IFC-models to OBJ with IfcConvert (https://ifcopenshell.org/downloads.html)
  -  `ifcConvert --precision 4 --use-element-names --weld-vertices --orient-shells %1 %1.obj `
- Convert OBJ's with Blender's Transmogrifier plugin https://github.com/SapwoodStudio/Transmogrifier to .blend
- Remove non-visualisation geometry, fix material and object names
- Export GLB's Y-up

## Please note
- OBJ's dont have normals, nor fixed material names, Z up.

## TODO
- Fix all material names
- Geometrynode versions for hedges
- Test IFC's with BlenderBIM
- USDZ AR-models
- Preview images with human for scale
