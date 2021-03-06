
.. THIS OUTPUT IS GENERATED FROM THE WADL. DO NOT EDIT.

.. _get-retrieve-list-of-key-pairs-os-keypairs:

Retrieve list of key pairs
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. code::

    GET /os-keypairs

This operation retrieves a list of server key pairs.


This table shows the possible response codes for this operation:


+--------------------------+-------------------------+-------------------------+
|Response Code             |Name                     |Description              |
+==========================+=========================+=========================+
|200                       |Success                  |Request succeeded.       |
+--------------------------+-------------------------+-------------------------+
|400                       |Error                    |A general error has      |
|                          |                         |occured.                 |
+--------------------------+-------------------------+-------------------------+
|401                       |Unauthorized             |Unauthorized.            |
+--------------------------+-------------------------+-------------------------+
|403                       |Forbidden                |Forbidden.               |
+--------------------------+-------------------------+-------------------------+
|405                       |Bad Method               |Bad method.              |
+--------------------------+-------------------------+-------------------------+
|409                       |Conflicting Reqest       |Conflicting request.     |
+--------------------------+-------------------------+-------------------------+
|413                       |Over Limit               |The number of items      |
|                          |                         |returned is above the    |
|                          |                         |allowed limit.           |
+--------------------------+-------------------------+-------------------------+
|500                       |API Fault                |API fault.               |
+--------------------------+-------------------------+-------------------------+
|503                       |Service Unavailable      |The requested service is |
|                          |                         |unavailable.             |
+--------------------------+-------------------------+-------------------------+


Request
""""""""""""""""








This operation does not accept a request body.




Response
""""""""""""""""





This table shows the body parameters for the response:

+-------------------------------+-----------------------+----------------------+
|Name                           |Type                   |Description           |
+===============================+=======================+======================+
|**keypairs**                   |Array                  |An array of key pairs.|
+-------------------------------+-----------------------+----------------------+
|keypairs.\ **keypair**         |Object                 |A container of key    |
|                               |                       |pair details.         |
+-------------------------------+-----------------------+----------------------+
|keypairs.keypair.\             |String                 |A short sequence of   |
|**fingerprint**                |                       |bytes used to         |
|                               |                       |authenticate, or look |
|                               |                       |up, a longer public   |
|                               |                       |key.                  |
+-------------------------------+-----------------------+----------------------+
|keypairs.keypair.\ **name**    |String                 |The name of the key   |
|                               |                       |pair.                 |
+-------------------------------+-----------------------+----------------------+
|keypairs.keypair.\             |String                 |The public ssh key    |
|**public_key**                 |                       |value.                |
+-------------------------------+-----------------------+----------------------+







**Example Retrieve list of key pairs: JSON response**


.. code::

       Status Code: 200 OK
       Content-Length: 540
       Content-Type: application/json
       Date: Thu, 02 Apr 2015 18:09:36 GMT, Thu, 02 Apr 2015 18:09:36 GMT
       Server: Jetty(9.2.z-SNAPSHOT)
       Via: 1.1 Repose (Repose/6.2.1.2)
       X-Compute-Request-Id: req-5a9c3b9d-67cf-4b7f-b31d-0670e1c667a0


.. code::

   {
       "keypairs":[
           {
               "keypair":{
                   "fingerprint":"15:b0:f8:b3:f9:48:63:71:cf:7b:5b:38:6d:44:2d:4a",
                   "name":"name_of_keypair-601a2305-4f25-41ed-89c6-2a966fc8027a",
                   "public_key":"ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAAAgQC+Eo/RZRngaGTkFs7I62ZjsIlO79KklKbMXi8F+KITD4bVQHHn+kV+4gRgkgCRbdoDqoGfpaDFs877DYX9n4z6FrAIZ4PES8TNKhatifpn9NdQYWA+IkU8CuvlEKGuFpKRi/k7JLos/gHi2hy7QUwgtRvcefvD/vgQZOVw/mGR9Q== Generated by Nova\n"
               }
           }
       ] 
    }
   




