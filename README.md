### Introduction

A causal relationship is defined by a correlation between two events or elements where one influences the other. In Molecular Biology, causality underlies the principles of interactions between biological components, for instance in governing regulatory mechanisms. Consequently, the understanding of these interactions and the mechanisms that they enable, involved in biological regulations (e.g., gene regulation) is to be improved by looking at the core interactions happening among entities. Once causality is established, the next challenge is to adequately represent and archive it so that it can be shared and used by computers and humans alike.
This repository is intended for:
* providing a state of the art of existing resources and formal representations depicting causal relationships among biological components
* developing and documenting mappings between resources/languages capturing causal reasoning information in Molecular and Cellular biology.


**Existing Resources depicting causal relationships:**
  * [The Gene Ontology](http://geneontology.org) - [schema_docs](doc/GO)
  * [GRECO](http://www.thegreco.org)  - [schema_docs](doc/GRECO)
  * [Signor](http://signor.uniroma2.it/)  - [schema_docs](doc/Signor)
  * [SignaLink](http://signalink.org/)  - [schema_docs](doc/SignaLink)
  * [InTact](http://www.ebi.ac.uk/intact/)  - [schema_docs](doc/InTact)
  * [Causal Biological Network](http://causalbionet.com/) - [schema_docs](doc/CBN)
  * [Reactome](http://www.reactome.org/) - [schema_docs](doc/Reactome)
 
**Languages:**
  * [OpenBel](http://wiki.openbel.org/display/BLD/Statement+Examples+-+Causal)
    * Open data in OpenBel: 
    * [RDF conversion available](http://wiki.openbel.org/display/BEL2RDF/BEL+to+RDF+Home)
    * 
  * [BioPax](http://www.biopax.org/)
  * [SBMLqual](http://sbml.org/Documents/Specifications/SBML_Level_3/Packages/qual)
  * [CausalTAB](http://signor.uniroma2.it/scripts/causalTabInfo.php)
    
**Tools:**
  * [CausalR](https://www.bioconductor.org/packages/release/bioc/html/CausalR.html)  - [schema]()
     * Open data in CausalR:

Each of these resources captures, or is begining to capture causal information.  There are many commonalities between the causal information being captured: multiple resources record whether causal relations are -ve vs +ve, direct or indirect & record mechanism.
 This site aims to document and align the vocabularies and semantics used by each of these resources.
 
### Strategy for sharing data:
 
We recognise that each resource already has a representation that is doing useful work, so we seek to map existing schemas rather than propose changes.  To do this we will:  
 
 * Map all entities to standard ontology classes/relations.
 * Map statements to a language with defined semantics: RDF triples?  OWL? ...
 
 
 
### Differences between resources:

* **IntAct, Signor, CausalR**: causal & regulatory *relations apply between gene products*.  Signor records the processes involved separately as 'mechanism', maintaining the association between regulation and process within each statement.
* **GO**: causal & regulatory *relations apply between the processes* that gene products are capable of.  This has some advantages.  A gene product may have multiple functions - only one of which is a mechanism for regulating the activity of a second gene product.

One obvious way to bridge this gap is for RO can define shortcut relations mapping to the GP:GP relations in other resources, something like this:

* name: has\_activity\_that\_positively\_regulates\_activity\_of
* xref: signor:activates
* xref: causalR:activates
* Property chain: capable_of o positively_regulates o enables -> has\_activity\_that\_regulates\_activity\_of

Where mechanism is recorded, we could potentially use a simpler relation:

GP1 activate GP2 mechanism:phosphorylation 
=>
GP1 capable\_of some (phosphorylation that regulates\_activity\_of GP2)

### Proposed structure for mapping files:

#### Relations table (signor example is fictional - for illustration purposes only)

| resource name | relation name | relation ID | domain | range | description | example usage |
|---------------|---------------|-------------|--------|-------|-------------|---------------|
| RO | regulates | RO_ | process | process | | |
| signor | activates | - | protein | protein | | |
 
#### Class table

| resource name | class name | class ID | domain | range | description | example usage |
|---------------|---------------|-------------|--------|-------|-------------|---------------|
| PRO | protein | PRO_ | process | process | | |

#### Mapping table

| resource name | relation name | relation ID | ontology relation name | ontology relation ID |
|---------------|---------------|-------------|------------------------|----------------------|
|  |  |  |  |  |

### Repository structure:

~~~~~~~~~.sh  
  doc/
    README.md
     GO/
        README.md
     GRECO/
        README.md
     Signor/
        README.md
     SignaLink/
       README.md
     IntAct/
       README.md
     CBN/
       README.md
     Reactome/
       README.md
~~~~~~~~~~~~
  
