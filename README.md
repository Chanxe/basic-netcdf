# basic-netcdf
basic layout for creating a netCDF file using python with inputs of lat/lon and a data value

#!/home/oper/miniconda2/envs/python2.7/bin/python

#import os
#import netCDF4
#import datetime
#import numpy as np

####### This is a base outline of creating a netCDF file in python
####### What is in this file will show you how to setup the lat/lon elements
####### and how to format the data to fit the lat on lon
####### then changing the metadata is reletively easy from there


### STEP #1 ###
#load file or data to be converted to netCDF
#eg. filename = '/home/oper/chance/work/INSOLEAST.2016206'
#f = open(filename, 'r')
#f.close()

### STEP 2 ###
#create the lat and lon meshgrid
#start with the upper left corner as the begining

###replace with your lat range
#lat = [5,4,3,2,1]

###replace with your lon range
#lon = [10,9,8,7,6]


##for lat you want the second ouput of meshgrid
##lon takes the first ouput of meshgrid
#mesh_lon,mesh_lat = np.meshgrid(lon,lat)
#lat output should look like this
#[[5 5 5 5 5]
#[4 4 4 4 4]
#[3 3 3 3 3]
#[2 2 2 2 2]
#[1 1 1 1 1]]

#lon output should look like this
#[[10  9  8  7  6]
#[10  9  8  7  6]
#[10  9  8  7  6]
#[10  9  8  7  6]
#[10  9  8  7  6]]


### STEP #3 ###
#create a grid of your data
#basically want to fit data to grids so
#in this example 5,10 would but upper left and 1,6 would be lower right
#method depends on how data is retrieved
### STEP #4 ###
#setting up netCDF file to write to
#dataset = netCDF4.Dataset(filename+".nc","w",format="NETCDF4")
#create dimensions for lat,lon,data idk about this yet

#dataset.createDimension('lat',sizeOf(lat))
#dataset.createDimension('lon',sizeOf(lon))
#dataset.createDimension('data',sizeOf(data))
#create variables for lat,lon and your data
#lats = dataset.createVariable('lat',float,('lat','lon'))
#lons = dataset.createVariable('lon',float,('lat','lon'))
#data = dataset.createVariable('data',float,('lat','lon'))

### STEP #5 ###
#assign variables with their data
#lats[:] = mesh_lat
#lons[:] = mesh_lon
#data[:] = your_data

### STEP #6 ###
#change metadata accordingly
#look up online for a list of vairable names, title, time etc
