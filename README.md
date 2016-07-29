ErlangMS Schemas Catalogs
====

ErlangMS is a platform developed in *Erlang/OTP* to facilitate the integration of systems through a service-oriented approach for the systems of the University of Brazilia. This work is the result of efforts made in the Master of Applied Computing at the University of Brasilia by graduate student *Everton Vargas Agilar*. 

The platform consists of a Enterprise Service Bus (ESB), called *EmsBus*, and a *documented architecture* to implement the services in Erlang, Java and future in .NET Framework languages.

###What's in this folder

This folder contains the JSON Schemas Draft 4 to describe the service contract layout of the ErlangMS service catalogs.

Useful links:
* Tool to validate JSON Schemas -- http://jsonschema.net/#/home
* Portal json-schema --  http://json-schema.org/


###Sample os service contract 

```
{
  "name": "/hackathon/cursos/:id",
  "comment": "Lista um curso pelo seu identificador",
  "owner": "hackathon",
  "version": "1.0.0",
  "service": "ems_dynamic_view_service:find_by_id",
  "url": "/hackathon/cursos/:id",
  "type": "GET",
  "public": true,
  "lang": "erlang",
  "authentication": "oauth",
  "querystring": {
    "filter": "",
    "fields": "semestre, nome_curso",
    "limit_ini": 1,
    "limit_offset": 100,
    "sort": "semestre desc, nome_curso asc"
  }
}
```

JSON Schema for validation: in https://github.com/erlangMS/schema/blob/master/schema_catalog_v1.0.0.json
