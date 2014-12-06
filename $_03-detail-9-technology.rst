
.. _$_03-detail-8-technology:

===========
Technology
===========

Search
------

User Interface
^^^^^^^^^^^^^^

screen shot

Sample Searches
^^^^^^^^^^^^^^^

list from long proposal

Graphs
------


.. seealso::

   Reference to a related section of the Proposal

REST
----


<consider moving to Concept - Detail>

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

   