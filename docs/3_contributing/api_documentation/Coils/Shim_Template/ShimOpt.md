# ShimOpt

**Filetype:** _MATLAB&reg; classdef_

**Synopsis:** _- Shim Optimization_

.......

Usage

Shim = ShimOpt( )
Shim = ShimOpt( Params )
Shim = ShimOpt( Params, Field )

Inputs (Optional)

    Field 
        A FieldEval-type object pertaining to the field map to be targetted by
        shimming.

    Params 
        A struct of parameters that can possess the following fields:

        .pathToShimReferenceMaps
            File path to .mat containing shim reference maps (ie basis fields) &
            .Hdr info

Outputs

    Shim possesses the following properties:

        .img
            Shim reference maps

        .Hdr
            Info Re: calibration data
            (e.g. Hdr.MaskingImage defines the spatial support of the ref maps)

        .Field
            As defined above in Inputs.
            Field can be supplied as an input during ShimOpt instantiation,
            or, at later point by calling Shim.setoriginalfield( Field ) ;

        .Aux
            .Shim
                When Shim does not itself refer to the scanner shims, then .Aux 
                is a ShimOpt object corresponding to the MRI host system.
        
        .Model
            .currents  
                Optimal shim current vector (i)
                [units A]

            .field     
                Optimal shim field from projection of i onto reference maps (Ai)
                [units Hz]

            .couplingCoefficients
                For realtime shimming, vector relating shim correction to
                respiratory state measurement (e.g. ProbeTracking.Data.p)
                [units: Hz/Pa (Probe), or Hz/rad (Nav) ]

            .dcCurrentsOffsets
                For realtime shimming, vector of "y-intercept" currents 
                (e.g currents when ProbeTracking.Data.p = 0)
                [units A]

        .System
            .currents
                
            .Specs
                Object of a type of ShimSpecs sub-class (e.g. ShimSpecs_IUGM_Prisma_fit) 

.......

NOTE

ShimOpt is a MaRdI subclass [ShimOpt < MaRdI]
      
=========================================================================
Author: ryan.topfer@polymtl.ca
=========================================================================

    Documentation for ShimOpt
       doc ShimOpt

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute            | Value |
|:--------------------:|:-----:|
| Hidden               | false |
| Sealed               | false |
| Abstract             | true  |
| Enumeration          | false |
| ConstructOnLoad      | false |
| HandleCompatible     | true  |
| RestrictsSubclassing | false |

- InferiorClasses : [N/A] 
- ContainingPackage : [N/A] 
- EventList : [N/A] 
- EnumerationMemberList : [N/A] 
- Superclasses: MaRdI
 
</details>

- - -
## Properties

 
-----
 
### Field

**Synopsis:** _- object of type FieldEval_

 Field -  object of type FieldEval

<details markdown="block">
<summary><b>Details</b></summary>
 
| Attribute     | Value |
|:-------------:|:-----:|
| Dependent     | false |
| Constant      | false |
| Abstract      | false |
| Transient     | false |
| Hidden        | false |
| GetObservable | false |
| SetObservable | false |
| AbortSet      | false |
| NonCopyable   | false |
| HasDefault    | false |

- GetAccess : public
- SetAccess : public
- PartialMatchPriority : [N/A] 
- GetMethod : 
- SetMethod : 
- DefaultValue : 
- Validation : [N/A] 
- DefiningClass : ShimOpt
 
</details>
 
-----
 
### Model

**Synopsis:** _- Modeled quantities for shimming_

 Model -  Modeled quantities for shimming 

<details markdown="block">
<summary><b>Details</b></summary>
 
| Attribute     | Value |
|:-------------:|:-----:|
| Dependent     | false |
| Constant      | false |
| Abstract      | false |
| Transient     | false |
| Hidden        | false |
| GetObservable | false |
| SetObservable | false |
| AbortSet      | false |
| NonCopyable   | false |
| HasDefault    | false |

- GetAccess : public
- SetAccess : public
- PartialMatchPriority : [N/A] 
- GetMethod : 
- SetMethod : 
- DefaultValue : 
- Validation : [N/A] 
- DefiningClass : ShimOpt
 
</details>
 
-----
 
### ShimmedField

**Synopsis:** _- object of type FieldEval_

 ShimmedField -  object of type FieldEval 

<details markdown="block">
<summary><b>Details</b></summary>
 
| Attribute     | Value |
|:-------------:|:-----:|
| Dependent     | false |
| Constant      | false |
| Abstract      | false |
| Transient     | false |
| Hidden        | false |
| GetObservable | false |
| SetObservable | false |
| AbortSet      | false |
| NonCopyable   | false |
| HasDefault    | false |

- GetAccess : public
- SetAccess : public
- PartialMatchPriority : [N/A] 
- GetMethod : 
- SetMethod : 
- DefaultValue : 
- Validation : [N/A] 
- DefiningClass : ShimOpt
 
</details>
 
-----
 
### System

**Synopsis:** _-_

 System - 

<details markdown="block">
<summary><b>Details</b></summary>
 
| Attribute     | Value |
|:-------------:|:-----:|
| Dependent     | false |
| Constant      | false |
| Abstract      | false |
| Transient     | false |
| Hidden        | false |
| GetObservable | false |
| SetObservable | false |
| AbortSet      | false |
| NonCopyable   | false |
| HasDefault    | false |

- GetAccess : public
- SetAccess : public
- PartialMatchPriority : [N/A] 
- GetMethod : 
- SetMethod : 
- DefaultValue : 
- Validation : [N/A] 
- DefiningClass : ShimOpt
 
</details>
 
-----
 
### Interpolant

**Synopsis:** _ShimOpt/Interpolant is a property._

<details markdown="block">
<summary><b>Details</b></summary>
 
| Attribute     | Value |
|:-------------:|:-----:|
| Dependent     | false |
| Constant      | false |
| Abstract      | false |
| Transient     | false |
| Hidden        | true  |
| GetObservable | false |
| SetObservable | false |
| AbortSet      | false |
| NonCopyable   | false |
| HasDefault    | false |

- GetAccess : public
- SetAccess : public
- PartialMatchPriority : [N/A] 
- GetMethod : 
- SetMethod : 
- DefaultValue : 
- Validation : [N/A] 
- DefiningClass : ShimOpt
 
