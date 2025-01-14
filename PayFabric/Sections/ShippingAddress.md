Shipping Address
=================

The PayFabric shipping addresses API is used for managing customer shipping addresses.  Please note that all requests require API authentication, see our [guide](Authentication.md) on how to authenticate.

Create Shipping Address
---------------------------

* `Post /payment/3.1/api/address/` will return the specified address

###### Response
<pre>
{
    "Customer": "Test Shipping",
    "City": "Ahaheim",
    "Country": "US",
    "Email": "sample@email.com",
    "Line1": "test address line 1",
    "Line2": "test address line 2",
    "Line3": "test address line 3",
    "Phone": "1234567890",
    "State": "CA",
    "Zip": "12345",
    "FirstName": "Testfirst",
    "LastName": "Testlast"
}
</pre>

###### Response
<pre>
{
    "Customer": "Test Shipping",
    "ID": "74b6d31f-4e57-4bae-8fa4-cbed44d525be",
    "Line1": "test address line 1",
    "Line2": "test address line 2",
    "Line3": "test address line 3",
    "State": "CA",
    "City": "Ahaheim",
    "Country": "US",
    "Zip": "12345",
    "Email": "sample@email.com",
    "Phone": "1234567890",
    "FirstName": "Rena",
    "LastName": "Wu"
}
</pre>

Delete Shipping Address
-----------------------
* `DELETE /payment/3.1/api/{AddressId}` will return the specified address

###### Response
A successful `DELETE` will result in a HTTP 204 No Content Response.

A failed `DELETE` may result in a HTTP 400 Bad Request Response if the specified address does not exist or the Device ID used for the Security Token does not match or post failed.

A failed `DELETE` may result in a HTTP 401 Unauthorized Response if the authorization is failed.
