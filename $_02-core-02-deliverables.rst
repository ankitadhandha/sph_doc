
.. _$_02-core-02-deliverables:

============
Deliverables
============

See :cite:`5382` for link to Wikipedia.

Ontomatica will deliver a :ref:`complete system <terms-Complete-System>` |_| composed of (1) :ref:`application services <terms-Application-Service>` |_| for :ref:`end-users <terms-End-User>`; (2) :ref:`deposition services <terms-Deposition-Service>` |_| for :ref:`food suppliers <terms-Food-Supplier>` |_| and :ref:`investigators <terms-Investigator>`; (3) :ref:`data services <terms-Data-Service>` |_| for production applications and investigators; (4) :ref:`infrastructure services <terms-Infrastructure-Service>` |_| for executing all services under demanding on-line conditions; (5) :ref:`operating services <terms-Operating-Service>` |_| for managing and controlling all services; and (6) :ref:`development services <terms-Development-Service>` |_| for information :ref:`curators <terms-Curator>` |_| and :ref:`food compilers <terms-Food-Compiler>`.

Ontomatica :ref:`application services <terms-Application-Service>` |_| manipulate :ref:`label classes <terms-Label-Class>`. Ontomatica has developed a library of label classes. USDA will identify the label classes required for :ref:`label project <terms-Label-Project>`. Ontomatica then will package USDA-identified classes to operate in label project applications. Label classes are composed of :ref:`facets <terms-Facet>`, :ref:`predicates <terms-Predicate>` |_| and :ref:`data <terms-Data>`. Ontomatica :ref:`Navigator <terms-Navigator>` |_| loads label classes and :ref:`items <terms-Item>` |_| that are members of label classes. Navigator presents information in two views: (1) :ref:`listing page <terms-Listing-Page>` |_| where :ref:`items <terms-Item>` |_| that are members of label classes are displayed; (2) :ref:`landing page <terms-Landing-Page>` |_| where all properties of a single :ref:`item <terms-Item>` |_| are displayed.

Ontomatica :ref:`deposition services <terms-Deposition-Service>` |_| accept data from food suppliers and investigators; validate data deposits; add value to deposits; and, update :ref:`data services <terms-Data-Service>`. Two options are available to deposit data: (1) :ref:`message deposit <terms-Message-Deposit>` |_| is an electronic submissions from GS1; and, (2) :ref:`web deposit <terms-Web-Deposit>` |_| is on-line interface for food suppliers and investigators. Ontomatica application, deposition and data services will support two data groups: (1) :ref:`USDA Select <terms-USDA-Select>` |_| data groups that meet the requirements for managing GS1 data; and (2) :ref:`USDA Prime <terms-USDA-Prime>` |_| data groups that meet and exceed USDA food :ref:`composition <terms-Food-Composition-Data>` |_| and :ref:`non-composition <terms-Food-Non-Composition-Data>` information requirements. Ontomatica deposition services will automate :ref:`current USDA NDL/FSRG practices <terms-USDA-NDL-FSRG-Practice>` used to produce their current databases.

Ontomatica :ref:`data services <terms-Data-Service>` |_| manage data deposits. Data services have two components: (1) data for :ref:`application services <terms-Application-Service>` |_| that is stored in :ref:`MySQL <terms-MySQL>`; and, (2) data for food suppliers and investigators that is available through :ref:`REST <terms-REST>` |_| services.

All services execute on :ref:`infrastructure services <terms-Infrastructure-Service>`. The major components of infrastructure services are :ref:`Intel Xeon servers <terms-Intel-Xeon-server>` |_| and :ref:`LAMP <terms-LAMP>`. :ref:`Operating services <terms-Operating-Service>` |_| will monitor primary CPU and storage and :ref:`failover <terms-Failover>` |_| to secondary services when necessary.

Curators and food compilers use Ontomatica :ref:`development services <terms-Development-Service>` |_| to manage and maintain deposits. Development services also manage the process of promoting a new version of label project applications from :ref:`development <terms-Development>` |_| to :ref:`quality assurance <terms-Quality-Assurance>` |_| to :ref:`production <terms-Production>`.

Ontomatica will provide source code for application services, deposition services, data services, and development service according to licensing terms.

.. |_| unicode:: 0x80

See :ref:`Services, Products and Technologies <$_02-core-06-services>` |_| for detail.