</details>
 
-----
 
### img

**Synopsis:** _MaRdI/img is a property._

<details markdown="block">
<summary><b>Details</b></summary>
 
| Attribute     | Value |
|:-------------:|:-----:|
| Dependent     | false |
| Constant      | false |
| Abstract      | false |
| Transient     | false |
| Hidden        | false |
| GetObservable | false |
| SetObservable | false |
| AbortSet      | false |
| NonCopyable   | false |
| HasDefault    | false |

- GetAccess : public
- SetAccess : public
- PartialMatchPriority : [N/A] 
- GetMethod : 
- SetMethod : 
- DefaultValue : 
- Validation : [N/A] 
- DefiningClass : MaRdI
 
</details>
 
-----
 
### Aux

**Synopsis:** _MaRdI/Aux is a property._

<details markdown="block">
<summary><b>Details</b></summary>
 
| Attribute     | Value |
|:-------------:|:-----:|
| Dependent     | false |
| Constant      | false |
| Abstract      | false |
| Transient     | false |
| Hidden        | false |
| GetObservable | false |
| SetObservable | false |
| AbortSet      | false |
| NonCopyable   | false |
| HasDefault    | false |

- GetAccess : public
- SetAccess : public
- PartialMatchPriority : [N/A] 
- GetMethod : 
- SetMethod : 
- DefaultValue : 
- Validation : [N/A] 
- DefiningClass : MaRdI
 
</details>
 
-----
 
### Hdr

**Synopsis:** _- full Siemens DICOM header of 1st img (i.e. Img.img(:,:,1) )_

 Hdr -  full Siemens DICOM header of 1st img (i.e. Img.img(:,:,1) )

<details markdown="block">
<summary><b>Details</b></summary>
 
| Attribute     | Value |
|:-------------:|:-----:|
| Dependent     | false |
| Constant      | false |
| Abstract      | false |
| Transient     | false |
| Hidden        | false |
| GetObservable | false |
| SetObservable | false |
| AbortSet      | false |
| NonCopyable   | false |
| HasDefault    | false |

- GetAccess : public
- SetAccess : protected
- PartialMatchPriority : [N/A] 
- GetMethod : 
- SetMethod : 
- DefaultValue : 
- Validation : [N/A] 
- DefiningClass : MaRdI
 
</details>
 
-----
 
### Hdrs

**Synopsis:** _- cell array of (truncated) DICOM headers courtesy of dicominfo()_

 Hdrs -  cell array of (truncated) DICOM headers courtesy of dicominfo()

<details markdown="block">
<summary><b>Details</b></summary>
 
| Attribute     | Value |
|:-------------:|:-----:|
| Dependent     | false |
| Constant      | false |
| Abstract      | false |
| Transient     | false |
| Hidden        | false |
| GetObservable | false |
| SetObservable | false |
| AbortSet      | false |
| NonCopyable   | false |
| HasDefault    | false |

- GetAccess : public
- SetAccess : protected
- PartialMatchPriority : [N/A] 
- GetMethod : 
- SetMethod : 
- DefaultValue : 
- Validation : [N/A] 
- DefiningClass : MaRdI
 
</details>
 
-----
 
### Ref

**Synopsis:** _- Reference properties - prior to manipulation_

 Ref -  Reference properties - prior to manipulation

<details markdown="block">
<summary><b>Details</b></summary>
 
| Attribute     | Value |
|:-------------:|:-----:|
| Dependent     | false |
| Constant      | false |
| Abstract      | false |
| Transient     | false |
| Hidden        | true  |
| GetObservable | false |
| SetObservable | false |
| AbortSet      | false |
| NonCopyable   | false |
| HasDefault    | false |

- GetAccess : public
- SetAccess : protected
- PartialMatchPriority : [N/A] 
- GetMethod : 
- SetMethod : 
- DefaultValue : 
- Validation : [N/A] 
- DefiningClass : MaRdI
 
</details>

---
## Methods


---


### tableshim

**Synopsis**: _Table of shim terms_ 

T = TABLESHIM( Shim )
T = TABLESHIM( Shim, Corrections )

When the only input argument is a ShimOpt-type object, T is a table where
the first column contains the shim terms (channel names), and the second column
contains their current setting.

e.g. T =

Correction_Term  | Original
    Tx Freq. [Hz]  | 123259218
     Ch.1    [A]   |    0
          .        |    .
          .        |    .
          .        |    .
     Ch.N    [A]   |    0

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Shim, Corrections
- OutputNames : T
- DefiningClass : ShimOpt
 
</details>

---


### optimizeshimcurrents

**Synopsis**: _OPTIMIZESHIMCURRENTS_ 

Corrections = OPTIMIZESHIMCURRENTS( Shim, Params )

Corrections.static

Corrections.realtime

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Shim, Params
- OutputNames : Corrections
- DefiningClass : ShimOpt
 
</details>

---


### optimizelarmor

**Synopsis**: _OPTIMIZELARMOR_ 


[f0, f0Voi, f0VoiShimmed] = OPTIMIZELARMOR( Shim, voi )

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Shim, voi
- OutputNames : f0, f0Voi, f0VoiShimmed
- DefiningClass : ShimOpt
 
</details>

---


### predictshimmedriro

**Synopsis**: _PREDICTSHIMMEDRIRO_ 

[PredictedRiro] = PREDICTSHIMMEDRIRO( Shim ) ;
[PredictedRiro] = PREDICTSHIMMEDRIRO( Shim, dp ) ;

Returns a FieldEval-type object

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Shim, p
- OutputNames : PredictedRiro
- DefiningClass : ShimOpt
 
</details>

---


### predictshimmedfield

**Synopsis**: _PREDICTSHIMMEDFIELD_ 

[PredictedField] = PREDICTSHIMMEDFIELD( Shim ) ;

Returns FieldEval-type object(s)

PredictedField.img = ( Shim.Field.img + Shim.Model.field ) ;

NOTE
    The regions of spatial support for Shim.Model.field and Shim.Field.img 
    are likely somewhat different (though ideally overlapping!).
    The predictions do not account for the finite spatial support of 
    either field term!

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Shim
- OutputNames : PredictedField
- DefiningClass : ShimOpt
 
</details>

---


