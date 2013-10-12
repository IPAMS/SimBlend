SimBlend
========

a [Blender](http://blender.org) module for the import of [SIMION](http://simion.com) ion trajectory data (in an very early state). 

## Installation
Copy the module in the "addons" folder of your Blender installation. Activate the module in the Addons Preferences (File -> User Preferences -> Addons). SimBlend is listed under "Import-Export". See the Blender documentation for details of the plugin system and module activation . 

## Usage
Once installed, SimBlend adds an import option under the Import menu (File -> Import -> SimBlend: SIMION Trajectories). A file dialog will come up, which allows to select a SIMION trajectory file, containing delimited ion trajectory data. 

The trajectory file has to be given as "delimited" SIMION log file, with at least the ion index, the ion mass, the X,Y,Z positions and  time of flight (TOF) recorded to the file. For an example of the file format see the files in the "examples" folder. 

Currently, SimBlend can import the trajectory data as animated spheres or tubes along the ion paths. The option to import ions as emitters of the Blender particle system is currently deactivated.
Note that individual materials are created in Blender according to the masses of the ions.

The import options are located in the Scene properties panel of Blender. The options are: 

+ **Object size:** Size of the object which represents an ion (sphere or tube diameter)
+ **Distance scale:** Scaling factor between the spatial coordinates of SIMION and Blender
+ **Number of frames:** Number of animated frames in an sphere animation
+ **Path tube vertrices:** Geometric resolution of the tubes along the paths
+ **Merged trajectory samples:** The spatial samples of the imported ion trajectories can be window-wise merged to smooth the trajectories or reduce the number of spatial samples. This is the window width, "5" each five samples in the SIMION data are combined to one sample in Blender
+ **Mark ion splat:** Switch if a marking object should be created at the terminal positions of the ions (ion splat positions)
+ **Animation Type:** Selection of the type of the ion representation

## Examples 
+ **Quadrupol_lowRes.rec** a low resolution version of the ion trajectories in a mass separating quadrupole geometry (quad example from the SIMION 8 examples)

## References / Literature
+ [Simblend - an open source visualization toolchain for SIMION](http://www.ptc.uni-wuppertal.de/uploads/media/MP279.pdf) poster, presented at the ASMS annual Meeting 2013 in Minneapolis

## Contact
[Physical and Theoretical Chemistry of the University of Wuppertal](http://www.ptc.uni-wuppertal.de)
