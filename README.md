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

### Hiflow

* Param
    * OutputPathAndPrefix *prefix of the output paths (folder has to be exists)*
    * Mesh
        * Filename
        * BCdataFilename
        * InitialRefLevel
    * LinearAlgebra
        * Platform *values: ..*
        * Implementation *values: ..*
        * MatrixFormat *values: DENSE, CSR, COO, ELL*
    * ElasticityModel
        * density
        * lambda
        * mu
        * gravity
    * QuadratureOrder2/QuadratureOrder
    * FiniteElements
        * DisplacementDegree
    * Instationary
        * SolveInstationary
        * DampingFactor
        * RayleighAlpha
        * RayleighBeta
        * Method *values: ImplicitEuler, CrankNicolson, ExplicitEuler, Newmark*
        * DeltaT
        * MaxTimeStepIts
    * Boundary
        * DirichletMaterial
        * DirichletMaterial
        * DirichletMaterial
        * NeumannMaterial1
        * NeumannMaterial1Pressure
        * NeumannMaterial2
        * NeumannMaterial2Pressure
    * LinearSolver
        * SolverName *values: CG (+ SGAUSS_SEIDEL etc) or GMRES (+ ILU2)*
        * MaximumIterations
        * AbsoluteTolerance
        * RelativeTolerance
        * DivergenceLimit
        * BasisSize
        * Preconditioning
        * PreconditionerName *values: SGAUSS_SEIDEL, NOPRECOND = 0, JACOBI = 1, GAUSS_SEIDEL = 2, SGAUSS_SEIDEL = 3, SOR, SSOR, ILU, ILU2, ILU_P, ILUpp*
        * Omega
        * ILU_p
    * ILUPP
        * PreprocessingType
        * PreconditionerNumber
        * MaxMultilevels
        * MemFactor
        * PivotThreshold
        * MinPivot
    * Backup
        * Restore
        * LastTimeStep
        * Filename
