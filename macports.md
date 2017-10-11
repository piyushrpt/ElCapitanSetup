### Manual installation of ports

- Install ports with ''sudo port install'' unless specified otherwise.

- Note that the gcc, python, postgresql versions evolve with time. Pick a consistent set for installing your ports


#### Basic C/C++ compiler
1. gcc5
  - sudo port select gcc mp-gcc5 (restart terminal)
  
#### Standard tools on a linux system  
2. cmake gmake bison gawk autoconf autoconf-archive
3. gconf coreutils automake pkgconfig dpkg ctags
4. tree unzip unrar szip p7zip gzip gnutar cabextract
5. gawk gsed
6. wget +ssl
7. xorg-libXt +flat_namespace
8. freetype tiff openmotif
9. subversion

#### Python versions
10. python27
   - sudo port select python python27
11. python36
   - sudo ln -s /opt/local/Library/Frameworks/Python.framework/Versions/3.6/bin/python3 /opt/local/bin/python3
   - sudo ln -s /opt/local/Library/Frameworks/Python.framework/Versions/3.6/include/python3.6m /opt/local/include/python3.6m
   
#### Useful computational stuff   
12. fftw +gcc5 fftw-single +gcc5
13. fftw-3 +gcc5 fftw-3-long +gcc5 fftw-3-single +gcc5
14. aria2 openldap
15. openmpi-default +gcc5 openmpi-gcc5 +fortran
   - sudo port select mpi openmpi-gcc5-fortran 
16. texlive +doc +full   (This is full LaTeX installation. Only needed if you plan to use LaTeX)
17. lapack +gfortran
18. eigen3 +blas +gcc5
19. gsl +gcc5
20. cgal sfcgal
21. bzr git rsync
22. hdf4 hdf5 hdfeos hdfeos5 h5utils
23. netcdf netcdf-cxx netcdf-fortran grib_api +gcc5
24. postgresql95 postgresql95-server
   - Follow instructions for setting up db that are displayed on the screen during installation
25. proj cairo scons pandoc
26. opencv +python27
27. gimp2 ImageMagick
28. samba3 swig swig-python

#### Python2-packages
29. py27-numpy +gcc5 (+atlas is recommended but port is often broken with this option)
30. py27-scipy +gcc5 (+atlas is recommended but port is often broken with this option)
31. py27-matplotlib +cairo +tkinter
32. py27-pandas py27-sympy py27-yaml py27-simplejson py27-Pillow
33. py27-ipython +notebook +parallel
   - sudo port select --set ipython py27-ipython
   - sudo port select --set ipython2 py27-ipython
34. gdal +curl +expat +geos +hdf4 +hdf5 +netcdf +openjpeg +postgresql95 +sqlite3
35. py27-gdal py27-cython py27-h5py
36. py27-lxml py27-networkx py27-shapely
37. py27-pygrib py27-pyproj py27-cartopy py27-fiona py27-matplotlib-basemap

#### Python3-packages
38. py36-numpy +gcc5
   - +atlas is recommended but port is often broken with this option
39. py36-scipy +gcc5
   - +atlas is recommended but port is often broken with this option
40. py36-matplotlib +cairo +tkinter py36-matplotlib-basemap
41. py36-pandas py36-sympy py36-yaml py36-simplejson
42. py36-h5py py36-cartopy py36-shapely py36-fiona py36-networkx
43. py36-ipython +notebook +parallel
   - sudo port select --set ipython3 py36-ipython
44. py36-mpi4py +gcc5 +openmpi

#### Other useful GIS stuff
45. gmt5 kealib pandoc
46. zmq py27-zmq py36-zmq
47. py36-bokeh py36-dynd py36-dask py36-sphinx py36-pip
48. postgis2 +gui +postgresql95 +raster +sfcgal +topology
49. py27-xmldiff wdiff cwdiff ndiff
50. qgis +postgresql95 +qt4
51. py27-backports-functools\_lru\_cache

### For petsc (massive matrix inversions)

1. atlas +gcc5
2. metis +gcc5
3. parmetis +gcc5 +openmpi
4. vecLibFort
5. suitesparse +gcc5 +metis +atlas
6. sundials +gcc5 +openmpi +atlas
7. superlu
8. superlu_dist +gcc5 +openmpi
9. hypre +gcc5 +openmpi
10. c2html
11. sowing
12. petsc +atlas +gcc5 +hypre +openmpi +parmetis +suitesparse +sundials +superlu +superlu_dist
   - export PETSC_DIR=/opt/local/lib/petsc

13. py36-petsc4py +gcc5 +openmpi
