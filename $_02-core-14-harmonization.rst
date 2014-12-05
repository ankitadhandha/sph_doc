
.. _$_02-core-14-harmonization:

=========================
Information Harmonization
=========================

This section addresses:

.. rst:role:: USDA #4

   Allow incorporation ARS ontology for ingredients nomenclature with access to external databases.

.. rst:role:: USDA #8

   Provide links to other nutrition-related databases.

Ontomatica harmonizes information from many :ref:`authorities <terms-Authority>`. Our methods create relationships between :ref:`terms <terms-Term>` |_| by using one or more of the following :ref:`predicates <terms-Predicate>`:

:class:`schema:sameAs` :class:`skos:exactMatch` :class:`skos:closeMatch` :class:`skos:relatedMatch`

.. csv-table::
   :header: "Domain", "Harmonized Terms from Authorities", "Example"
   :widths: 15, 35, 10

   "Bio-chemistry", "USDA ARS chemicals", ""
   "", "UN FAO INFOODS chemicals", ""
   "", "US NIH PubChem chemicals", ""
   "", "ChEBI chemicals", ""
   "", "USDA NALT chemicals", ""
   "", "USDA ARS GrainGenes (for wheat ontology)", ""
   "", "UN FAO AgroVoc chemicals", ""
   "", "Protein Data Bank (PDB) chemicals", ""
   "", "Bio-chemical references in US Code of Federal Regulation", ""
   "", "US NIH NCI Applied Research chemicals", ""
   "", "US NIH NCI thesaurus chemicals", ""
   "", "ChEMBL bioactive compounds", ""
   "", "UniProt bioactive compounds", ""
   "", "PDB bioactive compounds", ""
   "", "US NIH NCBI Structure bioactive compounds", ""
   "", "US NIH NCBI Taxon for bacteria and virus", ""
   "", "US FDA Unique Ingredient Identifiers (UNII)", ""
   "", "Enzyme Commission (EC) identifiers", ""
   "", "DBpedia terms", ""
   "", "Chemical Abstract Society (CAS) identifiers", ""
   "Agricultural commodities", "IR-4 commodities", ""
   "", "UN FAO AgroVoc commodities", ""
   "", "UN FAO CODEX crop groups", ""
   "", "UN FAO CODEX livestock groups", ""
   "", "UN FAO fish commodities", ""
   "", "USDA NALT commodities", ""
   "", "US EPA Food Commodity Intake Data (FCID)", ""
   "", "Agriculture commodity references in US Code of Federal Regulation", ""
   "", "DBpedia terms", ""
   "Food and meals", "USDA ARS Food Patterns Equivalents Data (FPED) identities", ""
   "", "US NIH NCI Applied Research identities", ""
   "", "Food identities in US Code of Federal Regulation", ""
   "", "UN FAO food groups", ""
   "Analytical methods", "UN INFOODS tags for CODEX methods", ""
   "", "AOAC international methods", ""
   "", "Methods associated with specific analytical devices and equipment", ""

Example: Fish
-------------

.. csv-table::
   :header: "Aquatic term", "UN FAO term code", "EUNIS term code", "DBpedia term", "AgroVoc term code", "NALT term code"
   :widths: 15, 10, 10, 10, 10, 10

   "Common octopus", "cl_species:OCC", "eunis:60605", "dbpedia:Common_Octopus", "agrovoc:c_5307", "nalt:55627"
   "Angler", "cl_species:MON", "eunis:124874", "dbpedia:Lophius_piscatorius", "agrovoc:c_46042", "nalt:201339"
   "Red mullet", "cl_species:MUT", "eunis:124879", "dbpedia:Mullus_barbatus", "agrovoc:c_43349", "nalt:43361"
   "Great Atlantic scallop", "cl_species:SCE", "eunis:60712", "dbpedia:Pecten_maximus", "agrovoc:c_31159", "nalt:57135"
   "Red swamp crawfish", "cl_species:RCW", "eunis:258990", "dbpedia:Procambarus_clarkii", "agrovoc:c_46824", "nalt:50664"
   "Swordfish", "cl_species:SWO", "eunis:124899", "dbpedia:Swordfish", "agrovoc:c_7559", "nalt:65299"
   "Crested flounder", "cl_species:LFG", "", "dbpedia:Crested_flounder", "agrovoc:c_45572", "nalt:40297"
   "Giant grouper", "cl_species:EEN", "", "dbpedia:Giant_grouper", "agrovoc:c_42341", "nalt:40299"
   "Largemouth black bass", "cl_species:MPS", "eunis:10072", "dbpedia:Largemouth_bass", "agrovoc:c_37035", "nalt:52789"
   "Pacific herring", "cl_species:HEP", "eunis:124939", "dbpedia:Pacific_herring", "agrovoc:c_39009", "nalt:40303"
   "Pandalid shrimps", "cl_species:PDZ", "", "dbpedia:Pandalidae", "agrovoc:c_46467", "nalt:31889"
   "Penaeid shrimps", "cl_species:PEZ", "", "dbpedia:Penaeidae", "agrovoc:c_46269", "nalt:31890"

.. |_| unicode:: 0x80

