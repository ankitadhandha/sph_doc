
.. _$_02-core-08-relationships:

=======================
Generic Verbs and Nouns
=======================

This section addresses:

.. rst:role:: USDA #12

   Support capture/documentation of metadata for food composition and non-composition data.

.. note::

   The following terms are members of a :ref:`class <terms-class>` of ontology-independent-terms. These terms map to **specific terms** in ontologies. The summary below identifies:
   
   - :class:`verb` (a.k.a. predicate, relationship, object property)
   
   - noun (a.k.a. thing, object) specified as **X** and **Y**. A more precise term is specified as **{noun}**. A precise noun, as specified by an :ref:`authority <terms-Authority>`, is identified on |N|_. Many examples are listed in |G|_.

`isA <http://en.wikipedia.org/wiki/Is-a>`_ Relationships
--------------------------------------------------------

.. list-table::
   :widths: 30 30
   :header-rows: 1

   * - Relationship
     - Inverse
   * - X :class:`includesSpecific` Y
          
          |_|
          
     - Y :class:`isA` X
          
          |_|
          
   * - 
     - Taxon :class:`isA` Taxon
          
          |_|
          
   * - 
     - Food product :class:`isA` Food product
          
          |_|
          
   * - 
     - Food product :class:`isOneOf` {Food product list}
          
          |_|
          
   * - X :class:`inheritsTo` Y
          
          |_|
          
     - Y :class:`inheritsFrom` X
          
          |_|
          

WordNet whole-part Relationships (`Holonymy/meronymy <http://en.wikipedia.org/wiki/Holonymy>`_)
-----------------------------------------------------------------------------------------------

.. list-table::
   :header-rows: 1

   * - Relationship
     - Inverse
   * - X :class:`containsSubstance` Y
          
          |_|
          
     - Y :class:`substanceContainedIn` X
          
          |_|
          
   * - FoodProduct :class:`containsSubstance`
          
          {Substance, amount in total,
          
          amount in solids,
          
          label claim (yes/no) }
     - 
   * - X :class:`hasIngredient` Y
          
          |_|
          
     - Y :class:`ingredientOf` X
          
          |_|
          
   * - FoodProduct :class:`hasIngredient`
          
          {Food product, rank,
          
          total ingredient in total product,
          
          ingredient solids in product solids
          
          {purpose list} }
     - 
   * - FoodProduct :class:`mayHaveIngredient`
          
          {Food product, rank,
          
          total ingredient in total product,
          
          ingredient solids in product solids
          
          {purpose list} }
     - 
   * - X :class:`madeFrom` Y
          
          |_|
          
     - Y :class:`usedToMake` X
          
          |_|
          
   * - Container :class:`usesStructuralStrengthMaterial`
          
          Substance
          
          |_|
          
     - 
   * - Container :class:`usesCoatingMaterial`
          
          Substance
          
          |_|
          
     - 
   * - FoodProduct :class:`isMadeFrom`
          
          FoodProduct
          
          |_|
     - 
   * - FoodProduct :class:`isDerivedFrom`
          
          {Food source, environment,
          
          agricultural treatment,
          
          growth stage}
     - 
   * - FoodProduct :class:`isPartOf`
          
          {Anatomical part, growth stage,
          
          cut, grade}
     - 
   * - FoodProduct :class:`isExtractedSubstance`
          
          {Extracted substance,
          
          extracting substance,
          
          process, temperature,
          
          duration, sequence_ID.}
     - 
   * - FoodProduct :class:`hadRemovedSubstance`
          
          {Extracted substance, etc.}
          
          |_|
     - 
   * - X :class:`yieldsPortion` Y
          
          |_|
          
     - Y :class:`portionOf` X
          
          |_|
          
   * - X :class:`spatiallyIncludes` Y
          
          |_|
          
     - Y :class:`spatiallyIncludedIn` X
          
          |_|
          
   * - X :class:`hasComponent` Y
          
          |_|
          
     - Y :class:`componentOf` X
          
          |_|
          
   * - FoodProduct :class:`containsDish`
          
          FoodProduct
          
          |_|
          
     - 

Additional Relationships
------------------------

.. list-table::
   :header-rows: 1

   * - Relationship
     - Inverse
   * - X :class:`causes` Y
          
          |_|
          
     - Y :class:`causedBy` X
          
          |_|
          
   * - X :class:`instrumentFor` Y
          
          |_|
          
     - Y :class:`performedByInstrument` X
          
          |_|
          
   * - X :class:`processFor` Y
          
          |_|
          
     - Y :class:`usesProcess` X
          
          |_|
          
   * - X :class:`appliedTo` Y
          
          |_|
          
     - Y :class:`underwentProcess` X
          
          |_|
          
   * - FoodProduct :class:`underwentProcess`
          
          {Process, equipment, temperature,
          
          duration, place/stage, sequence_ID,
          
          {purpose list} }
     - 
   * - FoodProduct :class:`isForSpecialUse`
          
          {Use/diet, {country list} }
          
          |_|
          
     - 
   * - FoodProduct :class:`madeFor`
          
          {Consumer, {country list} }
          
          |_|
          
     - 
   * - FoodProduct :class:`usuallyConsumedFor`
          
          {Meal type, {country list} }
          
          |_|
          
     - 
   * - {Taxon, AnatomicalPart} :class:`usedFor`
          
          {purpose, priority {country list} }
          
          |_|
          
     - 
   * - Substance :class:`usedFor`
          
          {purpose, priority, food product}
          
          |_|
          
     - 
   * - X :class:`beneficialFor` Y
          
          |_|
          
     - Y :class:`benefitsFrom` X
          
          |_|
          
   * - X :class:`treatmentFor` Y
          
          |_|
          
     - Y :class:`treatedWith` X
          
          |_|
          
   * - X :class:`harmfulFor` Y
          
          |_|
          
     - Y :class:`harmedBy` X
          
          |_|
          
   * - Substance :class:`harmfulFor`
          
          {harmful effect, strength,
          
          food product}
     - 
   * - X :class:`growsIn` Y
          
          |_|
          
     - Y :class:`growthEnvironmentFor` X
          
          |_|
          
   * - X :class:`hasPhase` Y
          
          |_|
          
     - Y :class:`phaseOf` X
          
          |_|
          
   * - FoodProduct :class:`hasState`
          
          Physical state
          
          |_|
          
     - 
   * - X :class:`hasForm` Y
          
          |_|
          
     - Y :class:`isFormOf` X
          
          |_|
          
   * - FoodProduct :class:`hasForm`
          
          Physical form
          
          |_|
          
     - 
   * - Container :class:`hasForm`
          
          Physical form
          
          |_|
          
     - 
   * - FoodProduct :class:`packedIn`
          
          Container
          
          |_|
          
     - 
   * - X :class:`hasPrice`
          
          MoneyAmount
          
          |_|
          
     - 
   * - Substance :class:`measuredIn`
          
          Unit of measurement
          
          |_|
          
     - 


.. |N| replace:: Data Integration
.. _N: $_02-core-15-integration.html

.. |G| replace:: Glossary of Terms
.. _G: $_07-glossary.html


.. |_| unicode:: 0x80

