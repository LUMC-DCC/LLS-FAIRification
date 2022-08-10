
The following variables are part of the LLS-data but were not explored during the LLS-FAIRification pilot. OPAL variable names, descriptions and candidate ontologies have not been discussed, agreed upon and/or may have changed. Go to the [Mica-catalogue](https://dw.clinicalresearch.nl/pub/study/lls) of LLS for an up-to-date overview of the LSS-data.

## Other variables

| Element           | OPAL variable name | Preliminary description                   | Candidate ontology                         | Values | Units |
| ----------------- | ------------------ | ----------------------------------------- | ------------------------------------------ | ------ | ----- |
| Visitdate         | visitdate          | The date at which the participant visited | http://purl.obolibrary.org/obo/NCIT_C83031 |        |       |
| time of blooddraw | time_of_blooddraw  | the time the blood was drawn              | http://purl.obolibrary.org/obo/NCIT_C25207 |        |       |
| LabNr_IOP1       | LabNr_IOP1         | ID of biomaterial during IOP1 inclusion   | http://edamontology.org/data_0842           |        |       |
| GWASnr           | GWASnr             | ID of SNP array data                      | http://edamontology.org/data_0842           |        |       |

## Gut microbiome related metabolites

| Element          | OPAL variable name      | Preliminary description                             | Candidate ontology                          | Values | Units |
| ---------------- | ----------------------- | --------------------------------------- | ------------------------------------------- | ------ | ----- |
| LabNr_IOP1       | LabNr_IOP1              | ID of biomaterial during IOP1 inclusion | http://edamontology.org/data_3273           |        |       |
| NMCname          | GMRM18_NMCname          | NMCname/ID                              |                                             |        |       |
| measurement_date | GMRM18_measurement_date | date of measurement                     | http://purl.obolibrary.org/obo/OPMI_0000580 |        |       |
| source           | GMRM18_source           | source material for measurement         | http://purl.org/dc/elements/1.1/source      |        |       |
| BetaineµM        | GMRM18_Betaine          | Betaine (µM)                            | http://purl.obolibrary.org/obo/CHEBI_17750  |        | µM    |
| CarnitineµM      | GMRM18_Carnitine        | Carnitine (µM)                          | http://purl.obolibrary.org/obo/CHEBI_17126  |        | µM    |
| CholineµM        | GMRM18_Choline          | Choline (µM)                            | http://purl.obolibrary.org/obo/CHEBI_15354  |        | µM    |
| DeoxycarnitineµM | GMRM18_Deoxycarnitine   | Deoxycarnitine (µM)                     | http://purl.obolibrary.org/obo/CHEBI_16244  |        | µM    |
| TMAOµM           | GMRM18_TMAO             | TMAO (µM)                               | http://purl.obolibrary.org/obo/CHEBI_15724  |        | µM    |

## Visit measures

| Element          | OPAL variable name | Preliminary description                                                                                                              | Candidate ontology | Values | Units |
| ---------------- | ------------------ | ------------------------------------------------------------------------------------------------------------------------ | --------           | ------ | ----- |
| StudNum          | LLnr               | LLnr (Leiden Longevity number)                                                                                           |                    |        |       |
| ADL01            | ADL01              | 1. Stoelgang (in voorafgaande week)                                                                                      |                    |        |       |
| ADL02            | ADL02              | 2. Blaas (in voorafgaande week)                                                                                          |                    |        |       |
| ADL03            | ADL03              | 3. Voeding                                                                                                               |          |        |       |
| ADL04            | ADL04              | 4. Verzorging (gezicht, haar, tanden, scheren)                                                                           |          |        |       |
| ADL05            | ADL05              | 5. Kleden                                                                                                                |          |        |       |
| ADL06            | ADL06              | 6. Verplaatsen                                                                                                           |          |        |       |
| ADL07            | ADL07              | 7. Gebruik van het toilet                                                                                                |          |        |       |
| ADL08            | ADL08              | 8. Lopen (met betrekking tot de mobiliteit in huis of op de afdeling, binnen)                                            |          |        |       |
| ADL09            | ADL09              | 9. Traplopen                                                                                                             |          |        |       |
| ADL10            | ADL10              | 10. Baden (meestal de moeilijkste handeling)                                                                             |          |        |       |
| IADL01           | IADL01             | 1. Kunt u telefoneren…                                                                                                   |          |        |       |
| IADL02           | IADL02             | 2. Kunt u plaatsen bereiken die buiten loopafstand liggen…                                                               |          |        |       |
| IADL03           | IADL03             | 3. Kunt u uw eigen boodschappen, levensmiddelen of kleding, doen (ervan uitgaande dat de patiënt beschikt over vervoer)… |          |        |       |
| IADL04           | IADL04             | 4. Kunt u voor u zelf koken…                                                                                             |          |        |       |
| IADL05           | IADL05             | 5. Kunt u huishoudelijk werk doen…                                                                                       |          |        |       |
| IADL06           | IADL06             | 6. Kunt u uw eigen medicijnen innemen…                                                                                   |          |        |       |
| IADL07           | IADL07             | 7. Kunt u uw eigen geldzaken regelen…                                                                                    |          |        |       |
| sum_adl_iadl     | sum_adl_iadl       | Som totalen ADL en IADL                                                                                                  |          |        |       |
| MMSE             | MMSE               | Mini Mental State Examination                                                                                            |          |        |       |
| MMSE_Status      | MMSE_Status        | Status over afname MMSE                                                                                                  |          |        |       |
| MMSE_Opmerking   | MMSE_Opmerking     | MMSE opmerking                                                                                                           |          |        |       |
| MMSE_filter      | MMSE_filter        | Status = 1 (FILTER)                                                                                                      |          |        |       |
| Cant01           | Cant01             | Waarop de ladder bevindt u zich persoonlijk op dit moment (in uw leven)?                                                 |          |        |       |
| Cant02           | Cant02             | Status over afname Cantril’s ladder                                                                                      |          |        |       |
| Cant02_Opmerking | Cant02_Opmerking   | Cantril ladder opmerking                                                                                                 |          |        |       |
