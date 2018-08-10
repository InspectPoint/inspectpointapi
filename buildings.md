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
         "id": 16,
         "name": "Advanced Tire Warehouse",
         "zip": "12657",
         "address1": "5 Tire Way",
         "address2": "",
         "city": "Tiretown",
         "state": "NY",
         "notes": "park in back. enter through loading dock",
         "number_of_floors": null,
         "building_number": "54321",
         "latitude": 40.653947,
         "longitude": -73.576772,
         "site_identification": "",
         "monitoring_entity_contact_name": "",
         "monitoring_entity_telephone": "",
         "monitoring_entity_ref_no": "",
         "monitoring_entity_type_transmission": ""
     },
     {  
         "id":121,
         "name": "Troy Innovation Garage",
         "zip": "12180",
         "address1": "24 Fake ST",
         "address2": "",
         "city": "Troy",
         "state": "NY",
         "notes": "Access code 12345",
         "number_of_floors": null,
         "building_number": "12345",
         "latitude": 40.653947,
         "longitude": -73.576772,
         "site_identification": "",
         "monitoring_entity_contact_name": "",
         "monitoring_entity_telephone": "",
         "monitoring_entity_ref_no": "",
         "monitoring_entity_type_transmission": ""        
    }
   ]
}
```
# BUILDING DETAIL
## HTTP Method
##### GET  /external/api/v1/buildings/id

## Example
```
 curl https://${tenant_subdomain}.inspectpoint.com/external/api/v1/buildings/${building_id} \
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
       "id":121,
       "name": "Troy Innovation Garage",
       "zip": "12180",
       "address1": "24 Fake ST",
       "address2": "",
       "city": "Troy",
       "state": "NY",
       "notes": "Access code 12345",
       "number_of_floors": null,
       "building_number": "12345",
       "latitude": 40.653947,
       "longitude": -73.576772,
       "site_identification": "",
       "monitoring_entity_contact_name": "",
       "monitoring_entity_telephone": "",
       "monitoring_entity_ref_no": "",
       "monitoring_entity_type_transmission": ""        
  }  
}
```

# CREATE BUILDING
## HTTP Method
##### PUT  /external/api/v1/buildings

## Example
```
 curl https://${tenant_subdomain}.inspectpoint.com/external/api/v1/buildings\
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
number_of_floors | Required | Integer
travel_time_minutes | Required | Integer
reference_number | Required | String
state | Required | String
zip | Required | String
notes | Required | String
billing_address1 | Required | String
billing_address2 | Required | String
billing_city | Required | String
billing_state | Required | String
billing_zip | Required | String
contract_start_date | Required | Date
contract_expiration_date | Required | Date
monitoring_entity_contact_name | Required | String
monitoring_entity_telephone | Required | String
monitoring_entity_ref_no | Required | String
monitoring_entity_type_transmission | Required | String
building_number | Required | String
site_identification | Required | String
contract_type | Required | String
internal_office_notes | Required | String
sales_person | Required | String
building_number | Required | String


## Example Response

+ Response 200 (application/json)
```json
{  
   "building":
     {  
         "id":121,
         "name": "Troy Innovation Garage",
         "zip": "12180",
         "address1": "24 Fake ST",
         "address2": "",
         "city": "Troy",
         "state": "NY",
         "notes": "Access code 12345",
         "number_of_floors": null,
         "building_number": "12345",
         "latitude": 40.653947,
         "longitude": -73.576772,
         "site_identification": "",
         "monitoring_entity_contact_name": "",
         "monitoring_entity_telephone": "",
         "monitoring_entity_ref_no": "",
         "monitoring_entity_type_transmission": ""        
    }  
}
```

# UPDATE BUILDING
## HTTP Method
##### POST  /external/api/v1/buildings/id

## Example
```
 curl https://${tenant_subdomain}.inspectpoint.com/external/api/v1/buildings/${building_id} \
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
number_of_floors | Required | Integer
travel_time_minutes | Required | Integer
reference_number | Required | String
state | Required | String
zip | Required | String
notes | Required | String
billing_address1 | Required | String
billing_address2 | Required | String
billing_city | Required | String
billing_state | Required | String
billing_zip | Required | String
contract_start_date | Required | Date
contract_expiration_date | Required | Date
monitoring_entity_contact_name | Required | String
monitoring_entity_telephone | Required | String
monitoring_entity_ref_no | Required | String
monitoring_entity_type_transmission | Required | String
building_number | Required | String
site_identification | Required | String
contract_type | Required | String
internal_office_notes | Required | String
sales_person | Required | String


## Example Response

+ Response 200 (application/json)
```json
{  
   "building":
       {  
           "id":121,
           "name": "Troy Innovation Garage",
           "zip": "12180",
           "address1": "24 Fake ST",
           "address2": "",
           "city": "Troy",
           "state": "NY",
           "notes": "Access code 12345",
           "number_of_floors": null,
           "building_number": "12345",
           "latitude": 40.653947,
           "longitude": -73.576772,
           "site_identification": "",
           "monitoring_entity_contact_name": "",
           "monitoring_entity_telephone": "",
           "monitoring_entity_ref_no": "",
           "monitoring_entity_type_transmission": ""        
      }  
}
```
