CDO USEFUL TOOLS FOR NETCDF
================================
Here are some examples I have used, its quick and easy command lines run from inside your terminal
---------------------------------------------------------------------
**CDO installation via macports**: 

[https://code.zmaw.de/projects/cdo/wiki/MacOS_Platform](https://code.zmaw.de/projects/cdo/wiki/MacOS_Platform)

    port install cdo

Here is a link to a reference card for all the operations you can perform to data with CDO:
[http://www.iac.ethz.ch/edu/courses/master/modules/radiation_and_climate_change/download/cdo_refcard.pdf](http://www.iac.ethz.ch/edu/courses/master/modules/radiation_and_climate_change/download/cdo_refcard.pdf)


Examples:
----------------

**Change the dates of your data:**  

    cdo settaxis,0199-01-16,12:00:00,1day infile.nc outfile.nc
  
**Data interpolation example**  Monthly to daily:

    cdo intntime,32 infile.nc outfile.nc 

**Crop the time:** crop two years to one year:

    cdo seltimestep,0/365 filein.nc fileout.nc

**Change dimension name:**

    ncrename -d ,dimensionname, newdimensionname infile.nc outfile.nc

**Merge all netcdf files in a folder to one netcdf file:**

    cdo cat *.nc outfile.nc

**Select a grid:** 

    cdo sellonlatbox,0,10,-44,-47 infile.nc infileregrid.nc 

