# SIMS API

## Get Incidents

### Request uses Basic Authorization based on API token provided, different filters e.g., countries, time period, incident type and others.

`GET /api/incident?country_id[]=2&amp;search_from=2017-07-22&amp;search_to=2017-07-22&amp;fields=Incident.id,Incident.remarks,Incident.latitude,Incident.longitude,Country.name,Type.name,Type.id,Incident.date HTTP/1.1
Host: simsplatform.com
Authorization: Basic <INSERT TOKEN KEY HERE>
Cache-Control: no-cache
Postman-Token: fc147580-2b6f-1cdc-d3e0-61cbe9219af0`

### Response is returned in JSON format. Fields returned depend on requested fields e.g., "fields=Incident.id,Incident.remarks,Incident.latitude,Incident.longitude,Country.name,Type.name,Type.id,Incident.date"

`{
    "message": "",
    "data": {
        "total": 46,
        "results": [
            {
                "id": "289840",
                "remarks": "3 robbers stole 10 million IQD from a civilian along al-Mutheef Street in Ameria, Baghdad on Saturday.",
                "latitude": "33.29883400",
                "longitude": "44.28890200",
                "date": "2017-07-22",
                "country_name": "Iraq",
                "type_name": "type_robbery",
                "type_id": "7",
                "mgrs": "38S MB 33796 84642",
                "weight": 1
            },
            {
                "id": "287651",
                "remarks": "An explosion from an unknown origin injured a civilian in Khalidiyah on Saturday.",
                "latitude": "33.41295900",
                "longitude": "43.45445200",
                "date": "2017-07-22",
                "country_name": "Iraq",
                "type_name": "type_ied",
                "type_id": "5",
                "mgrs": "38S LB 56291 98137",
                "weight": 1
            },
            {
                "id": "287539",
                "remarks": "Security forces arrested the ISIS Minister of Agriculture in west Mosul on Saturday.",
                "latitude": "36.33587000",
                "longitude": "43.10283700",
                "date": "2017-07-22",
                "country_name": "Iraq",
                "type_name": "type_arrest",
                "type_id": "29",
                "mgrs": "38S LF 29732 22873",
                "weight": 1
            },
            {
                "id": "287469",
                "remarks": "The Nineveh Plains Protection Units, a Christian led and Sunni dominated group, clashed with Shia PMU militia Kataib Sayyid al Shuhada on the outskirts of west Mosul on Saturday, when the Shia group attempted to enter Mosul. Shia militias have largely been kept outside of the city in fear of retribution against the local Sunni population. ",
                "latitude": "36.32419800",
                "longitude": "43.02246100",
                "date": "2017-07-22",
                "country_name": "Iraq",
                "type_name": "type_armed_clashes",
                "type_id": "3",
                "mgrs": "38S LF 22491 21723",
                "weight": 1
            },
            ...
            {
                "id": "286905",
                "remarks": "ISIS militants infiltrated the al Fadiliya village area north of Jarf Sakhar on Saturday morning, ambushing and killing 2 PMU soldiers during an exchange of gunfire. ",
                "latitude": "33.01784400",
                "longitude": "44.17087600",
                "date": "2017-07-22",
                "country_name": "Iraq",
                "type_name": "type_armed_clashes",
                "type_id": "3",
                "mgrs": "38S MB 22561 53570",
                "weight": 1
            },
            {
                "id": "286902",
                "remarks": "3 ISIS militants placed an IED near the home of a officer belonging to the Sunni tribal PMU forces in the Saridiya village, 10km west of Hit on Saturday, no injuries reported. Local security forces chased away the militants, wounding 1 during the process. ",
                "latitude": "33.64993800",
                "longitude": "42.63244600",
                "date": "2017-07-22",
                "country_name": "Iraq",
                "type_name": "type_ied",
                "type_id": "5",
                "mgrs": "38S KC 80444 25857",
                "weight": 1
            }
        ]
    },
    "total": 52
}`