### predictslicewiseshim

**Synopsis**: _PREDICTSLICEWISESHIM_ 

TEMPORARY FUNCTION FOR SAGITTAL FIELD MAPS:
    --> Decompose global shim voi into axial segments and shim segments individually

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Shim, Params
- OutputNames : [N/A] 
- DefiningClass : ShimOpt
 
</details>

---


### computerealtimeupdate

**Synopsis**: _COMPUTEREALTIMEUPDATE_ 

Usage

currents = COMPUTEREALTIMEUPDATE( Shim, p )

    currents = Shim.Model.currents + p*Shim.Model.couplingCoefficients ;

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Shim, p
- OutputNames : currents
- DefiningClass : ShimOpt
 
</details>

---


### getshimsupport

**Synopsis**: _GETSHIMSUPPORT_ 

shimSupport = GETSHIMSUPPORT( Shim ) ;

    shimSupport is a logical map over the grid (voxel positions) defined by
    Shim.img of where the shim reference maps have well defined values.

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Shim
- OutputNames : shimSupport
- DefiningClass : ShimOpt
 
</details>

---


### getnactivechannels

**Synopsis**: _GETNACTIVECHANNELS_ 

Returns number of active shim channels

nActiveChannels = GETNACTIVECHANNELS( Shim ) ;

nActiveChannels = size( Shim.img, 4 ) ;

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Shim
- OutputNames : nActiveChannels
- DefiningClass : ShimOpt
 
</details>

---


### getshimoperator

**Synopsis**: _GETSHIMOPERATOR_ 

A = GETSHIMOPERATOR( Shim ) ;

    where A * vectorOfShimCurrents = shimField

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Shim
- OutputNames : A
- DefiningClass : ShimOpt
 
</details>

---


### gettruncationoperatorriro

**Synopsis**: _GETTRUNCATIONOPERATORRIRO_ 

M = GETTRUNCATIONOPERATORRIRO( Shim ) ;

Returns sparse linear truncation operator M
i.e. M*b, 'picks out' the VOI voxels from vector b
where the VOI is defined by the full 3d array Shim.Field.Model.Riro.Hdr.MaskingImage

if b has length nImg, and nVoi is the # of non-zero VOI voxels, then length(M*b)=nVoi.

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Shim
- OutputNames : M
- DefiningClass : ShimOpt
 
</details>

---


### gettruncationoperator

**Synopsis**: _GETTRUNCATIONOPERATOR_ 

M = GETTRUNCATIONOPERATOR( Shim ) ;

Returns sparse linear truncation operator M
i.e. M*b, 'picks out' the VOI voxels from vector b
where the VOI is defined by the full 3d array Shim.Field.Hdr.MaskingImage

if b has length nImg, and nVoi is the # of non-zero VOI voxels, then length(M*b)=nVoi.

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Shim
- OutputNames : M
- DefiningClass : ShimOpt
 
</details>

---


### setupdateoperator

**Synopsis**: _SETUPDATEOPERATOR_ 

[] = SETUPDATEOPERATOR( Shim ) ;

Calls Shim.getupdateoperator() to set field Shim.Model.updateOperator

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Shim
- OutputNames : [N/A] 
- DefiningClass : ShimOpt
 
</details>

---


### getvaliditymask

**Synopsis**: _GETVALIDITYMASK_ 

Returns binary mask - TRUE where field values are well defined and within
the expected range and where (interpolated) shim reference maps are well
defined.

mask = GETVALIDITYMASK( Shim, Fields )
mask = GETVALIDITYMASK( Shim, Fields, Params )

Fields : a cell array of FieldEval-type objects
(e.g. may correspond to 'Inspired' and/or 'Expired' fields.)

.......................
    
The following Params.fields are supported

.maxAbsField
    maximum absolute voxel value assumed to represent an accurate field
    measurement. Voxels with abs-values greater than this might stem from
    errors in the unwrapping.  [default: 500 Hz]
    (To ignore this criterion, set value to Inf)

.isAuxIncluded
    true || false, account for spatial support of the Shim.Aux system?

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Shim, Fields, Params
- OutputNames : mask
- DefiningClass : ShimOpt
 
</details>

---


### getupdateoperator

**Synopsis**: _GETUPDATEOPERATOR_ 

UO = GETUPDATEOPERATOR( Shim ) ;

    where UO * respiratory_measurement = currentsUpdate

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Shim
- OutputNames : UO
- DefiningClass : ShimOpt
 
</details>

---


### forwardmodelshimcorrection

**Synopsis**: _FORWARDMODELSHIMCORRECTION_ 

shimCorrection = FORWARDMODELSHIMCORRECTION( Shim, correctionCoefficients ) ;

Forward projection of the shim correction :

shimCorrection = reshape( Shim.getshimoperator()*correctionCoefficients, Shim.Field.getgridsize() ) ;

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Shim, correctionCoefficients
- OutputNames : shimCorrection
- DefiningClass : ShimOpt
 
</details>

---


### setshimvolumeofinterestriro

**Synopsis**: _SETSHIMVOLUMEOFINTERESTRIRO_ 

[] = SETSHIMVOLUMEOFINTERESTRIRO( Shim, mask )

Sets Shim.Field.Model.Riro.Hdr.MaskingImage

mask is a binary image (with the same dimensions as Shim.Field.Model.Riro.img) of
the desired shim region.

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Shim, mask
- OutputNames : [N/A] 
- DefiningClass : ShimOpt
 
</details>

---


### setshimvolumeofinterest

**Synopsis**: _SETSHIMVOLUMEOFINTEREST_ 

[] = SETSHIMVOLUMEOFINTEREST( Shim, mask )

Sets Shim.Field.Hdr.MaskingImage

mask is a binary image (with the same dimensions as Shim.Field.img) of
the desired shim region.

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Shim, mask
- OutputNames : [N/A] 
- DefiningClass : ShimOpt
 
</details>

---


### setshimmedfield

**Synopsis**: _SETSHIMMEDFIELD_ 

[] = SETSHIMMEDFIELD( Shim, Field )

Sets Shim.ShimmedField

Field is a FieldEval type object with .img in Hz

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Shim, Field
- OutputNames : [N/A] 
- DefiningClass : ShimOpt
 
</details>

---


