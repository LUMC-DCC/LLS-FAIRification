# LLS-FAIRification pilot: Semantic modeling of the Leiden Longevity Study (LLS) data.
![GitHub](https://img.shields.io/github/license/LUMC-DCC/LLS-FAIRification)

## LLS description and OPAL data warehouse
For the [Leiden Longevity Study](https://leidenlangleven.nl/), long-lived siblings of European descent were recruited together with their offspring and the partners of this offspring between 2002 and 2006. Families were recruited if at least two long-lived siblings were alive and fulfilled the age criterion of 89 years or older for males and 91 years or older for females. In total 944 long-lived siblings were included with a mean age of 94 years (range 89-104), 1671 offspring (61 years, 34-81) and 744 partners (60 years, 30-79). The initial aim of the study was to retrieve genetically determined mechanisms of longevity and their interaction with the environment. For all subjects, blood samples and other biomaterial was taken, and demography information, information on medical history and self-reported / survey information was collected. Data are stored at LUMC data warehouse OPAL and are made human-findable through [data catalogue Mica](https://dw.clinicalresearch.nl/pub/study/lls).

## FAIRification pilot description
In this Github repository we present a complementary effort to semantically model a part of the LSS data, namely the demography data. It is a preliminary pilot effort to make Dutch cohort data interoperable according to the FAIR principles. Please go to the links below for more information on:
* [The ontologies and definitions used](https://github.com/LUMC-DCC/LLS-FAIRification/blob/main/terms-and-definitions/demography-terms-and-definitions.md)
* The model modules for [Pseudonyms](https://github.com/LUMC-DCC/LLS-FAIRification/blob/main/model/demography/01_pseudonym.md), [Sex](https://github.com/LUMC-DCC/LLS-FAIRification/blob/main/model/demography/02_sex.md), [Age](https://github.com/LUMC-DCC/LLS-FAIRification/blob/main/model/demography/03_age.md) and [Vital status](https://github.com/LUMC-DCC/LLS-FAIRification/blob/main/model/demography/04_vital-status.md)
* The FAIRification process, experiences and tools used in the [wiki](https://github.com/LUMC-DCC/LLS-FAIRification/wiki). In this pilot:
  * We followed a [FAIRification workflow](https://github.com/LUMC-DCC/LLS-FAIRification/wiki/FAIRification-workflow)
  * We used [Ontop and GraphDB](https://github.com/LUMC-DCC/LLS-FAIRification/wiki/Tools-used-to-ontologize-data) to create and store ontologized data in RDF-format
  * We based our semantic model on the one for common data elements for rare disease registries (see [here](https://doi.org/10.1186/s13326-022-00264-6) and [here](https://github.com/ejp-rd-vp/CDE-semantic-model)), but decided to make use of [OBO foundry ontologies](https://obofoundry.org/) only. This was prompted by the work on the [COVID-19 Epidemiology and Monitoring Ontology (CEMO)](https://github.com/NuriaQueralt/covid19-epidemiology-ontology)
  * Our presented semantic model is limited to the LSS demography data for now and is an 'alpha version' 

## LLS FAIR Data Point (FDP) catalog
A first test was done with creating an [LLS catalog](https://fdp.lumc.nl/catalog/3d06ba8c-f2d6-4e56-9ddc-7f40dcee3e72) according to the [pre-loaded metadata structure of the FDP reference implementation](https://specs.fairdatapoint.org/#navigationinformation) (LUMC FDP > LLS catalog > two LLS datasets). A next step would be to explore how human-findable metadata from OPAL/Mica can be converted to machine-actionable metadata in the LLS FDP catalog.