# SicuroTrack API

## Get Incidents

### Request uses Basic Authorization based on username and password provided as well as an App-Key

`GET /api/1.0/pois HTTP/1.1
Host: www.sicurotrack.com
Authorization: Basic <INSERT BASE 64-ENCODED username and password>
App-Key: <INSERT APP KEY HERE>
Cache-Control: no-cache
Postman-Token: 0335c45a-63bf-00ec-bc05-24395c7da66d
`

### Response is returned in JSON format. Fields returned are shown below

`{
    "total": 930,
    "pois": [
        {
            "id": 880720892554932224,
            "icon": {
                "id": 0,
                "url": "http://localhost:8080/Images/Iconos/POI/000.png"
            },
            "label": "label test",
            "description": "description test",
            "coordinate": {
                "lat": 40.639503,
                "lng": -4.857809
            },
            "created": 1498815198,
            "lastmodified": 1498815198
        },
        {
            "id": 880721058288656384,
            "icon": {
                "id": 0,
                "url": "http://localhost:8080/Images/Iconos/POI/000.png"
            },
            "label": "label test 2",
            "description": "description test",
            "coordinate": {
                "lat": 40.639503,
                "lng": -4.857809
            },
            "created": 1498815237,
            "lastmodified": 1498815237
        },
        {
            "id": 880721090656104448,
            "icon": {
                "id": 1,
                "url": "http://localhost:8080/Images/Iconos/POI/001.png"
            },
            "label": "label test 3",
            "description": "description test",
            "coordinate": {
                "lat": 40.639503,
                "lng": -4.857809
            },
            "created": 1498815245,
            "lastmodified": 1498815245
        },
        {
            "id": 880721216799797248,
            "icon": {
                "id": 1,
                "url": "http://localhost:8080/Images/Iconos/POI/001.png"
            },
            "label": "label test 5",
            "description": "description test",
            "coordinate": {
                "lat": 40.639503,
                "lng": -4.857809
            },
            "created": 1498815275,
            "lastmodified": 1498815275
        },
        ...
        {
           "id": 881074107473477632,
           "icon": {
               "id": 189,
               "url": "http://localhost:8080/Images/Iconos/POI/189.png"
           },
           "label": "2017-06-30 |  ARREST - ISF arrested a wanted crimi",
           "description": "ISF arrested a wanted criminal on charges of premeditated murder in the Ameria area of west Baghdad on Friday. ",
           "coordinate": {
               "lat": 33.315661,
               "lng": 44.341121
           },
           "created": 1498899411,
           "lastmodified": 1498899411
       }
   ]
}`

## Create Incidents

### Request uses Basic Authorization based on username and password provided as well as an App-Key. A POST request with POI data in body is sent

`POST /api/1.0/pois HTTP/1.1
Host: www.sicurotrack.com
Authorization: Basic <INSERT BASE 64-ENCODED username and password>
App-Key: <INSERT APP KEY HERE>
Content-Type: application/x-www-form-urlencoded
Cache-Control: no-cache
Postman-Token: 58d055c1-fb02-74b4-068d-f45aac92d5a1

iconid=46&label=RegroupPOI&description=RegroupPOI&coordinate=40.639503%2C-4.857809
`

### Response is returned in JSON format. Fields returned depend on requested fields e.g., "fields=Incident.id,Incident.remarks,Incident.latitude,Incident.longitude,Country.name,Type.name,Type.id,Incident.date"

`{
    "poi": {
        "id": 899280338335875072,
        "icon": {
            "id": 46,
            "url": "http://localhost:8080/Images/Iconos/POI/046.png"
        },
        "label": "Regroupas",
        "description": "Regroupasd",
        "coordinate": {
            "lat": 40.639503,
            "lng": -4.857809
        },
        "created": 1503240115,
        "lastmodified": 1503240115
    }
}`