### setoriginalfield

**Synopsis**: _SETORIGINALFIELD_ 

[] = SETORIGINALFIELD( Shim, Field )
[] = SETORIGINALFIELD( Shim, Field, currents )

Sets Shim.Field

Field is a FieldEval type object with .img in Hz

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Shim, Field, currents
- OutputNames : [N/A] 
- DefiningClass : ShimOpt
 
</details>

---


### setdccurrentoffsets

**Synopsis**: _ShimOpt/setdccurrentoffsets is a function._ 

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Shim, currentsInspired, currentsExpired, pInspired, pExpired
- OutputNames : [N/A] 
- DefiningClass : ShimOpt
 
</details>

---


### setcouplingcoefficients

**Synopsis**: _ShimOpt/setcouplingcoefficients is a function._ 

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Shim, currentsInspired, currentsExpired, pInspired, pExpired
- OutputNames : [N/A] 
- DefiningClass : ShimOpt
 
</details>

---


### calibraterealtimeupdates

**Synopsis**: _CALIBRATEREALTIMEUPDATES_ 

CALIBRATEREALTIMEUPDATES asks user to select the intervals of a pair of
respiratory recordings (e.g. ProbeTracking.Data.t ) corresponding to inspired
and expired field maps acquisitions.

From these, and the associated optimal currents for the 2 respiratory states,
the following function calls are made:

--> Shim.Opt.setcouplingcofficients()
--> Shim.Opt.setdccurrentoffsets()
--> Shim.Opt.setupdateoperator()


Usage

Params = CALIBRATEREALTIMEUPDATES( Shim, Params )

    Params.
        .Inspired
            .currents
            .measurementLog

        .Expired
            .currents
            .measurementLog

The returned Params struct has additional fields (Params.Inspired.medianP,
and Params.Expired.medianP) corresponding to the user-selected medians (e.g.
pressures)

NOTE : Possibly deprecated

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Shim, Params
- OutputNames : Params
- DefiningClass : ShimOpt
 
</details>

---


### resettoreference

**Synopsis**: _RESETTOREFERENCE_ 

RESETTOREFERENCE( Shim )

Returns Shim.img and Shim.Hdr to their original (reference) values (before
interpolations, cropping etc.)

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Shim
- OutputNames : [N/A] 
- DefiningClass : ShimOpt
 
</details>

---


### delete

**Synopsis**: _DELETE_ 

clear Shim

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Shim
- OutputNames : [N/A] 
- DefiningClass : ShimOpt
 
</details>

---


### assessshim

**Synopsis**: _ASSESSSHIM_ 


ASSESSSHIM( Shim )

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Shim, voi
- OutputNames : Results
- DefiningClass : ShimOpt
 
</details>

---


### ShimOpt

**Synopsis**: _Constructor_ 

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : varargin
- OutputNames : Shim
- DefiningClass : ShimOpt
 
</details>

---


### mapdbdi

**Synopsis**: _map dB/dI : field shift [Hz] per unit current (A)_ 


[ img, Hdr ] = MAPDBDI( Params )

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | true  |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Params
- OutputNames : img, Hdr
- DefiningClass : ShimOpt
 
</details>

---


### derivedataweights

**Synopsis**: _DERIVEDATAWEIGHTS_ 

dataWeights = DERIVEDATAWEIGHTS( Mag, targetEchoTime )
dataWeights = DERIVEDATAWEIGHTS( Mag, targetEchoTime, targetMask )

Assumes basic model of T2* signal decay using the magnitude images of the
2 echoes in the dual-echo GRE

if: Mag(TE) = M0 * exp(-TE/T2star)
then:
t2star  = -deltaTe ./ log( Mag2.img ./ Mag1.img ) ;

dataWeights is the predicted + normalized signal intensity at the targetEchoTime
(e.g. a long TE for a GRE-EPI sequence).

targetMask, if provided, is a logical array specifying a priority region
(e.g. spinal canal) that will receive maximal (unity) weighting in dataWeights,
irrespective of the t2*-forecasted signal.
(i.e. dataWeights( targetMask ) = 1 ;)

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | true  |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Mag, targetEchoTime, targetMask
- OutputNames : dataWeights
- DefiningClass : ShimOpt
 
</details>

---


### parseinput

**Synopsis**: _PARSEINPUT_ 

Simple parser returns the optional user inputs Field and Params irrespective
of their input order (convenient).

[ Field, Params ] = PARSEINPUT( Inputs )

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | true  |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | true  |

- Access : public
- InputNames : Inputs
- OutputNames : Field, Params
- DefiningClass : ShimOpt
 
</details>

---


### calibratereferencemaps

**Synopsis**: _CALIBRATEREFERENCEMAPS_ 

Wraps to ShimOpt.mapdbdi( ) and writes output to disk

[ img, Hdr ] = CALIBRATEREFERENCEMAPS( Params )

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | true  |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | true  |

- Access : public
- InputNames : Params
- OutputNames : img, Hdr
- DefiningClass : ShimOpt
 
</details>

---


### assigndefaultparameters

**Synopsis**: _ASSIGNDEFAULTPARAMETERS_ 

Params = ASSIGNDEFAULTPARAMETERS( Params )

Add default parameters fields to Params without replacing values (unless empty)

DEFAULT_PATHTOSHIMREFERENCEMAPS = [] ;
DEFAULT_INSTITUTIONNAME         = 'IUGM' ;
DEFAULT_STATIONNAME             = 'MRC35049' ;

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | true  |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | true  |

- Access : public
- InputNames : Params, Specs
- OutputNames : Params
- DefiningClass : ShimOpt
 
</details>

---


### loadshimreferencemaps

**Synopsis**: _LOADSHIMREFERENCEMAPS_ 


[ img, Hdr, Interpolant ] = LOADSHIMREFERENCEMAPS( filename )

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | true  |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : pathToShimReferenceMaps
- OutputNames : img, Hdr, Interpolant
- DefiningClass : ShimOpt
 
</details>

---


### empty

**Synopsis**: _Returns an empty object array of the given size_ 

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | true  |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | true  |

- Access : public
- InputNames : varargin
- OutputNames : E
- DefiningClass : ShimOpt
 
</details>

---


### write

**Synopsis**: _Ma(t)-R-dI(com)_ 

