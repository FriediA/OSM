# OSM

Get all hospitals - readme

Author: Friederike Alschner CartONG/ICRC
Date: 27.03.2015

The script is to get all hospitals that are currently available in OSM between 70° North and 60° South.
It returns all polygon centroids and points with the predicate: amenity=hospital from overpass.api

The script will return a csv-file and a feature class (ESRI geodatabase feature class) giving the following information about each hospital: 
Name, Emergency, Latitude, Longitude and whether the source in OSM is a centroid or node.
The script runs for approximately one hour.

To use the script on your computer update
a)	the output file and path for the intermediate csv-file  -line 131 csvfile_path='C://Users//FriediA//Downloads//all_hospital.csv'
b)	the env.workspace for the conversion to a gdb –line 174 (only used for temporary files ) 
c)	The final output layer and location –line 174 (which needs to be the name of a feature class in a ESRI geodatabase): 
    outlayer= 'D:/GIS/OSM_dataextract/getting_OSMdata.gdb/hospitals'

	
If a csv or feature class with the same name exist already it will be overwritten.
