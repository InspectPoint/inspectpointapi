# Contacts API
Retrieve, create, and edit contacts

# LIST CONTACTS
## HTTP Method
##### GET  /external/api/v1/contacts

## Example
```
 curl https://${tenant_subdomain}.inspectpoint.com/external/api/v1/contacts \
     -X GET \
     -H 'Content-Type: application/json' \
     -H 'Api-Key: API_KEY_HERE' \
```

## Parameters
+ offset (defaults to 0)
+ limit  (defaults to 50)
+ building_id (filter by building)

## Example Response

+ Response 200 (application/json)
```json
{  
   "contacts":[  
     {
        "id": 2,
        "name": "Phil Surge",
        "title": "Facility Manager",
        "cell_phone_number": "518-555-5551",
        "business_phone_number": "",
        "email": "phil@ndh.com",
        "notes": ""
     },
     {  
       "id": 66,
       "name": "Nick D",
       "title": "Owner",
       "cell_phone_number": "518-555-1234",
       "business_phone_number": "",
       "email": "nick@ndh.com",
       "notes": ""      
    }
   ]
}
```
# CONTACT DETAIL
## HTTP Method
##### GET  /external/api/v1/contacts/id

## Example
```
 curl https://${tenant_subdomain}.inspectpoint.com/external/api/v1/contacts/${contact_id} \
     -X GET \
     -H 'Content-Type: application/json' \
     -H 'Api-Key: API_KEY_HERE' \
```

## Example Response

+ Response 200 (application/json)
```json
{  
   "contact":
   {  
     "id": 66,
     "name": "Nick D",
     "title": "Owner",
     "cell_phone_number": "518-555-1234",
     "business_phone_number": "",
     "email": "nick@ndh.com",
     "notes": ""      
   }
}
```

# CREATE CONTACT
## HTTP Method
##### PUT  /external/api/v1/contacts

## Example
```
 curl https://${tenant_subdomain}.inspectpoint.com/external/api/v1/contacts\
     -X GET \
     -H 'Content-Type: application/json' \
     -H 'Api-Key: API_KEY_HERE' \
     -d
```

## Request Attributes

Parameter Name | Required | Data Type
-------------- | -------------- | --------------
name | Required | String
address1 | Required | String
address2 | Required | String
city | Required | String
state | Required | String
zip | Required | String
notes | Required | String
title | Required | Integer
reference_number | Required | Integer
cell_phone_number | Required | String
home_phone_number | Required | String
business_phone_number | Required | String
business_fax_number | Required | String
company | Required | String

## Example Response

+ Response 200 (application/json)
```json
{  
   "contact":
     {  
       "id": 66,
       "name": "Nick D",
       "title": "Owner",
       "cell_phone_number": "518-555-1234",
       "business_phone_number": "",
       "email": "nick@ndh.com",
       "notes": ""      
     }  
}
```

# UPDATE CONTACT
## HTTP Method
##### POST  /external/api/v1/contacts/id

## Example
```
 curl https://${tenant_subdomain}.inspectpoint.com/external/api/v1/contacts/${contact_id} \
     -X GET \
     -H 'Content-Type: application/json' \
     -H 'Api-Key: API_KEY_HERE' \
     -d
```

## Request Attributes
Parameter Name | Required | Data Type
-------------- | -------------- | --------------
name | Required | String
address1 | Required | String
address2 | Required | String
city | Required | String
state | Required | String
zip | Required | String
notes | Required | String
title | Required | Integer
reference_number | Required | Integer
cell_phone_number | Required | String
home_phone_number | Required | String
business_phone_number | Required | String
business_fax_number | Required | String
company | Required | String

## Example Response

+ Response 200 (application/json)
```json
{  
   "contact":
   {  
     "id": 66,
     "name": "Nick D",
     "title": "Owner",
     "cell_phone_number": "518-555-1234",
     "business_phone_number": "",
     "email": "nick@ndh.com",
     "notes": ""      
   }
}
```