Write MaRdI image object to DICOM and/or NifTI

.....

    Usage 

    WRITE( Img )
    WRITE( Img, saveDirectory )
    WRITE( Img, saveDirectory, imgFormat ) 
    WRITE( Img, saveDirectory, imgFormat, isSavingSingleNiis ) 

    Inputs

    default saveDirectory = './tmp'
    
    imgFormat can be:
        'dcm' [default]
        'nii' (creating temporary DICOMs which are deleted after the system call to dcm2niix)
        'both' (does not delete the DICOMs)

    isSavingSingleNiis (boolean):
        false [default] : DICOMs are combined into single NifTI file
        true : Separate .nii output for each image (passes '-s y' argument to dcm2niix)

.....

Adapted from dicom_write_volume.m (D.Kroon, University of Twente, 2009)
https://www.mathworks.com/matlabcentral/fileexchange/27941-dicom-toolbox?focused=5189263&tab=function

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Img, saveDirectory, imgFormat, isSavingSingleNiis
- OutputNames : [N/A] 
- DefiningClass : MaRdI
 
</details>

---


### unwrapphase

**Synopsis**: _UNWRAPPHASE_ 

Interface to SUNWRAP, to FSL Prelude, or to Abdul-Rahman's path-based phase unwrapper

.......
    
Usage

    [] = UNWRAPPHASE( Phase )
    [] = UNWRAPPHASE( Phase, Mag )
    [] = UNWRAPPHASE( Phase, Mag, Options )
    
    Phase and Mag are objects of type MaRdI.

    Options is a struct that can contain the following fields:

    .unwrapper 
        == 'AbdulRahman_2007' [default if Phase.img is 3D] : 
            calls UNWRAP3D. 
            Not permitted if Phase.img is 2D (will default to SUNWRAP)
            If Mag is supplied, Phase.Hdr.MaskingImage must
            See HELP UNWRAP3D for description of permitted Options 

        == 'Sunwrap' [default if Phase.img is 2D] : 
            calls SUNWRAP. See HELP SUNWRAP for more details.

        == 'FslPrelude' : calls PRELUDE. 
            See HELP PRELUDE for description of permitted Options 

    .threshold  [default = 0.01] 
        Relative threshold of Mag.img used to define the unwrapping region in
        the SUNWRAP case and for the other 2 cases when Phase.Hdr.MaskingImage
        is undefined (Mag.getreliabilitymask() is called).

    NOTE: UNWRAP3D and PRELUDE support an Options.mask input to which
    Phase.Hdr.MaskingImage will always be assigned. To assign the mask
    manually, run Phase.setmaskingimage before calling Phase.unwrapphase.

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Phase, varargin
- OutputNames : [N/A] 
- DefiningClass : MaRdI
 
</details>

---


### timestd

**Synopsis**: _TIMESTD_ 

standardDeviation = TIMESTD( Img )

Assumes 5th dimension of Img.img corresponds to time:
    
    standardDeviation = std( Img.img, 0, 5 ) ;

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Img
- OutputNames : timeStd
- DefiningClass : MaRdI
 
</details>

---


### timeaverage

**Synopsis**: _TIMEAVERAGE_ 

Img = TIMEAVERAGE( Img)

Assumes 5th dimension of Img.img corresponds to time:
    
    timeAverage = mean( Img.img, 5 ) ;

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Img
- OutputNames : timeAverage
- DefiningClass : MaRdI
 
</details>

---


### setmaskingimage

**Synopsis**: _SETMASKINGIMAGE_ 

[] = SETMASKINGIMAGE( Img, mask )

Copies valid mask (a logical array of 1's and 0's) to Img.Hdr.MaskingImage

The purpose of this function is to specify the signal spatial support (e.g.
of mag, phase, field data) within the image grid. e.g. it is called during
phase unwrapping/field mapping, but it might also be called prior to regridding
if the interpolation should exclude certain voxels.

To be valid, mask must either be the same size as Img.img OR the same size as
Img.getgridsize() (i.e. the size of a single image volume of a
multi-echo/multi-measurement stack), in which case, the single mask is simply
copied such that the assigned Img.Hdr.MaskingImage always possesses the same
dimensions as Img.img

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Img, mask
- OutputNames : [N/A] 
- DefiningClass : MaRdI
 
</details>

---


### segmentspinalcanal

**Synopsis**: _SEGMENTSPINALCANAL_ 

segment T2* multiecho data using the Spinal Cord Toolbox (must be installed + in path)

[ mask, weights ] = SEGMENTSPINALCANAL( Img, Params )

Params

    .dataLoadDir 
        DICOM folder
    
    .dataSaveDir 

    .isUsingPropsegCsf
        [default = false]

NOTE
    The protocol is basically that of Topfer R, et al. Magn Reson Med, 2018. 
    It hasn't been tested extensively for different acquisition prtocols/systems

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Img, Params
- OutputNames : mask, weights
- DefiningClass : MaRdI
 
</details>

---


### resliceimg

**Synopsis**: _RESLICEIMG_ 

Interpolate a MaRdI image (Img.img) and update Img.Hdr accordingly.

In general, RESLICEIMG() uses MATLAB's scatteredInterpolant class.
The exception is when the image input (Img.img) is 2d and the target
output (prescribed by inputs X,Y,Z) is a volume. This scenario is
incompatible with scatteredInterpolant, and nearest-neighbor substitution is
used instead.

-----
Basic Usage

[] = RESLICEIMG( Img, X, Y, Z )
[] = RESLICEIMG( Img, X, Y, Z, mask )

Inputs:

X, Y, Z:
        2d or 3d arrays (size=output image grid) describing the X, Y, Z patient
        coordinates (i.e. of the DICOM reference coordinate system) of the
        target (output) voxels. In general, if one is interpolating from one
        image grid (Img) to another (MaRdI-type object Img2), these arrays are
        obtained by the call: [X,Y,Z] = Img2.getvoxelpositions()

mask: [Optional, default = true(size output image grid)]
        A logical array (size=output image grid) specifying the subset of the
        output voxels that are of interest. (i.e. voxels in the output image
        with a corresponding mask entry == FALSE will simply be assigned zero).
        Note: Specifying the region of interest for extrapolation with this
        variable can greatly accelerate the interpolation!

