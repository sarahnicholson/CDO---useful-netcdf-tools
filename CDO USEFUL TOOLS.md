CDO USEFUL TOOLS FOR NETCDF
================================
Here are some examples I have used, its quick and easy command lines run from inside your terminal
---------------------------------------------------------------------
**CDO installation via macports**: 

[https://code.zmaw.de/projects/cdo/wiki/MacOS_Platform](https://code.zmaw.de/projects/cdo/wiki/MacOS_Platform)


  port install cdo


Examples:
----------------

**Change the dates of your data:**  

  cdo settaxis,0199-01-16,12:00:00,1day infile.nc outfile.nc  </br>
  
**Data interpolation example**  Monthly to daily: </br>
   
  cdo intntime,32 infile.nc outfile.nc </br>

**Crop the time:** crop two years to one year: </br>

  cdo seltimestep,0/365 filein.nc fileout.nc  </br >

**Change dimension name:**  </br > 
  
  ncrename -d ,dimensionname, newdimensionname infile.nc outfile.nc </br>

**Merge all netcdf files in a folder to one netcdf file:**  </br >

  cdo cat *.nc outfile.nc </br >

**Select a grid:** </br >

  cdo sellonlatbox,0,10,-44,-47 infile.nc infileregrid.nc  </br >

