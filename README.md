# LLS-FAIRification pilot: Semantic modeling of the Leiden Longevity Study (LLS) data.
![GitHub](https://img.shields.io/github/license/LUMC-DCC/LLS-FAIRification)

## LLS description and OPAL data warehouse
For the Leiden Longevity Study, long-lived siblings of European descent were recruited together with their offspring and the partners of this offspring between 2002 and 2006. Families were recruited if at least two long-lived siblings were alive and fulfilled the age criterion of 89 years or older for males and 91 years or older for females. In total 944 long-lived siblings were included with a mean age of 94 years (range 89-104), 1671 offspring (61 years, 34-81) and 744 partners (60 years, 30-79). The aim of the study was to retrieve genetically determined mechanisms of longevity and their interaction with the environment. For all subjects, blood samples and other biomaterial was taken, and demography information, information on medical history and self-reported / survey information was collected. Data are stored at LUMC data warehouse OPAL and are made human-findable through [data catalogue Mica](https://dw.clinicalresearch.nl/pub/study/lls).

## FAIRification pilot description
In this Github repository we present a complementary effort to semantically model a part of the LSS data, namely the demography data. It is a preliminary effort to make Dutch cohort data interoperable according to the FAIR principles as well. In this pilot:
* We followed a [FAIRification workflow](https://github.com/LUMC-DCC/LLS-FAIRification/wiki/FAIRification-workflow)
* We used [Ontop and GraphDB](https://github.com/LUMC-DCC/LLS-FAIRification/wiki/Tools-used-to-ontologize-data) to create and store ontologized data in RDF-format
* We based our semantic model on the one for common data elements for rare disease registries (see [here](https://doi.org/10.1186/s13326-022-00264-6) and [here](https://github.com/ejp-rd-vp/CDE-semantic-model)), but decided to make use of [OBO foundry ontologies](https://obofoundry.org/) only
* Our presented semantic model is limited to the LSS demography data for now and is an 'alpha version' 



