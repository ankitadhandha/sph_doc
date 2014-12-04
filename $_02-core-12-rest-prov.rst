
.. _$_02-core-12-rest-prov:

=========================
REST Services and Reports
=========================

This section addresses:

.. rst:role:: USDA #6

   Permit export of composition and analytical data and conversion of composition data to an application development format.

.. rst:role:: USDA #10

   Permit assembly of ad hoc databases to suit individual needs.

.. rst:role:: USDA #11

   Permit export of ad hoc data.

Table of contents for REST Service and Reports
----------------------------------------------

.. contents::
   :depth: 2
   :local:

:ref:`Label project <terms-Label-Project>` |_| data will be available to :ref:`investigators <terms-Investigator>` |_| via :ref:`REST <terms-REST>` |_| (Representational State Transfer) services. REST is a simple stateless architecture that runs over HTTP. REST service reads a designated Web page that contains an XML file in RDF format. XML/RDF file describes and includes label project data. Data is returned to investigator in :ref:`JSON-LD <terms-JSON-LD>` |_| format.

.. figure:: 2_REST.png
   :align: center

-----------------------------
General Structure of REST API
-----------------------------

The following illustrates the retrieval of blog posts by a specific user and identified by a specific tag. The general structure is:

.. http:get:: /users/(int:user_id_)/posts/(tag)

   **Example request**:

   .. sourcecode:: http

      GET /users/123/posts/web HTTP/1.1
      Host: example.com
      Accept: application/json, text/javascript

   **Example response**:

   .. sourcecode:: http

      HTTP/1.1 200 OK
      Vary: Accept
      Content-Type: text/javascript

      [
        {
          "post_id": 12345,
          "author_id": 123,
          "tags": ["server", "web"],
          "subject": "I tried JavaScript"
        },
        {
          "post_id": 12346,
          "author_id": 123,
          "tags": ["html5", "standards", "web"],
          "subject": "We moved to HTML 5"
        }
      ]

   :query sort: one of ``hit``, ``created-at``
   :query offset: offset number. default is 0
   :query limit: limit number. default is 30
   :reqheader Accept: the response content type depends on :mailheader:`Accept` header
   :reqheader Authorization: optional OAuth token to authenticate
   :resheader Content-Type: this depends on :mailheader:`Accept` header of request
   :statuscode 200: no error
   :statuscode 404: there's no user

---------------------------
OnDemand REST Data Services
---------------------------

Discussion of REST and :ref:`OnDemand <terms-OnDemand>` 

Sample USDA REST API
^^^^^^^^^^^^^^^^^^^^

Structure:

.. http:get:: /input specification/operation specification/output specification/operation_options

Specific:

::

   http://usda.ars.gov/rest/<input_specification>/<operation_specification>/[<output_specification>][?<operation_options>]

Query Parameters: Input Specification
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Input portion of URL tells service which records to use as subject of query. This is further subdivided into two or more locations in URL "path" as follows:

::

    <input_specification> = <domain>/<namespace>/<identifiers>
    
      <domain> = food | compound | NFP_values | <other inputs>
    
        food domain <namespace> = USDA_fid | sourceid/<source name> | sourceall/<source name> | name | <xref>
    
        compound domain <namespace> = PC_cid | name | inchikey | <xref>
    
        <xref> = xref / {RegistryID | RN | NCBI_ProteinGI | NCBI_TaxonomyID }
    
        <source_name> = any valid Branded Food depositor name
    
      NFP_values domain <namespace> = NFP_id | type/<NFP type> | sourceall/<source name> | activity/<activity column name> | {_to_be_specified_}
    
        <NFP_type> = all | panel | summary | {_to_be_specified_}
    
      <identifiers> = comma-separated list of positive integers (e.g. PC_cid, USDA_fid, NFP_id) or identifier strings (source, inchikey)
    
        <other_inputs_to_be_specified_> = sources / [substance, assay] | conformers

Query Parameters: Operation Specification
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Operation part of URL tells service what to do with input records - such as to retrieve whole record or specific properties of a food. Construction of this part of "path" will depend on operation. If no operation is specified, default is to retrieve entire record. Available operations dependent on input domain. For example, certain operations are applicable only to foods, compounds and not NFP_values.

::

    food domain <operation_specification> = record | <food_property> | synonyms | PC_cids | NFP_values | classification | <xrefs> | description
    
      <food_property> = property / [comma-separated list of property tags]
    
      <xrefs> = xrefs / [comma-separated list of xrefs tags]
    
      NFP domain <operation_specification> = record | NFP_ids | USDA_fids | PC_cids | description | summary | classification | xrefs

Query Parameters: Output Specification
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Final portion of URL tells service what output format is desired. Output format also can be specified in HTTP Accept field of request header.

::

    <output:specification> = JSON | CSV | TXT

Example: Full-record retrieval
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

::

    http://usda.ars.gov/rest/food/USDA_fid/2244/JSON

Request: Food property tables
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Request properties for a food (USDA_fid) or compound (PC_cid).

::

    http://usda.ars.gov/rest/food/USDA_fid/3114/property/JSON

Return food property table
""""""""""""""""""""""""""

.. csv-table::
   :header: "Property", "Notes"
   :widths: 20, 20

   "_to_be_specified_", "_to_be_specified_"
   "_to_be_specified_", "_to_be_specified_"

Variation: Return Nutrient Fact Panel (NFP)
"""""""""""""""""""""""""""""""""""""""""""

.. csv-table::
   :header: "Options", "Allowed Values", "meaning"
   :widths: 20, 20, 20

   "NFP_type", "all, primary, secondary", "Type of NFP to return given, USDA_fids, PC_cids"

Variation: Return dates
"""""""""""""""""""""""

.. csv-table::
   :header: "Date", "Meaning"
   :widths: 20, 20

   "Deposition", "when an USDA_fid or NFP_id first appeared"
   "Modification", "when an USDA_fid or NFP_id was last modified"
   "Hold", "when an USDA_fid or NFP_id will be released"
   "Creation", "when a USDA_fid or NFP_id first appeared"
   "Deprecation", "when a USDA_fid or NFP_id is no longer active"

Variation: Return Cross References (XRefs)
""""""""""""""""""""""""""""""""""""""""""

.. csv-table::
   :header: "Cross Reference", "Meaning"
   :widths: 20, 20

   "RegistryID", "external registry identifier"
   "PubMedID", "NCBI PubMed identifier"
   "DBURL", "external database home page URL"
   "TaxonomyID", "NCBI taxonomy identifier"
   "SourceName", "external depositor name"
   "SourceCategory", "depositor category(ies)"

.. seealso:: Model sites that implement REST

   * `ChemAxon concepts <http://www.chemaxon.com/products/jchem-web-services/>`_

   * `ChemAxon application programming interface (APIs) <https://restdemo.chemaxon.com/apidocs/>`_

.. |_| unicode:: 0x80
