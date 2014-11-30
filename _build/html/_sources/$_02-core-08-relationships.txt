
.. _$_02-core-08-relationships:

=====================
Generic Relationships
=====================

Introduction

.. rst:role:: USDA #12

   Support capture/documentation of metadata for food composition and non-composition data.

.. note::

   These are not ``ontology terms``. These are generic expressions that map to **specific terms** in :class:`ontologies`.

`isA <http://en.wikipedia.org/wiki/Is-a>`_ Relationships
--------------------------------------------------------

.. list-table::
   :widths: 30 30
   :header-rows: 1

   * - Relationship
     - Inverse
   * - X :class:`includesSpecific` Y
     - Y :class:`isA` X
   * - 
     - Taxon :class:`isA` Taxon
   * - 
     - Food product :class:`isA` Food product
   * - 
     - Food product :class:`isOneOf` {Food product list}
   * - X :class:`inheritsTo` Y
     - Y :class:`inheritsFrom` X

WordNet whole-part Relationships (`Holonymy/meronymy <http://en.wikipedia.org/wiki/Holonymy>`_)
-----------------------------------------------------------------------------------------------

.. list-table::
   :widths: 30 30
   :header-rows: 1

   * - Relationship
     - Inverse
   * - X :class:`containsSubstance` Y
     - Y :class:`substanceContainedIn` X
   * - FoodProduct :class:`containsSubstance` {Substance, amount in total, amount in solids, label claim (yes/no)}
     - 
   * - X :class:`hasIngredient` Y
     - Y :class:`ingredientOf` X
   * - FoodProduct :class:`hasIngredient` {Food product, rank, total ingredient in total product, ingredient solids in product solids {purpose list}}
     - 
   * - FoodProduct :class:`mayHaveIngredient` {Food product, rank, total ingredient in total product, ingredient solids in product solids {purpose list}}
     - 
   * - X :class:`madeFrom` Y
     - Y :class:`usedToMake` X
   * - Container :class:`usesStructuralStrengthMaterial` Substance
     - 
   * - Container :class:`usesCoatingMaterial` Substance
     - 
   * - FoodProduct :class:`isMadeFrom` FoodProduct
     - 
   * - FoodProduct :class:`isDerivedFrom` {Food source, environment, agricultural treatment, growth stage}
     - 
   * - FoodProduct :class:`isPartOf` {Anatomical part, growth stage, cut, grade}
     - 
   * - FoodProduct :class:`isExtractedSubstance` {Extracted substance, extracting substance, process, temperature, duration, sequence_ID.}
     - 
   * - FoodProduct :class:`hadRemovedSubstance` {Extracted substance, etc.}
     - 
   * - X :class:`yieldsPortion` Y
     - Y :class:`portionOf` X
   * - X :class:`spatiallyIncludes` Y
     - Y :class:`spatiallyIncludedIn` X
   * - X :class:`hasComponent` Y
     - Y :class:`componentOf` X
   * - FoodProduct :class:`containsDish` FoodProduct
     - 

Additional Relationships
------------------------

.. list-table::
   :widths: 30 30
   :header-rows: 1

   * - Relationship
     - Inverse
   * - X :class:`causes` Y
     - Y :class:`causedBy` X
   * - X :class:`instrumentFor` Y
     - Y :class:`performedByInstrument` X
   * - X :class:`processFor` Y
     - Y :class:`usesProcess` X
   * - X :class:`appliedTo` Y
     - Y :class:`underwentProcess` X
   * - FoodProduct :class:`underwentProcess` {Process, equipment, temperature, duration, place/stage, sequence_ID, {purpose list}}
     - 
   * - FoodProduct :class:`isForSpecialUse` {Use/diet, {country list}}
     - 
   * - FoodProduct :class:`madeFor` {Consumer, {country list}}
     - 
   * - FoodProduct :class:`usuallyConsumedFor` {Meal type, {country list}}
     - 
   * - {Taxon, AnatomicalPart} :class:`usedFor` {purpose, priority {country list}}
     - 
   * - Substance :class:`usedFor` {purpose, priority, food product}
     - 
   * - X :class:`beneficialFor` Y
     - Y :class:`benefitsFrom` X
   * - X :class:`treatmentFor` Y
     - Y :class:`treatedWith` X
   * - X :class:`harmfulFor` Y
     - Y :class:`harmedBy` X
   * - Substance :class:`harmfulFor` {harmful effect, strength, food product}
     - 
   * - X :class:`growsIn` Y
     - Y :class:`growthEnvironmentFor` X
   * - X :class:`hasPhase` Y
     - Y :class:`phaseOf` X
   * - FoodProduct :class:`hasState` Physical state
     - 
   * - X :class:`hasForm` Y
     - Y :class:`isFormOf` X
   * - FoodProduct :class:`hasForm` Physical form
     - 
   * - Container :class:`hasForm` Physical form
     - 
   * - FoodProduct :class:`packedIn` Container
     - 
   * - X :class:`hasPrice` MoneyAmount
     - 
   * - Substance :class:`measuredIn` Unit of measurement
     - 

.. seealso::
   
   Reference to a related section of the Proposal

