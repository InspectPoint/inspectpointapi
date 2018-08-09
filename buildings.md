# Buildings API
Retrieve, create, and edit buildings

# LIST BUILDINGS
## HTTP Method
##### GET  /external/api/v1/buildings

## Example
```
 curl https://${tenant_subdomain}.inspectpoint.com/external/api/v1/buildings \
     -X GET \
     -H 'Content-Type: application/json' \
     -H 'Api-Key: API_KEY_HERE' \
```

## Parameters
+ offset (defaults to 0)
+ limit  (defaults to 50)

## Example Response

+ Response 200 (application/json)
```json
{  
   "buildings":[  
      {  
         "id":146,
         "name":"Free Pizza",
      },
      {  
         "id":121,
         "name":"$5.00 off",         
      }
   ]
}
```
# BUILDING DETAIL
## HTTP Method
##### GET  /external/api/v1/buildings/id

## Example
```
 curl https://${tenant_subdomain}.inspectpoint.com/public/api/v1/buildings/${building_id} \
     -X GET \
     -H 'Content-Type: application/json' \
     -H 'Api-Key: API_KEY_HERE' \
```

## Example Response

+ Response 200 (application/json)
```json
{  
   "building":
      {  
         "id":146,
         "name":"Free Pizza",
      }  
}
```

# CREATE BUILDING
## HTTP Method
##### PUT  /external/api/v1/buildings

## Example
```
 curl https://${tenant_subdomain}.inspectpoint.com/public/api/v1/buildings/${building_id} \
     -X GET \
     -H 'Content-Type: application/json' \
     -H 'Api-Key: API_KEY_HERE' \
     -d
```

## Request Attributes
Parameter Name | Required | Data Type
-------------- | -------------- | --------------
Name | Required | String

## Example Response

+ Response 200 (application/json)
```json
{  
   "building":
      {  
         "id":146,
         "name":"Free Pizza",
      }  
}
```
