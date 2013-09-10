openFoamMan
===========

manual for using OpenFOAM for ABL simulations

turbulence modelling
====================

* realizableKE: http://foam.sourceforge.net/docs/cpp/a01830.html#details
* atmBoundaryLayerInletVelocity: http://foam.sourceforge.net/docs/cpp/a00058.html#details (used in 0/U)
* atmBoundaryLayerInletEpsilon: http://foam.sourceforge.net/docs/cpp/a00057.html (used in 0/epsilon)

Wall function settings: 

* nutkAtmRoughWallFunction: http://foam.sourceforge.net/docs/cpp/a01453.html#details (used in 0/nut)
* nutURoughWallFunction: http://foam.sourceforge.net/docs/cpp/a01457.html#details (not used)
* nutkRoughWallFunction: http://foam.sourceforge.net/docs/cpp/a01454.html#details (used in 0/k)
