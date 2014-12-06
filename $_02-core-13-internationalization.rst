
.. _$_02-core-13-internationalization:

==============================
International Data and Methods
==============================

This section addresses:

.. rst:role:: Ontomatica defined objective

Ontomatica proposes, as part of LABEL PROJECT, to implement COMPLETE SYSTEM for two national authorities - USA and GBR (UK).

Internationalization is enabled by USDA PRIME.

Ontomatica will identify countries.

Then, for a specific country and for a specific food, Ontomatica will illustrate the distribution of energy (kilocal, kilojoule) as defined by the national authority.

For example:

.. csv-table::
   :header: "Country", "ISO 3", "UN FAO", "DBpedia"
   :widths: 15, 10, 10, 20

   "United Kingdom", "GBR", "826", "dbpedia:United_Kingdom"
   "United States", "USA", "840", "dbpedia:United_States"

Energy illustration is generated using UN FAO INFOODS and authority values.

Note below: USDA and GBR use different analytical methods when reporting values.

Methods

::

   EC carbohydrates	CHOPL = (SUGAR [ncit:C38046]) + (SUGOH [ncit:C38046])

   GBR carbohydrates	CHOAVLM = (MNSAC [ncit:C38046]) + (DISAC [ncit:C38046]) + (DEXTN [ncit:C38046]) + (STARCHM [ncit:C38046]) + (GLYCM [ncit:C38046])

   USA carbohydrates (food: whole wheat)	CHOCDF = 100 g - ((NT [vocal:Kjeldahl] x [infoods:XPROT] 5.83 [xsd:float]) + (WATER [ncit:C38046]) + (FAT [ncit:C38046]) + (ASH [ncit:C38046])g)

   GBR fiber	FIBTS = (GLUCNB [ncit:C38046]) + (CELLU [ncit:C38046]) + (HEMCEL [ncit:C38046]) + (INULN [ncit:C38046]) + (LIGN [ncit:C38046]) + (PECT [ncit:C38046])

   USA fiber	FIBTG [aoac:978.10] = (FIBSOL [ncit:C38046]) + (FIBINS [ncit:C38046]) + (NSP [ncit:C38046])

Legend

- ALL CAPS = INFOODS_identifier.
- Method format = [method-ontology-prefix : ontology-identifier].
- ncit = NIH NCI thesaurus.
- ncit:C38046 = Unspecified.
- XPROT = protein conversion factor.
- XPROT value = 5.83 for the food: whole wheat.
- XPROT is a floating point number [xsd:float].

