# Detrend-Surface-Models
ESRI 10.x and ArcPro tools to detrend surface models.  These tools are intended to detrend surface models along river channels.
These tool include Arc Toolbox tool to detred surface models using Euclidean plane, transects, and Voronoi polygons (experimental).  
ArcGIS or ArcPro are required.

Detrend By Transect:
Using user defined transect lines that cross perpendicular to a river channel the tool finds the lowest elevation along the river channel.  The lowest elevation along the transect become the z value for the detrended surface.  The detrended surface is subtracted from the existing surface models.  Note:  Transect lines must not cross each other.  

Detrend By Voronoi:
Detrend by Voronoi polygons uses points distrubuted along the river centerline.  Voronoi (Theissen polygons) are created around each point and the lowest elevation within each polygon is used to create the detrended surface.

Detrend By Euclidean Plane:
Three user-defined x,y,z points define a plane across the extent of the surface.  This plane is used as the detrending surface.