-----

Advanced Usage TODO

    [F] = RESLICEIMG( Img, X, Y, Z, mask, F ) 

    case:
        interpolationMethod [default='linear']
        is a string supported by the scatteredInterpolant constructor.
    F is the object of type 'scatteredInterpolant' used for interpolation.

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Img, X_Ep, Y_Ep, Z_Ep, varargin
- OutputNames : F
- DefiningClass : MaRdI
 
</details>

---


### isocenter

**Synopsis**: _ISOCENTER_ 

xyzIso = ISOCENTER( Img )

Returns the 3-element vector of the x, y and z coordinates of the magnet
isocenter in the patient coordinate system

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Img
- OutputNames : xyzIso
- DefiningClass : MaRdI
 
</details>

---


### isphase

**Synopsis**: _Returns TRUE if Img is a phase image, FALSE otherwise._ 


isPhase = ISPHASE( Img )

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Img
- OutputNames : isPhase
- DefiningClass : MaRdI
 
</details>

---


### ismagnitude

**Synopsis**: _Returns TRUE if Img is a magnitude image, FALSE otherwise._ 


isMag = ISMAGNITUDE( Img )

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Img
- OutputNames : isMag
- DefiningClass : MaRdI
 
</details>

---


### getvoxelspacing

**Synopsis**: _GETVOXELSPACING_ 

h = GETVOXELSPACING( Img )
        
Returns 3-component grid-spacing vector [units: mm]:

    h(1) : row spacing (between centers of adjacent rows, i.e. vertical spacing). 

    h(2) : column spacing (between the centers of adjacent columns,
    i.e. horizontal spacing).    

    h(3) : slice spacing (between the centers of adjacent slices, i.e.
    from the DICOM hdr, this is Hdr.SpacingBetweenSlices - for a 2D acquisition
    this not necessarily the same as Hdr.SliceThickness).

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Img
- OutputNames : h
- DefiningClass : MaRdI
 
</details>

---


### getvoxelpositions

**Synopsis**: _GETVOXELPOSITIONS_ 

[X,Y,Z] = GETVOXELPOSITIONS( Img )

    Returns three 3D arrays of doubles, each element containing the
    location [units: mm] of the corresponding voxel with respect to 
    DICOM's 'Reference Coordinate System'.

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Img
- OutputNames : X, Y, Z
- DefiningClass : MaRdI
 
</details>

---


### getreliabilitymask

**Synopsis**: _GETRELIABILITYMASK_ 

mask = getreliabilitymask( Mag )
mask = getreliabilitymask( Mag, threshold )

For each echo and each measurement, GETRELIABILITYMASK normalizes
Mag.img(:,:,:,iEcho,iMeasurement) and returns a logical mask wherein
elements are assigned TRUE whenever the corresponding normalized magnitude
voxel is > threshold

By default, threshold = 0.01

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Mag, threshold
- OutputNames : mask
- DefiningClass : MaRdI
 
</details>

---


### getnumberofvoxels

**Synopsis**: _GETNUMBEROFVOXELS_ 

 GETNUMBEROFVOXELS

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Img
- OutputNames : nVoxels
- DefiningClass : MaRdI
 
</details>

---


### getgyromagneticratio

**Synopsis**: _GETGYROMAGNETICRATIO_ 

Gyro = getgyromagneticratio( Img )

Examines .Hdr of MaRdI-type Img for .ImagedNucleus and returns gyromagnetic
ratio in units of rad/s/T.

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Img
- OutputNames : GYRO
- DefiningClass : MaRdI
 
</details>

---


### getgridsize

**Synopsis**: _Image dimensions as 3-element vector (rows, columns, slices)_ 


gridSize = GETGRIDSIZE( Img )

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Img
- OutputNames : gridSize
- DefiningClass : MaRdI
 
</details>

---


### getfieldofview

**Synopsis**: _GETFIELDOFVIEW_ 

fov = GETFIELDOFVIEW( Img ) ;

Returns field of view in units of mm : [Row Column Slice] dimensions

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Img
- OutputNames : fieldOfView
- DefiningClass : MaRdI
 
</details>

---


### getechotime

**Synopsis**: _GETECHOTIME_ 

TE = GETECHOTIME( Img )
TE = GETECHOTIME( Img, iEcho )

Returns vector of echo times in units of ms.
If 2nd argument (echo index iEcho) is provided, GETECHOTIME returns the TE of
the corresponding echo.

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Img, iEcho
- OutputNames : echoTime
- DefiningClass : MaRdI
 
</details>

---


### getpartialfourierfactors

**Synopsis**: _Returns fraction of k-space coverage in each dim_ 

pff = GETPARTIALFOURIERFACTORS( Img )

Returns 3-element vector of partial Fourier factors in read, phase (in-plane),
and partition (slice) encoding directions.

NOTE:
Siemens uses an enumeration scheme to store Partial Fourier info in the DICOM header:

pff --> Siemens DICOM Hdr entry
4/8 --> 0x1  = 1
5/8 --> 0x2  = 2
6/8 --> 0x4  = 4
7/8 --> 0x8  = 8
8/8 --> 0x10 = 16 (i.e. no partial Fourier)

See: https://github.com/malaterre/GDCM/blob/master/Source/DataDictionary/CSAHeader.xml

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Img
- OutputNames : pff
- DefiningClass : MaRdI
 
</details>

---


### getnumberofslices

**Synopsis**: _Returns number of acquired slices_ 

nSlices = GETNUMBEROFSLICES( Img )

NOTE: nSlices is not necessarily equal to size( Img.img, 3).
e.g. For a 3d (slab) encoding, GETNUMBEROFSLICES returns 1.

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Img
- OutputNames : nSlices
- DefiningClass : MaRdI
 
</details>

---


### getnumberofmeasurements

**Synopsis**: _Returns the number of measurements_ 

n = GETNUMBEROFMEASUREMENTS( Img )

NOTE

GETNUMBEROFMEASUREMENTS( Img ) is equivalent to n = size( Img.img, 5 ),
however GETNUMBEROFMEASUREMENTS also checks the DICOM header in Img.Hdr and
issues a warning if n differs from the expected value
(Img.Hdr.MrProt.lRepetitions +1).

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Img
- OutputNames : nVolumes
- DefiningClass : MaRdI
 
