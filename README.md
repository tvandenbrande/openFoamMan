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

Settings of the model
====================

k-epsilon model:

* realizableKE: http://foam.sourceforge.net/docs/cpp/a01830.html#details

Inlet profile: 

* atmBoundaryLayerInletVelocity: http://foam.sourceforge.net/docs/cpp/a00058.html#details (used in 0/U)
* atmBoundaryLayerInletEpsilon: http://foam.sourceforge.net/docs/cpp/a00057.html (used in 0/epsilon)
* urbulentIntensityKineticEnergyInlet http://foam.sourceforge.net/docs/cpp/a02381.html#details (currently not used, constant k now)

Wall function settings: 

* nutkAtmRoughWallFunction: http://foam.sourceforge.net/docs/cpp/a01453.html#details (used in 0/nut)
* nutURoughWallFunction: http://foam.sourceforge.net/docs/cpp/a01457.html#details (not used)
* nutkRoughWallFunction: http://foam.sourceforge.net/docs/cpp/a01454.html#details (used in 0/k)
* epsilonWallFunction: http://foam.sourceforge.net/docs/cpp/a00547.html#details (not used, currently fixed value)

Details on discretisation:

* OpenFOAM manual: http://www.openfoam.org/docs/user/fvSchemes.php

Eulerian Multiphase models in OpenFOAM
======================================

* Kubilay et al. (2013): adjustments to the simple solver
* twoFaseEulerFoam http://www.tfd.chalmers.se/~hani/kurser/OS_CFD_2008/PraveenPrabhuBaila/Report_twoPhaseEuler.pdf
* details on programming in OpenFOAM:
   * code styling guide: http://openfoam.org/contrib/code-style.php
   * on creating solvers: http://www.openfoam.com/features/creating-solvers.php
   * Using functionobjects, like for example streamLine (http://foam.sourceforge.net/docs/cpp/a07932_source.html)
* details on the SIMPLE algorithm: http://openfoamwiki.net/index.php/OpenFOAM_guide/The_SIMPLE_algorithm_in_OpenFOAM
* details on fvc: http://openfoamwiki.net/index.php/Fvc_H
* details on the fvm/fvc namespace: http://openfoamwiki.net/index.php/Finite_volume_method_(OpenFOAM)
