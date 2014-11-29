elasticity
==========

    Author: Nicolai Schoch
    Maintainer: Alexander Weigl <Alexander.Weigl@student.kit.edu
    Date: 2014-11-28
    License: elasticity is closed source
             Documentation under GPL v3

Soft tissue simulation based on Hiflow³

[cite paper please]


## Installation

Download the latest *elasticity* binary for your system:

* [Linux 64bit](https://raw.githubusercontent.com/CognitionGuidedSurgery/elasticity/master/bin/elasticity.lx64)
* Linux 32bit (not supported)
* Windows (not supported)

You should consider [hf3lint](https://github.com/areku/hf3lint)
for checking the input files for elasticity.

## Input Files

Two input files, one with constraints (hf3) one with constraints.
Each input files is in XML. 



### Hiflow


* `Param`
    * `OutputPathAndPrefix`
       prefix of the output paths (folder has to be exists)
    * <Mesh>
        * `Filename` path
        
          path to the mesh file

        * `BCdataFilename` path
        
          path to the contraint file
          
        * `InitialRefLevel` unsigned integer
        
          ** no doc **
        
    * `LinearAlgebra`
        * `Platform` enumeration
        
           *values: ..*
           
        * `Implementation` enumeration
          
           *values: ..*
           
        * `MatrixFormat` enumeration 
          
          * *DENSE
            
            **no doc**
          
          * CS 
           
            **no doc**
          
          * COO 
          
            **no doc**
          
          * ELL
            
            **no doc**
          
    * `ElasticityModel`
        * `density` float
        
          density value of the material in kg / mm³
          
        * `lambda` float
        
          **no doc**
          
        * `mu` float
        
          **no doc**
          
        * `gravity` float
        
          Gravity is applied reverse to the z axis. 
          A given gravity is transformed into the vector: `gravity * [0, 0, -1]`.
          
          **no doc**
    * `QuadratureOrder`
       
       **no doc**
       
    * `FiniteElements`
        * `DisplacementDegree`
        
           **no doc**
           
    * `Instationary`
        * `SolveInstationary` boolean
        
           **no doc**
           
        * `DampingFactor`float
        
          **no doc**
          
        * `RayleighAlpha`float
        
          **no doc**
        
        * `RayleighBeta`float
        
          **no doc**
        
        * `Method` enumeration
        
          **no doc**
          
          * ImplicitEuler
          * CrankNicolson 
          * ExplicitEuler
          * Newmark
        
        * `DeltaT` unsigned integer
        
          **no doc**
        
        * `MaxTimeStepIts` unsigned integer
        
        
          **no doc**
        
    * `Boundary`
        * `DirichletMaterial`
        
          **no doc**
        
        * `DirichletMaterial`
        
          **no doc**
        
        * `NeumannMaterial1`
        
          **no doc**
        
        * `NeumannMaterial1Pressure`
        
          **no doc**
        
        * `NeumannMaterial2`
        
          **no doc**
        
        * `NeumannMaterial2Pressure`
        
          **no doc**
        
    * `LinearSolver`
        * `SolverName` enumeration 
           
           determines the linear solver to use. Specfiy one these:
        
          * *CG*
            
            SGAUSS_SEIDEL
            
          * *GMRES*
          
            +ILU2 
          
          
        * `MaximumIterations`
        
          **no doc**
        
        * `AbsoluteTolerance`
        
          **no doc**
        
        * `RelativeTolerance`
        
          **no doc**
        
        * `DivergenceLimit`
        
          **no doc**
        
        * `BasisSize` 
        
          **no doc**
        
        * `Preconditioning` boolean
        
          **no doc**
        
        * `PreconditionerName` enumeration 
        
          specifies the preconditioner.
          
          One of these values can be given:

          **no doc**          
          
          * SGAUSS_SEIDEL
          * NOPRECOND
          * JACOBI
          * GAUSS_SEIDEL
          * SGAUSS_SEIDEL
          * SOR
          * SSOR
          * ILU
          * ILU2
          * ILU_P
          * ILUpp
    
        * `Omega`
        
          **no doc**
        
        * `ILU_p`
        
          **no doc**
        
    * `ILUPP`
        * `PreprocessingType`
        
          **no doc**
        
        * `PreconditionerNumber`
        
          **no doc**
        
        * `MaxMultilevels`
        
          **no doc**
        
        * `MemFactor`
        
          **no doc**
        
        * `PivotThreshold`
        
          **no doc**
        
        * `MinPivot`
        
          **no doc**
        
    * `Backup`
        * `Restore`
        
          **no doc**
        
        * `LastTimeStep`
        
          **no doc**
        
        * `Filename`
        
          **no doc**
        
