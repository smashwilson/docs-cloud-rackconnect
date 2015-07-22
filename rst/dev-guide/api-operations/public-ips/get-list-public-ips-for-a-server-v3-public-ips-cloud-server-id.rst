
.. THIS OUTPUT IS GENERATED FROM THE WADL. DO NOT EDIT.

=============================================================================
List Public Ips For A Server -  rackconnect
=============================================================================

List Public Ips For A Server
~~~~~~~~~~~~~~~~~~~~~~~~~

`Request <get-list-public-ips-for-a-server-v3-public-ips-cloud-server-id.html#request>`__
`Response <get-list-public-ips-for-a-server-v3-public-ips-cloud-server-id.html#response>`__

.. code::

    GET /v3/public_ips/cloud_server_id

				List public IP addresses for a server. 

This operation 				lists all 				public IP addresses 				for the specified ``cloud_server_id``.



This table shows the possible response codes for this operation:


+--------------------------+-------------------------+-------------------------+
|Response Code             |Name                     |Description              |
+==========================+=========================+=========================+
|200                       |OK                       |Success.                 |
+--------------------------+-------------------------+-------------------------+
|400                       |Bad request              |The input was not in the |
|                          |                         |correct format.          |
+--------------------------+-------------------------+-------------------------+
|404                       |Not found                |The requested item was   |
|                          |                         |not found.               |
+--------------------------+-------------------------+-------------------------+
|500                       |Internal server error    |An unexpected error has  |
|                          |                         |occurred.                |
+--------------------------+-------------------------+-------------------------+


Request
^^^^^^^^^^^^^^^^^

This table shows the URI parameters for the request:

+--------------------------+-------------------------+-------------------------+
|Name                      |Type                     |Description              |
+==========================+=========================+=========================+
|cloud_server_id           |xsd:string               |Specifies the UUID of a  |
|                          |                         |cloud server.            |
+--------------------------+-------------------------+-------------------------+



This table shows the query parameters for the request:

+--------------------------+-------------------------+-------------------------+
|Name                      |Type                     |Description              |
+==========================+=========================+=========================+
|                          |xsd:string *(Required)*  |                         |
+--------------------------+-------------------------+-------------------------+







**Example List Public Ips For A Server: JSON request**


.. code::

    curl --include \
     'https://dfw.rackconnect.api.rackspacecloud.com/v3/{tenant_id}/public_ips'


Response
^^^^^^^^^^^^^^^^^^





**Example List Public Ips For A Server: JSON response**


.. code::

    200 (OK)
    Content-Type: application/json
    
    [
        {
            "created": "2014-05-30T03:23:42Z",
            "cloud_server": {
                "cloud_network": {
                    "cidr": "192.168.100.0/24",
                    "created": "2014-05-25T01:23:42Z",
                    "id": "07426958-1ebf-4c38-b032-d456820ca21a",
                    "name": "RC-CLOUD",
                    "private_ip_v4": "192.168.100.5",
                    "updated": "2014-05-25T02:28:44Z"
                },
                "created": "2014-05-30T02:18:42Z",
                "id": "d95ae0c4-6ab8-4873-b82f-f8433840cff2",
                "name": "RCv3TestServer1",
                "updated": "2014-05-30T02:19:18Z"
            },
            "id": "2d0f586b-37a7-4ae0-adac-2743d5feb450",
            "public_ip_v4": "203.0.113.110",
            "status": "ACTIVE",
            "status_detail": null,
            "updated": "2014-05-30T03:24:18Z"
        }
    ]
