openFoamMan
===========

manual for using OpenFOAM for ABL simulations

PyFoam installation
=====

1. Downaload the latest version of "PyFoam" from the link: http://openfoamwiki.net/index.php/Contrib_PyFoam
2. It will be a tar file. Untar the tar file in the folder of your choice
3. Open the command terminal and go to the folder in which you have untared the pyFoam file.
4. Using Synaptic Package manager install these two library files which are needed for pyFoam
  * libboost-dev
  * libboost-doc
5. In pyfoam folder you will see a set up file named "setup.py". In the terminal window type the command: ```sudo python setup.py install```
6. You are done with installation.

To check your installation,in the terminal type:
  ```
  python
  > import PyFoam
  > import PyFoam.FoamInformation
  > print PyFoam.FoamInstallation.foamTutorials()
  ```

This command should produce a output showing the openfoam tutorials directory.

turbulence modelling
====================

* realizableKE: http://foam.sourceforge.net/docs/cpp/a01830.html#details
* atmBoundaryLayerInletVelocity: http://foam.sourceforge.net/docs/cpp/a00058.html#details (used in 0/U)
* atmBoundaryLayerInletEpsilon: http://foam.sourceforge.net/docs/cpp/a00057.html (used in 0/epsilon)

Wall function settings: 

* nutkAtmRoughWallFunction: http://foam.sourceforge.net/docs/cpp/a01453.html#details (used in 0/nut)
* nutURoughWallFunction: http://foam.sourceforge.net/docs/cpp/a01457.html#details (not used)
* nutkRoughWallFunction: http://foam.sourceforge.net/docs/cpp/a01454.html#details (used in 0/k)
* epsilonWallFunction: http://foam.sourceforge.net/docs/cpp/a00547.html#details (not used, currently fixed value)
