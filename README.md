# ResourceRegistry
Repository for resources related to the Resource Registry (ECRR) component of the GeoCODES platform. 

A schema for use in a jsonforms application  ecrrjsonschema1.0_jsonforms.json
this deletes the many oneOf, and anyOf options for which are used to allow
for abilities like (string, arrayof(string)), (object,arrayOf(object)) that 
make the interface difficult for users to navigate. Basically, if it could be an
array, it is an array.
