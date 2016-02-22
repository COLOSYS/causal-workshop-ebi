This repository is intended for developing and documenting mappings
between resources/langauages capturing causal reasoning information in molecular
and cellular biology.

Resources:
  * [The Gene Ontology](http://geneontology.org) - [schema_docs](doc/GO)
  * [GRECO](http://www.thegreco.org)  - [schema_docs](doc/GRECO)
  * [Signor](http://signor.uniroma2.it/)  - [schema_docs](doc/Signor)
  * [SignaLink](http://signalink.org/)  - [schema_docs](doc/SignaLink)
  * [InTact](http://www.ebi.ac.uk/intact/)  - [schema_docs](doc/InTact)
 
Languages:
  * [OpenBel](http://wiki.openbel.org/display/BLD/Statement+Examples+-+Causal)
    * Open data in OpenBel: 
    * [RDF conversion available](http://wiki.openbel.org/display/BEL2RDF/BEL+to+RDF+Home)
    
Tools:
  * [CausalR]()  - [schema]()
     * Open data in CausalR:

Each of these resources captures, or is begining to capture causal information.  There are many commonalities between the causal information being captured: multiple resources record whether causal relations are -ve vs +ve, direct or indirect & record mechanism.
 This site aims to document and align the vocabularies and semantics used by each of these resources.
 
Differences between resources:

**GO**: causal & regulatory *relations apply between the processes* that gene products are capable of.
**IntAct, Signor, CausalR**: causal & regulatory *relations apply between gene products*.  Signor records the processes involved separately as 'mechanism'
  
 Repository structure:

~~~~~~~~~.sh  
  doc/
    README.md
     GO/
          README.md
     GRECO/
         README.md
     Signor/
         README.md
	 Signor - example data
     SignaLink/
         README.md
     IntAct/
         README.md
~~~~~~~~~~~~
  
