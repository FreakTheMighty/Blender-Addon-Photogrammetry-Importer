# Blender-Addon-Photogrammetry-Importer
This repository contains a Blender addon to import reconstruction results of several libraries.

Supported libraries / data formats:
- [x] Polygon Files ([http://paulbourke.net/dataformats/ply/](http://paulbourke.net/dataformats/ply/))
	* PLY
- [x] VisualSFM reconstructions ([http://ccwu.me/vsfm/](http://ccwu.me/vsfm/))
	* NVM
- [x] Colmap reconstructions ([https://github.com/colmap/colmap](https://github.com/colmap/colmap)) 
	* Colmap model folders (binary and txt format), Colmap workspaces, NVM, PLY 
- [x] OpenMVG reconstructions ([https://github.com/openMVG/openMVG](https://github.com/openMVG/openMVG))
	* JSON, NVM, PLY
- [x] Meshroom reconstructions ([https://alicevision.github.io/](https://alicevision.github.io/))
	* MG, JSON, SfM, PLY
- [x] Open3D reconstructions ([http://www.open3d.org/](http://www.open3d.org/))
	* JSON, LOG, PLY


Tested for Blender 2.81. There is an older version of the addon available for Blender 2.79 that allows to import NVM files - see the [2.79 branch](https://github.com/SBCV/Blender-Import-NVM-Addon/tree/blender279).

## Getting Started
- [Tutorial Video](https://www.youtube.com/watch?v=BwwaT2scoP0) 
- [Installation Instructions](doc/markdown/installation.md)
- [Examples](doc/markdown/example.md)
- [Import Data](doc/markdown/import.md)
- [Export Data](doc/markdown/export.md)
- [Adjust Results (Scale Cameras and Points)](doc/markdown/adjustment.md)
- [Ensure Camera and Point Alignment](doc/markdown/alignment.md)
- [Point Cloud Visualization and Rendering](doc/markdown/point_cloud.md)
- [Addon Usage with Python](doc/markdown/python.md)
- [Contribution](doc/markdown/contribution.md)
- [Recent features / Changelog](doc/markdown/changelog.md)

## Example
This repository contains an example NVM file. The imported result looks as follows.
![alt text](https://github.com/SBCV/Blender-Import-NVM-Addon/blob/master/doc/images/import_result.jpg)
The input images of the NVM file are located here: [https://github.com/openMVG/ImageDataset_SceauxCastle](https://github.com/openMVG/ImageDataset_SceauxCastle).

There is an import option that interpolates the reconstructed camera poses to compute a camera animation.
![alt text](https://github.com/SBCV/Blender-Import-NVM-Addon/blob/master/doc/images/camera_animation.gif)

You can also overlay the (sparse) point cloud with the corresponding mesh - see [Import Data](doc/markdown/import.md). 
![alt text](https://github.com/SBCV/Blender-Import-NVM-Addon/blob/master/doc/images/point_cloud_mesh_overlay.jpg)

The addon offers an option to draw big point clouds with OpenGL to reduce computational requirements. The addon provides a panel to export these OpenGL point clouds renderings - see [Point Cloud Visualization and Rendering](doc/markdown/point_cloud.md). 
![alt text](https://github.com/SBCV/Blender-Import-NVM-Addon/blob/master/doc/images/import_result_opengl.jpg)
