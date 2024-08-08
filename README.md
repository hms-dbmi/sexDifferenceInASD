# Sex difference in autism spectrum disorder (ASD)
Jupyter Notebook for conducting comorbidity analysis for ASD patients on a claim database and replication in an independent electronic health record database. 

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
library( "rentrez" )
```
## Authorizations
- To have access to the claim database, approval is required. 
- To have access to the electronic health record database, IRB approval is required.

## How to
The jupyter notebook 1.DataSelection comprises all the code used for the selection of data from patients in the claims database. It comprises the SQL code queries. 

The jupyter notebook 2.ComorbidityAnalysis comprises the code to perform the comorbidity analysis in the claims database, specifically, in one of the cases studied, ASD females vs ASD males. SQL code to retrieve the patient counts for the different PheCodes and the subsequent R code for statistical analysis. 

The jupyter notebook 3.CompareThreeGroupsResults comprises the R code to compare the results from the different groups under study and the automatic detection of the phenotypes statistically significant for ASD females. This can be applied to both previous results. 

The jupyter notebook 4.resultsByAgeGroup VisualRepresentation comprises the R code to visualize in an UpSetR graphic the comparison of the statistically significant results in the different age groups under study. This can be applied to both, previous results. 

The jupyter notebook 5.PubMedCheckForPhecode comprises the R and SQL code to map the PheCodes to MESH terms, generate the UMLS queries and the subsequent PubMed queries to extract the number of previous publications in the field. 

The jupyter notebook 6.ReplicationOfTheAnalysisInEHRdataset_dataSelectionAndComorbidityAnalysis comprises the R coded used to validate the results in BCH database. 

## Publication
This code supports the analysis presented in: "Multi-PheWAS intersection approach to identify sex differences across comorbidities in 59 140 pediatric patients with autism spectrum disorder" https://academic.oup.com/jamia/article/29/2/230/6354089 

### Citation: 
Gutiérrez-Sacristán, A., Sáez, C., De Niz, C., Jalali, N., DeSain, T.N., Kumar, R., Zachariasse, J.M., Fox, K.P., Palmer, N., Kohane, I. and Avillach, P., 2022. Multi-PheWAS intersection approach to identify sex differences across comorbidities in 59 140 pediatric patients with autism spectrum disorder. Journal of the American Medical Informatics Association, 29(2), pp.230-238.

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
