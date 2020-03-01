# Open API Koppeling Regie - Backoffice

Een open standaard om gegevensuitwisseling tussen regiesystemen en backofficeapplicaties mogelijk te maken. Vanuit gemeenten is er behoefte om gegevens tussen regie- en backofficeapplicaties uit te wisselen. Omdat hier geen standaard voor is vanuit VNG-Realisatie of het Zorginstituut hebben enkele leveranciers (ZorgNed, Solviteers Software) hier zelf het initiatief toe genomen.

Functionaliteit die met deze API mogelijk gemaakt wordt:
* Raadplegen aanvragen in de backoffice
  * Hiermee kan een klantbeeld samengesteld worden
  * De vraag naar de backoffice kan gefilterd worden op basis van _regeling_ en _maximale einddatum_ van het toegewezen product
* Opvragen van toewijzingen in de backoffice
* Opvragen details van een specifieke toewijzing

# Getting started

* cd into this folder
* run `docker-compose up` or `docker-compose up -d` if you want to run it in detached mode in the background
* open the API-docs (depending on the developer preferences) by browsing to either http://localhost:8020 (Swagger-ui) or http://localhost:8025 (Redoc)

Or view online:
* [Swagger formaat](https://petstore.swagger.io/?url=https://raw.githubusercontent.com/solviteers/koppeling-regie-backoffice/master/api-specification.yml)

# Folder Structure

    .                               # API specification (in OAS3), Git project root
    ├── headers                 # OAS3 header specifations
    ├── parameters              # OAS3 parameter specifations
    ├── paths                   # OAS3 path specifations
    ├── responses               # OAS3 response specifations
    ├── schemas                 # OAS3 schema specifations
    ├── security_schemes        # OAS3 security definitions
    ├── docker-compose.yml      # Instructions to run swagger-ui and swagger editor
    └── README.md               # Documentation on how to work with API specs
    └── ...

# How Open Api Specication 3.0 works

* [Official OpenAPI specification on github](https://github.com/OAI/OpenAPI-Specification)
* [Formatted docs based on the github repo](https://spec.openapis.org/oas/v3.0.2)
* [Swaggers take on OAS3 with examples (good place to get started)](https://swagger.io/docs/specification/about)
* [OAS3 recommandation by the Dutch government](https://www.forumstandaardisatie.nl/standaard/openapi-specification)

# API guidelines and principles

* The API-specification in itself should be descriptive enough to know how to use and interact with the API;
* Developers write code based on the API-specification, not the other way around. We don't generate documentation based on written code;
* API's are documented using Open Api Specification version 3 (OAS3) since this an open standerd AND because it is adopted as standard by the Dutch government;
* The API-specification describes the endpoints and the input and output of every resource;
* The API-specification describes how a call should be authenticated and where to get credentials or API-keys;
* The API-specification is always up to date with its code-branch and available through the API's base-url (i.e.: localhost:8080/api/v1);
* A proper API-specification contains enough technical detail to serve as a functional means of communication with developers;
