# LocationAPI-Demo

LocationAPI project is for searching near by places using categories etc.
Also it will provide the service to mark the places in favorite list. 

## Prerequisites

Java 1.8

Maven

FourSquare API


## Installation

Use below command to compile & run the project.

#### To create artifact of project

mvn clean install

#### To run / start the project

java -Dapp.log.dir=c:\temp -Dclient_id={{FOURSQUARE_CLIENT_ID}} -Dclient_secret={{FOURSQUARE_CLIENT_SECRET}} -cp config -jar target\locationapidemo-1.0-SNAPSHOT.jar

VM argument "-Dapp.log.dir" is used to set log folder path.

Also add config folder in classpath using "-cp config" command.

Replace FourSquare client_id & client_secret properties with valid credentials provided by FourSquare.

## Usage
This application use to provide services to client so that client can easily search locations. It also provides basic filters to search different places all around the world.

#### Ex. 

HTTP Request (GET): http://localhost:8080/api/location?query=yewale&nearBy=pune&limit=1

HTTP Response :

{
    "places": [
        {
            "placeId": "5c74e490872f7d0039a394d3",
            "name": "Yewale Amrut-Tulya",
            "address": "[Pune 411037, Mahārāshtra, India]",
            "phoneNumber": null,
            "rating": null,
            "categories": [
                {
                    "id": "4bf58dd8d48988d16d941735",
                    "name": "Café",
                    "icon": {
                        "prefix": "https://ss3.4sqi.net/img/categories_v2/food/cafe_",
                        "sufix": null
                    },
                    "categories": null
                }
            ]
        }
    ]
}

Application will maintain favorite places list with respect to users.
User can fetch their favorite place details very easily.

Application is covered with Junit test cases so that all test cases are get executed during packaging the artifact.

## Configuration
Application configureation are maintain under config/application.properties file.
For example API client key, secret key, Database configuration details etc.
Application logging configuration is managed in log4j2.xml file

## API 
API documentation will be accessible using below link.

http://localhost:8080/swagger-ui.html

```
## Contributing

## License
