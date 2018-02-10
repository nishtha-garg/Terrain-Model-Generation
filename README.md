# Terrain-Model-Generation
Generates the terrain model of the input point cloud file


READ ME
APPROACH 1: PYTHON
The code provided is written in Python2.7 and uses the following additional packages/libraries:
1.Numpy
2.COLORSYS
3.BOKEH
4.PCL
 

1. You have to put path for the input point cloud file into datafile. Also set the paths for Outlier and Inlier files.
2. To run the code, you have to launch it from a terminal like using this syntax:
Path_to_python/python2.7 terrain_model.py
3. The program displays the terrain model at the end of the execution. Change the output file destination as desired.

APPROACH 2: MATLAB
The code is provided with MATLAB R2016a version and you need to download Point_cloud_tool in order to process the point cloud data from the link:

http://www.geo.tuwien.ac.at/downloads/pg/pctools/pctools.html#PointCloud_class 

1. Download this zip archive and extract it into an arbitrary folder
2. Add this folder to the search path in MATLAB
3. Run the file: terrainModelGeneration.m

