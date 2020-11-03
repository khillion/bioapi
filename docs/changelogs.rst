.. dabeplech

.. _changelog:

**********
Changelogs
**********

Summary of developments of dabeplech library.

v0.4
====

v0.4.0
------

* Add an endpoint to query Ontology Lookup Service  https://www.ebi.ac.uk/ols/index (https://github.com/motleystate/dabeplech/pull/30)

    * a first ``get_term`` method to query by ontology term ID

v0.3
====

v0.3.0
------

* Add an endpoint to query the HAL (https://hal.archives-ouvertes.org) endpoint to retrieve information in the JSON format. (https://github.com/motleystate/dabeplech/pull/29)

v0.2
====

v0.2.0
------

* Add an endpoint to query the DOI (https://dx.doi.org) endpoint to retrieve information in the JSON format. (https://github.com/motleystate/dabeplech/pull/28)

v0.1
====

v0.1.1
------

* Fix bug and deal with variant of NCBI taxonomy item page (e.g. ``tax_id=12345``)

v0.1.0
------

* Add scrapper for NCBI taxonomy (https://github.com/motleystate/dabeplech/pull/24)
* Add ``NCBITaxonomyScrapAPI`` that mimics API behaviour to retrieve hierarchy information for a given ``tax_id`` (https://github.com/motleystate/dabeplech/pull/24)
* add first PDBe REST endpoints (https://github.com/motleystate/dabeplech/pull/21)

v0.0
====

v0.0.6
------

* LIST of entries described in KEGG models only contains the necessary fields (https://github.com/motleystate/dabeplech/pull/20)
* deal with empty responses (`200`) from `FIND` operation on KEGG API (https://github.com/motleystate/dabeplech/pull/19)

v0.0.5
------

* ``FIND`` works and gives a ``json`` output for pathway and ko. It can be used using ``.find(database, query)`` (https://github.com/motleystate/dabeplech/pull/16)
* ``LINK`` has been splitted in two methods (there are using the same endpoint, but having two different methods make more sense). (https://github.com/motleystate/dabeplech/pull/16)

    - ``link_db(target_db, source_db)``: allows retrieval of database to database cross-references
    - ``link_entries(target_db, dbentries)``: allows retrieval for a selected number of entries

* replace ``get_all()`` by ``list()`` for LIST operation on KEGG API
* Add model description and API for KEGG module (https://github.com/motleystate/dabeplech/pull/17)
* change name to ``dabeplech``

v0.0.4
------

* Replace models for pathway and ko list by simpler model

v0.0.3
------

* Add parser and api for KEGG pathway list (https://github.com/khillion/dabeplech/pull/10)
* Add parser and api for KEGG ko list (https://github.com/khillion/dabeplech/pull/10)
* Change ``name`` attribute to ``names`` for KEGG
* Handle reference with no pubmed ID (https://github.com/khillion/dabeplech/pull/7)

v0.0.2
------

* Add parser for KEGG pathway response

v0.0.1
------

This is the first release of dabeplech:

* Parser for KEGG orthology response
* Base structure for KEGG API

    * Return structured dict if parser available
    * If no parser available, return raw response from KEGG API

* Base structure for TogoWS API
