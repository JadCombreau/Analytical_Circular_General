# ANANAX ANALYTICAL CIRCULAR
## Markdown documentation file
## Ananax2d_Analytical_Circular Workflow over Isight

| | CANONICAL | ANALYTICAL |
|-----------|:-----------:|:-----------:|
|INTAKE | -- | X |
|BYPASS | -- | X |

### Workflow type & role

This Workflow (__Analytical Circular__) has the final goal, like others Workflows, the acoustic attenuation matrix calculus.
This Workflow is for canonical geometries, that is to say we do not have to generate any mesh. 

In numerical cases, ACTRAN automatically generates mesh supposed to be uniformed. In analytical cases, we do not have to create any mesh. Sounds simple right ?


The air inlet or the bypass duct is therefore assumed to be more or less uniform. We do not calculate any flow either.
For the acoustic computation, we no longer use the ACTRAN solver, as was the cas in numerical workflows but a new solver nammed MADIWHAX. 

__This Workflow therefore presents four boxes :__

![Analytical Circular Workflow](https://user-images.githubusercontent.com/45098441/86543241-107ff700-bf1d-11ea-8b44-2653949889d9.JPG)
----------------------------


- __Initialization :__ *allows among other things the creation of initialization variables, environment variables or even structure test and the input XML file reading.*
- __Acoustic Models :__ *input file, thermodynamic file conditions (etc.)*
- __Acoustic Computations :__ *MADIWHAX solver for the noise acoustic calculation in the air intake/bypass (to obtain frequencies)*
- __Postprocessing :__ *allows the generation of the attenuation matrix (PIFF & PID calculus)*
