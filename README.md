# Sex difference in autism spectrum disorder (ASD)
Jupyter Notebook for conducting comorbidity analysis for ASD patients on Aetna claims database and replication in Boston Children Hospital (BCH) database. 

## Prerequisites
The following libraries must be installed: 
```bash
library( "knitr" )
library( "dplyr" )
library( "tidyr" )
library( "devtools" )
library( "SqlServerJtds" )
library( "SqlTools" )
library( "FactToCube" )
library( "UpSetR" )
```
## Authorizations
- To have access to the Aetna database, approval is required. 
- To have access to the BCH data, IRB approval is required.

## How to
The jupyter notebook 1.DataSelection comprises all the code used for the selection of data from patients in Aetna claims database. It comprises the SQL code queries. 

The jupyter notebook 2.ComorbidityAnalysis comprises the code to perform the comorbidity analysis in Aetna claims database, specifically, in one of the cases studied, ASD females vs ASD males. SQL code to retrieve the patient counts for the different PheCodes and the subsequent R code for statistical analysis. 

The jupyter notebook 3.CompareThreeGroupsResults comprises the R code to compare the results from the different groups under study and the automatic detection of the phenotypes statistically significant for ASD females. This can be applied to both, Aetna and BCH previous results. 

The jupyter notebook 4.resultsByAgeGroup VisualRepresentation comprises the R code to visualize in an UpSetR graphic the comparison of the statistically significant results in the different age groups under study. This can be applied to both, Aetna and BCH previous results. 

The jupyter notebook BCHreplicationCode comprises the R coded used to validate the results in BCH database. 

## Publication
This code supports the analysis presented in: "Sex differences in Autism Spectrum Disorder, a Comorbidity Pattern Analysis in National Scale Data" (publication to come).

## License
Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