</details>

---


### getimagetype

**Synopsis**: _Returns image type as string_ 

imgType = GETIMAGETYPE( Img )

Returns either 'PHASE', 'MAGNITUDE', or 'UNKNOWN'

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Img
- OutputNames : imgType
- DefiningClass : MaRdI
 
</details>

---


### getimagingfrequency

**Synopsis**: _Returns Larmor frequency in Hz_ 


f0 = GETIMAGINGFREQUENCY( Img ) ;

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Img
- OutputNames : f0
- DefiningClass : MaRdI
 
</details>

---


### getacquisitiontime

**Synopsis**: _GETACQUISITIONTIME_ 

t = GETACQUISITIONTIME( Img )

Derives from the AcquisitionTime field in Siemens DICOM header to return
an array of doubles describing the milliseconds elapsed since midnight

dimensions of t: [ nSlices x nEchoes x nMeasurements ]

t - t(1) yields the elapsed time since acquisition of the 1st k-space point
in the series.

For EPI MOSAIC (which has a single AcquisitionTime value for each volume),
t( iSlice ) = AcquisitionTime (first slice) + iSlice*(volumeTR/nSlices)

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Img
- OutputNames : t
- DefiningClass : MaRdI
 
</details>

---


### filter

**Synopsis**: _FILTER_ 

3D low-pass (weighted or unweighted) or median filtering.
Wraps to smooth3() or medfilt3() accordingly.

[] = FILTER( Img )
[] = FILTER( Img, weights )
[] = FILTER( Img, weights, Params )

Img
    the MaRdI-type image volume.

weights
    an array of data weights (>=0) to penalize (for smooth3) or exclude (for
    medfilt3()) identifiable outliers.  Dimensions of weights must be the
    same as the image volume (i.e. Img.getgridsize() )

Params
    an optional struct for which the following Params.fields are supported

    .kernelSize
        in number of voxels
        default = [3 3 3] 

    .method
        'gaussian' OR 'box' OR 'median'
        default = 'gaussian'


TODO
    Add support for 2d (single slice) images

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Img, weights, Params
- OutputNames : [N/A] 
- DefiningClass : MaRdI
 
</details>

---


### exist

**Synopsis**: _EXIST_ 

 EXIST

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Img
- OutputNames : is
- DefiningClass : MaRdI
 
</details>

---


### estimatekorigintime

**Synopsis**: _ESTIMATEKORIGINTIME_ 

t0 = ESTIMATEKORIGINTIME( Img )

Returns an estimate of when the k-space origin of an image was sampled
relative to the AcquisitionTime (field in Siemens DICOM header) as a double
in units of milliseconds.

See also: MaRdI.getacquisitiontime()

NOTE: This is a crude estimate and only the case of Cartesian k-space
sampling, beginning at the k_min periphery, has been considered in the
current implementation!

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Img
- OutputNames : t0
- DefiningClass : MaRdI
 
</details>

---


### copy

**Synopsis**: _COPY_ 

Make a copy of a MaRdI (i.e. handle) object.

ImgCopy = Copy( Img ) ;

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Img
- OutputNames : ImgCopy
- DefiningClass : MaRdI
 
</details>

---


### associateaux

**Synopsis**: _- link image to corresponding auxiliary recording object_ 

Usage

    [] = ASSOCIATEAUX( Img, Aux )
    [] = ASSOCIATEAUX( Img, Aux, Params )

.......

Description
    
Function compares an acquired image (typically, a time-series of multiple
images) and an auxiliary recording (e.g. respiratory trace, ideally
featuring synchronization triggers) and returns (copies to Img.Aux) an
estimate of the Aux recording corresponding to each image measurement.

Cases:
    
    1. Single measurement Aux:
        The value is copied across all image time points

    2. Single measurement Img:
        If Aux possesses multiple measurements, the image is presumed to have
        been taken during a breath-hold. In this case, the Aux signal variance
        is calculated over a shifting time-window (width = total image
        acquisition time) and the median Aux value over the window pertaining
        to the least variance is returned. (Length of Aux recording must be >=
        total scan time).

    3. Img and Aux are both time-series:
        Length of Aux recording must be >= length of the image time-series.

        3.0: Img and Aux time-points already correspond: 
             Aux is simply copied. 

        3.1: Aux recording possesses a single synchronization trigger:
            The trigger is assumed to correspond to the first image in the time series.
            Aux is cropped and linearly interpolated.

        3.2: Aux recording possesses multiple synchronization triggers:
            NOT IMPLEMENTED

        3.3: Aux recording does not possess triggers:
            DEPRECATED 
.......

Params - optional struct for which the following Params.fields are supported

Only used in Case 3 (image time series):

    .interpolationMethod    [default = 'linear']
        argument to INTERP1(), used to interpolate between Aux samples
        (see INTERP1 for other options)

    .auxDelay   [default = 0]
        estimation of transmission delay inherent in the Aux recording process [units: ms]

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Img, Aux, Params
- OutputNames : [N/A] 
- DefiningClass : MaRdI
 
</details>

---


### adjvalidateshim

**Synopsis**: _ADJVALIDATESHIM_ 

[f0, g0, s0] = ADJVALIDATESHIM( Img )

ADJVALIDATESHIM is not a particularly revealing name for a function; however,
it is based on the Siemens AdjValidate commandline tool, with a "-shim" input
argument.

f0 = scalar Larmor (Tx) freq. [ units : Hz ]
g0 = 3-element vector of the linear gradient offsets (gX, gY, gZ) [units : DAC bits]
s0 = 5-element vector of 2nd order shim currents [units : mA]

To convert to the units of the 3D Shim card on the Siemens (Prisma) console,
see
ShimSpecs_IUGM_Prisma_fit.converttomultipole( )
ShimSpecs_HGM_Prisma_fit.converttomultipole( )

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Img
- OutputNames : f0, g0, s0
- DefiningClass : MaRdI
 
</details>

---


### scalephasetofrequency

**Synopsis**: _SCALEPHASETOFREQUENCY_ 

