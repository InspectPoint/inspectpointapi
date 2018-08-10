# Inspections API
Retrieve, create, and edit inspections

# LIST Inpsections
## HTTP Method
##### GET  /external/api/v1/inspections

## Example
```
 curl https://${tenant_subdomain}.inspectpoint.com/external/api/v1/inspections \
     -X GET \
     -H 'Content-Type: application/json' \
     -H 'Api-Key: API_KEY_HERE' \
```

## Parameters
+ offset (defaults to 0)
+ limit  (defaults to 50)
+ building_id (filter by building)
+ technician_id (filter by technician)

## Example Response

+ Response 200 (application/json)
```json
{  
   "inspections":[  
     {
       "id": 1690,
       "scheduled_date": "2018-03-01T15:15:00.000-05:00",
       "status": "Scheduled",
       "frequency": "monthly",
       "reference_number": "236789",
       "building": {
         "id": 1,
         "name": "District 9 Warehouse"
       },
       "technician": {
         "id": 1,
         "name": "Drew Smith"
       }
     },
     {
       "id": 1800,
       "scheduled_date": "2018-03-29T15:15:00.000-05:00",
       "status": "Scheduled",
       "frequency": "annual",
       "reference_number": "54321",
       "building": {
         "id": 10,
         "name": "Innovation Garage"
       },
       "technician": {
         "id": 1,
         "name": "Drew Smith"
       }
     }
   ]
}
```
# INSPECTION DETAIL
## HTTP Method
##### GET  /external/api/v1/inspections/id

## Example
```
 curl https://${tenant_subdomain}.inspectpoint.com/external/api/v1/inspections/${inspection_id} \
     -X GET \
     -H 'Content-Type: application/json' \
     -H 'Api-Key: API_KEY_HERE' \
```

## Example Response

+ Response 200 (application/json)
```json
{  
   "inspection":
   {
     "id": 1690,
     "scheduled_date": "2018-03-01T15:15:00.000-05:00",
     "status": "Scheduled",
     "frequency": "monthly",
     "reference_number": "236789",
     "building": {
       "id": 1,
       "name": "District 9 Warehouse"
     },
     "technician": {
       "id": 1,
       "name": "Drew Smith"
     }
   }
}
```

# CREATE INSPECTION
## HTTP Method
##### PUT  /external/api/v1/inspections

## Example
```
 curl https://${tenant_subdomain}.inspectpoint.com/external/api/v1/inspections\
     -X GET \
     -H 'Content-Type: application/json' \
     -H 'Api-Key: API_KEY_HERE' \
     -d
```

## Request Attributes

Parameter Name | Required | Data Type
-------------- | -------------- | --------------
scheduled_date | Required | Datetime
building_id | Required | Integer
technician_id | Required | Integer
frequency | Required | Enum
status | Required | Enum
reference_number | Required | String

## Example Response

+ Response 200 (application/json)
```json
{  
   "inspection":
     {
       "id": 1690,
       "scheduled_date": "2018-03-01T15:15:00.000-05:00",
       "status": "Scheduled",
       "frequency": "monthly",
       "reference_number": "236789",
       "building": {
         "id": 1,
         "name": "District 9 Warehouse"
       },
       "technician": {
         "id": 1,
         "name": "Drew Smith"
       }
     }  
}
```

# UPDATE INSPECTION
## HTTP Method
##### POST  /external/api/v1/inspections/id

## Example
```
 curl https://${tenant_subdomain}.inspectpoint.com/external/api/v1/inspections/${inspection_id} \
     -X GET \
     -H 'Content-Type: application/json' \
     -H 'Api-Key: API_KEY_HERE' \
     -d
```

## Request Attributes
Parameter Name | Required | Data Type
-------------- | -------------- | --------------
scheduled_date | Required | Datetime
building_id | Required | Integer
technician_id | Required | Integer
frequency | Required | Enum
status | Required | Enum
reference_number | Required | String

## Example Response

+ Response 200 (application/json)
```json
{  
   "inspection":
     {
       "id": 1690,
       "scheduled_date": "2018-03-01T15:15:00.000-05:00",
       "status": "Scheduled",
       "frequency": "monthly",
       "reference_number": "236789",
       "building": {
         "id": 1,
         "name": "District 9 Warehouse"
       },
       "technician": {
         "id": 1,
         "name": "Drew Smith"
       }
     }
}
```
