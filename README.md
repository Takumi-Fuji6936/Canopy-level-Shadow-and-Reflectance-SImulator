This readme file was generated on 2022-06-29 by Takumi Fujiwara and Wataru Takeuchi.

ORCID:https://orcid.org/0000-0001-5018-1776
Institution:Institute of Industrial Science, The University of Tokyo.
Email:takumifujiwara0121133@gmail.com


Title: 
Canopy-level Shadow and Reflectace Simulator (CSRS)


#CSRS
CSRS composed by three python programs.
>CSRS_parameter.py
>Create_virtualforst.py
>Compute_reflectance.py

CSRS_parameter.py is a parameter file for Create_virtualforest.py and Compute_reflectance.py.
Firstly, edite CSRS_parameter.py for your virtual forest.
Secondly, run "Create_virtualforst.py".
Thirdly, run "Compute_reflectance.py".

#Create_virtualforst.py
This program create virtual forests composed by point cloud.
The generated txt file has 8 attributes which is "x y z Nx Ny Nz Tree_ID material".
The numbers in "material" correspond to 0 for "Stem", 1 for "Canopy", and 2 for "Floor".
The result of run "Create_vitrualforest.py" is stored in /Test/CC_050/1_PointCloud/.

#Compute_reflectance.py
This program include five steps to simulate reflectance using virtual forest.
1: It's voxelize the point cloud of the virtual forest generated by Create_virtualforest.py.
2: Self Cast Shadow (SCS) will be computed in each voxel.
3: Cast Shadow (CS) will be computed in each voxel.
4: Ortho image will be generated.
Note, the size of the image is 10m x 10m smaller than the size of virtual forest.
If you set 50m-50m as size of virtual forest, outputed image size is 40m-40m.
5: reflectance will be computed.
The result of run "Compute_reflectance.py" is stored in /Test/Ellipsoid/CC_050/6_reflectance/0.
The each band of 1-3 in the image corresponds to SCS, CS, and reflectance of target wavelength.

#Requirement
- macOS  10.15.3
- python 3.7.4
- pandas 1.1.5
- numpy  1.16.0
- numba  0.51.2
- joblib 1.1.0
- gdal   2.3.3

#Citation

To cite package citation in publications use:
 
