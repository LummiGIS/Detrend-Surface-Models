## Detrend-Surface-Models
ESRI Toolbox tools to detrend surface models (create relative elevation models REM).  These tools were developed to detrend surface models along river channels.
These tool include Arc Toolbox tool to detrend surface models using Euclidean plane, by transect lines, and (coming soon to Pro) using Voronoi polygons, and points along thalweg.  Tools we updated for use in ArcGIS Pro 3.3 in June, 2025.

### Detrend By Cross Sections (Pro v3.3):
Inputs and outputs: 
       1. A folder or geodatabase to store temporary data.
       2. A TIN surface models that gets created as temporary data.
       3. User defined cross sections lines running perpendicular to the river thalweg.
       4. Input surface model to detrend.
       5. Output detrended (REM) surface.
Using user defined transect lines that cross perpendicular to a river channel (or any topographic fall line). The tool finds the lowest elevation along the fall line.  The lowest elevation along the transect become the z value for the trend surface.  The trended surface is subtracted from the existing surface models to produce the detrended surface (REM).  Note:  Transect lines must not cross each other.  The recent popularity in topo-bathymetric surface models means that cross sections can pick up elevation values from river bottoms like pools and have lower values than adjacent cross sections.  These river bottom transect z values will cause dips in the detrend.  User feedback is appreciated if this is noticeable in your detrended surface.

### Detrend By Euclidean Plane (Pro v3.3):
Inputs and outputs: 
    1.  A featureclass of three non-collinear points.  These points need to be attributed with the z values at the top, bottom, and center of the river channel.
    2.  The attribute field name that stores the z values.
    3.  The surface model to detrend.
    4.  The output detrended surface (REM).
Three user-defined x,y,z points define a plane across the extent of the surface.  This plane is used as the detrending surface.  The trend surface will be bound by the extend of the non-collinear points so make sure your points extend beyond your area of interest.

See this link for more information on detrending by the great W.  Huber. (https://gis.stackexchange.com/questions/11440/removing-elevation-trend-over-sloped-surfaces)
or this link from Wa DOE on detrending:  https://apps.ecology.wa.gov/publications/documents/1406025.pdf
and this link by Dan Coe for a QGIS methods:  https://dancoecarto.com/creating-rems-in-qgis-the-cross-section-method

### ArcGIS10x tools are available on request. 
