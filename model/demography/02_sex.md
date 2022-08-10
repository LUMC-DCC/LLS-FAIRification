### Model sex

```mermaid
%%{init: {'theme':'base'}}%%
graph TD
   
    
    A{Person} -->|rdf:type| B[ncit:person]
    C{Role:<br> Study participant} -->|rdf:type| D[ncit:human study subject]
    F{Quality: Sex}
    G{Process:<br>Sex recording process} -->|ro:has output| H{Output type:<br>Female/male}
    C -->|rdf:type| E[ro:role]
    A -->|ro:has role| C
    A -->|ro:has quality| F
    C -->|ro:realized in| G
    H -->|stato:has value| I((female/male))
    H -->|rdf:type| K[ncit:output]
    G -->|rdf:type| J[iao:process]
    H -->|iao:is about| F
    F -->|rdf:type| L[iao:quality]
    F -->|rdf:type| M[gsso:administrative gender]
    F -->|rdf:type| N[ncit:female/male]
    
    classDef literal fill:#dae8fc;
    classDef ontology fill:#d5e8d4;
    class I literal;
    class K,J,B,D,E,L,M,N ontology;
 ```
 
### Description
1. The model separates two 'things'. On the hand, there is the attribute or quality a person has (e.g., brown hair, female sex, age of 94). On the other hand, there is the process of how this was measured or determined plus the value of the output of that process. Of course, the value of the output of the recording process (e.g., of female sex) should correspond to the actual attribute or quality of the person (e.g., female).
2. In the LLS-case the recording process to determine the sex of a person involved taking the value of a person's sex from the Dutch ['Basisregistratie Personen'](https://www.rvig.nl/brp)(National identity registration). Because this concerns a person's gender or sex as represented in an 'administrative system' and may be changed after birth, we decided this concept is best reflected by the term ['Administrative gender'](http://purl.obolibrary.org/obo/GSSO_009316) from the 'Gender, Sex and Sexual Orientation Ontology'.
3. In the LLS-case the values of the administrative sex of the participants were limited to 'male' and 'female' (so no missings, unknowns, or other values).

### Abbreviations
* ncit = [National Cancer Institute Thesaurus OBO edition](https://ontobee.org/ontology/ncit)
* ro = [Relation Ontology](https://ontobee.org/ontology/RO)
* iao = [Information Artefact Ontology](https://ontobee.org/ontology/IAO)
* stato = [Statistical Methods Ontology](https://ontobee.org/ontology/STATO)
* gsso = [Gender, Sex, and Sexual Orientation Ontology](https://ontobee.org/ontology/GSSO)

### Example RDF (turtle)