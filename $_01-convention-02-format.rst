
.. _$_02-convention-format:

=======================
Format Used in Proposal
=======================

USDA **requirements** are formatted as follows:

.. rst:role:: USDA #12

   Support capture/documentation of metadata for food composition and non-composition data.

**Ontology terms** are formatted as follows:

- :class:`schema:sameAs` (the schema.org facet term meaning that A is the same as B)
- :class:`ncit:C46090` (the NIH NCI facet term code for the facet term "Glycemic Index")
- :class:`agrontology:isUsedToMake` (the UN FAO term meaning that A is used to make B)

A **word** or **phrase** that is a link to a URL is formatted as follows: `food labeling services for the USDA community <http://www.ontomatica.com/public/organizations/BETV/Intro.html>`_

A **term** that is defined in the glossary is formatted as follows: :ref:`application services <terms-Application-Service>`

A bibliographic **references** is formatted as follows: See :cite:`5002` for more information about ...

.. sidebar:: Sidebar

   Provides complementary detail

**Discussion** about a design or approach.

- point 1
- point 2
- point 3
- point 4

Illustration of a **REST conversation**

.. http:get:: /users/(int:user_id_)/posts/(tag)

.. seealso::
     
   Reference to a related section of the Proposal

.. tip::
   
   Advice based on experience with managing similar issues
   
.. attention::

   Warning that an alternative approach may produce an ineffective result

.. danger::

   Advice that an alternative approach will produce a poor or unintended outcome

Mathematics
-----------

The INFOODS tag for the calculation "amino acids, total essential" is AAE8. There are eight basic essential amino acids. AAE8 is represented as follows:

.. math:: \begin{align}AAE8=\sum_{1}^8(essential-amino-acids)\end{align}

Which reduces to:

.. math::
   \begin{align}
   AAE8=[isoleucine]\\
   +[leucine]\\
   +[lysine]\\
   +[methionine]\\
   +[phenylalanine]\\
   +[threonine]\\
   +[tryptophan]\\
   +[valine]
   \end{align}

Introducing semantic syntax in the form of a `CURIE <http://en.wikipedia.org/wiki/CURIE>`_ where the authority is "infoods" and the `Universal Resource Identifier <http://en.wikipedia.org/wiki/Uniform_resource_identifier>`_ is the unique INFOODS "tag":

.. math::
   \begin{align}[infoods:AAE8]=[infoods:ILE]\\
   +[infoods:LEU]\\
   +[infoods:LYS]\\
   +[infoods:MET]\\
   +[infoods:PHE]\\
   +[infoods:THR]\\
   +[infoods:TRP]\\
   +[infoods:VAL]
   \end{align}

Now replace the operator symbol "+" with its equivalent semantic operator :class:`[ncit:C64911]`.

.. math::
   \begin{align}
   [infoods:AAE8]=[infoods:ILE]\\
   [ncit:C64911][infoods:LEU]\\
   [ncit:C64911][infoods:LYS]\\
   [ncit:C64911][infoods:MET]\\
   [ncit:C64911][infoods:PHE]\\
   [ncit:C64911][infoods:THR]\\
   [ncit:C64911][infoods:TRP]\\
   [ncit:C64911][infoods:VAL]
   \end{align}

To be absolutely clear, the unit to express a value for an amino acid is "grams per 100 grams per edible portion" :class:`[vocal:v62177]`:

.. math::
   \begin{align}
   [infoods:AAE8]_{g-100-g-EP}=\\
   ([infoods:ILE][vocal:v62177])\\
   [ncit:C64911]([infoods:LEU][vocal:v62177])\\
   [ncit:C64911]([infoods:LYS][vocal:v62177])\\
   [ncit:C64911]([infoods:MET][vocal:v62177])\\
   [ncit:C64911]([infoods:PHE][vocal:v62177])\\
   [ncit:C64911]([infoods:THR][vocal:v62177])\\
   [ncit:C64911]([infoods:TRP][vocal:v62177])\\
   [ncit:C64911]([infoods:VAL][vocal:v62177])
   \end{align}

Each amino acid in a sample will have a <value> in the form of a floating point number :class:`[xsd:float]`:

.. math::
   \begin{align}
   [infoods:AAE8]_{[vocal:v62177]}=\\
   ([infoods:ILE][vocal:v62177][xsd:float]<value>)\\
   [ncit:C64911]([infoods:LEU][vocal:v62177][xsd:float]<value>)\\
   [ncit:C64911]([infoods:LYS][vocal:v62177][xsd:float]<value>)\\
   [ncit:C64911]([infoods:MET][vocal:v62177][xsd:float]<value>)\\
   [ncit:C64911]([infoods:PHE][vocal:v62177][xsd:float]<value>)\\
   [ncit:C64911]([infoods:THR][vocal:v62177][xsd:float]<value>)\\
   [ncit:C64911]([infoods:TRP][vocal:v62177][xsd:float]<value>)\\
   [ncit:C64911]([infoods:VAL][vocal:v62177][xsd:float]<value>)
   \end{align}

A semantic record will have the following syntax:

:class:`[infoods:AAE8]` :class:`[vocal:v62177]` = :class:`[infoods:ILE]` :class:`[vocal:v62177]` :class:`[xsd:float]` <value> :class:`[ncit:C64911]` :class:`[infoods:LEU]` :class:`[vocal:v62177]` :class:`[xsd:float]` <value> :class:`[ncit:C64911]` :class:`[infoods:LYS]` :class:`[vocal:v62177]` :class:`[xsd:float]` <value> :class:`[ncit:C64911]` :class:`[infoods:MET]` :class:`[vocal:v62177]` :class:`[xsd:float]` <value> :class:`[ncit:C64911]` :class:`[infoods:PHE]` :class:`[vocal:v62177]` :class:`[xsd:float]` <value> :class:`[ncit:C64911]` :class:`[infoods:THR]` :class:`[vocal:v62177]` :class:`[xsd:float]` <value> :class:`[ncit:C64911]` :class:`[infoods:TRP]` :class:`[vocal:v62177]` :class:`[xsd:float]` <value> :class:`[ncit:C64911]` :class:`[infoods:VAL]` :class:`[vocal:v62177]` :class:`[xsd:float]` <value>

The operator symbol "=" is replaced with its equivalent semantic operator :class:`[ncit:C54125]`. A complete semantic record will have the following syntax:

:class:`[infoods:AAE8]` :class:`[vocal:v62177]` :class:`[ncit:C54125]` :class:`[infoods:ILE]` :class:`[vocal:v62177]` :class:`[xsd:float]` <value> :class:`[ncit:C64911]` :class:`[infoods:LEU]` :class:`[vocal:v62177]` :class:`[xsd:float]` <value> :class:`[ncit:C64911]` :class:`[infoods:LYS]` :class:`[vocal:v62177]` :class:`[xsd:float]` <value> :class:`[ncit:C64911]` :class:`[infoods:MET]` :class:`[vocal:v62177]` :class:`[xsd:float]` <value> :class:`[ncit:C64911]` :class:`[infoods:PHE]` :class:`[vocal:v62177]` :class:`[xsd:float]` <value> :class:`[ncit:C64911]` :class:`[infoods:THR]` :class:`[vocal:v62177]` :class:`[xsd:float]` <value> :class:`[ncit:C64911]` :class:`[infoods:TRP]` :class:`[vocal:v62177]` :class:`[xsd:float]` <value> :class:`[ncit:C64911]` :class:`[infoods:VAL]` :class:`[vocal:v62177]` :class:`[xsd:float]` <value>

.. |_| unicode:: 0x80