Converts unwrapped phase [units:rad] to field [units: Hz]

    Field = scalephasetofrequency( UnwrappedPhase )
    Phase = scalephasetofrequency( Field, -1 )
    
    The 'undo' mode with -1 as the 2nd argument scales from Hz back to rad

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : protected
- InputNames : Img, undoFlag
- OutputNames : [N/A] 
- DefiningClass : MaRdI
 
</details>

---


### iscoincident

**Synopsis**: _Check coincidence of 2 images_ 

isSame = ISCOINCIDENT( Img1, Img2 )

Returns TRUE if Img1 and Img2 possess coincident voxel positions
and number of measurements/volumes

TODO: Check additional properties + add outputs for each?

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : protected
- InputNames : Img1, Img2
- OutputNames : isSame
- DefiningClass : MaRdI
 
</details>

---


### getinterpolant

**Synopsis**: _Return object of type scatteredInterpolant_ 

GETINTERPOLANT returns an instance of Matlab's scatteredInterpolant class,
useful for interpolating between different image grids (voxel positions).

Interpolant = GETINTERPOLANT( Img )
Interpolant = GETINTERPOLANT( Img, method )
Interpolant = GETINTERPOLANT( Img, method, extrapolationMethod )

Default Interpolant property assignments:

    .Method = 'linear' [i.e. the *interpolation* method]

    .ExtrapolationMethod = 'none' 

    .Values = [vectorized voxel values of 1st echo/measurement, i.e.: Img.img(:,:,:,1,1)]

Note that all 3 properties can be reassigned at any point upon return.

For info on the 2 optional arguments, see help scatteredInterpolant

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : protected
- InputNames : Img, method, extrapolationMethod
- OutputNames : Interpolant
- DefiningClass : MaRdI
 
</details>

---


### nii

**Synopsis**: _- Write MaRdI image to NiFtI file_ 

Wraps to NII( ) (which wraps to the NiFtI toolbox)

.....
    Syntax

    nii( Img ) 
.....

WARNING

    nii() function is convenient for quickly writing a file to throw
    into an external viewing application (e.g. ImageJ). 
    The nifti Hdr info (i.e. orientation) is probably all wrong. 

    To save NifTI's properly (takes longer) use Img.write()

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | false |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | true  |

- Access : public
- InputNames : Img
- OutputNames : [N/A] 
- DefiningClass : MaRdI
 
</details>

---


### segmentspinalcanal_s

**Synopsis**: _SEGMENTSPINALCANAL_S_ 

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | true  |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : Params
- OutputNames : mask, weights
- DefiningClass : MaRdI
 
</details>

---


### findimages

**Synopsis**: _FINDIMAGES_ 

list = FINDIMAGES( imageDirectory )

Calls dir() to return list of .dcm OR .IMA files in imageDirectory and its echo_* subdirectories

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | true  |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : imgDir
- OutputNames : list
- DefiningClass : MaRdI
 
</details>

---


### compareimggrids

**Synopsis**: _COMPAREIMGGRIDS_ 

isSame = COMPAREIMGGRIDS( Img1, Img2 )
isSame = COMPAREIMGGRIDS( X1, Y1, Z1, X2, Y2, Z2 )

Returns TRUE if voxel positions of Img1 and Img2 are identical

<details markdown="block">
<summary><b>Details</b></summary>
 

| Attribute          | Value |
|:------------------:|:-----:|
| Static             | true  |
| Abstract           | false |
| Sealed             | false |
| ExplicitConversion | false |
| Hidden             | false |

- Access : public
- InputNames : varargin
- OutputNames : isSame
- DefiningClass : MaRdI
 
</details>

---

### set
— _built-in method derived from class_ **matlab.mixin.SetGet**. 
For more info, refer to the MATLAB documentation.

---

### get
— _built-in method derived from class_ **matlab.mixin.SetGet**. 
For more info, refer to the MATLAB documentation.

---

### setdisp
— _built-in method derived from class_ **matlab.mixin.SetGet**. 
For more info, refer to the MATLAB documentation.

---

### getdisp
— _built-in method derived from class_ **matlab.mixin.SetGet**. 
For more info, refer to the MATLAB documentation.

---

### eq
— _built-in method derived from class_ **handle**. 
For more info, refer to the MATLAB documentation.

---

### ne
— _built-in method derived from class_ **handle**. 
For more info, refer to the MATLAB documentation.

---

### lt
— _built-in method derived from class_ **handle**. 
For more info, refer to the MATLAB documentation.

---

### gt
— _built-in method derived from class_ **handle**. 
For more info, refer to the MATLAB documentation.

---

### le
— _built-in method derived from class_ **handle**. 
For more info, refer to the MATLAB documentation.

---

### ge
— _built-in method derived from class_ **handle**. 
For more info, refer to the MATLAB documentation.

---

### isvalid
— _built-in method derived from class_ **handle**. 
For more info, refer to the MATLAB documentation.

---

### findprop
— _built-in method derived from class_ **handle**. 
For more info, refer to the MATLAB documentation.

---

### notify
— _built-in method derived from class_ **handle**. 
For more info, refer to the MATLAB documentation.

---

### notify
— _built-in method derived from class_ **handle**. 
For more info, refer to the MATLAB documentation.

---

### addlistener
— _built-in method derived from class_ **handle**. 
For more info, refer to the MATLAB documentation.

---

### listener
— _built-in method derived from class_ **handle**. 
For more info, refer to the MATLAB documentation.

---

### addlistener
— _built-in method derived from class_ **handle**. 
For more info, refer to the MATLAB documentation.

---

### listener
— _built-in method derived from class_ **handle**. 
For more info, refer to the MATLAB documentation.

---

### addlistener
— _built-in method derived from class_ **handle**. 
For more info, refer to the MATLAB documentation.

---

### listener
— _built-in method derived from class_ **handle**. 
For more info, refer to the MATLAB documentation.

---

### addlistener
— _built-in method derived from class_ **handle**. 
For more info, refer to the MATLAB documentation.

---

### listener
— _built-in method derived from class_ **handle**. 
For more info, refer to the MATLAB documentation.

---

### addlistener
— _built-in method derived from class_ **handle**. 
For more info, refer to the MATLAB documentation.

---

### listener
— _built-in method derived from class_ **handle**. 
For more info, refer to the MATLAB documentation.

---

### findobj
— _built-in method derived from class_ **handle**. 
For more info, refer to the MATLAB documentation.
