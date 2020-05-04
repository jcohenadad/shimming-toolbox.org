# shaver

**Filetype:** _MATLAB&reg; function_

**Synopsis:** _shaves a 3D binary mask by 'R'_

    SHAVER convolves binary input image ROI with an ellipsoid defined by
    radius (or radii) R to return a contracted version of ROI

    Syntax

    ROIshaved = SHAVER(ROI,R)

    Description

    ROIshaved = SHAVER(ROI,R) returns ROI eroded by R. If R is a single
    scalar, every dimension is eroded by R. If R is a 3-component vector
    [Rx Ry Rz], each dimension is then eroded by its corresponding R value.
    

    see also DILATER( )

=========================================================================
Updated::20170210::ryan.topfer@polymtl.ca
=========================================================================


### Attributes


- nInputs : 2

- nOutputs : 1
