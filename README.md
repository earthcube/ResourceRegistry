# ResourceRegistry
Repository for resources related to the Resource Registry (ECRR) component of the GeoCODES platform.
[ecrrjsonschema1.0.json](./ecrrjsonschema1.0.json)
This is the json schema that should be used for validating the ECRR JSON-LD
It includes the flexibility to have oneOf (object/array)

[ecrrjsonschema1.0_jsonforms.json](./ecrrjsonschema1.0_jsonforms.json)
This is pulled from the JSONForms UI. Changes here will not be reflected in the UI...
Change UI. In the Chrome Vue UI toolbar naviagate to Jsonforms element and copy the value to the schema object.

A schema for use in a jsonforms application  ecrrjsonschema1.0_jsonforms.json
* _simplifies/removes flexibility:_  deletes the many oneOf, and anyOf options for which are used to allow
for abilities like (string, arrayof(string)), (object,arrayOf(object)) A JSONForms interface
containting these is  difficult for users to navigate. Basically, if it could be an
array, it is an array.
* _moves/duplicates the additionalProperties to the top level_. The JSONFOrms app cannot
properly handle the nested fields in additionalProperties, simply.
  * code moves objects to and from additionalProperties on load/save.
