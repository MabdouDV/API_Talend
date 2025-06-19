---
# NOTICE: Copyright 2025 Talend SA, Talend, Inc., and affiliates. All Rights Reserved. Customer’s use of the software contained herein is subject to the terms and conditions of the Agreement between Customer and Talend.
layout: "apiDefinition_1.1.0"
api-definition:
  specVersion: "4.1.0"
  info:
    name: "Customers API"
    version: "2.0.0"
    description: "Une API pour garder une trace de vos clients "
    license: {}
    contact: {}
  contract:
    baseUrls:
    - url: "https://76b9lv652cv10lb.eu.api-mocks.com"
      description: "This is your API mock server URL. When called, it will simulate the behavior of your API."
      isPublished: true
    mediaTypes:
    - "application/json"
    sections:
    - name: "Objets"
      elementOrder:
      - "#/contract/types/ecefa328-ed13-4070-beda-8f9bc7058a76"
      - "#/contract/types/3b8bf1a3-3ace-40d7-903e-0c26f373f8b8"
      - "#/contract/types/aef485ab-5acf-4df7-bfdf-7cdc6f3bf4cf"
    - name: "Opérations"
      elementOrder:
      - "#/contract/resources/54a38c99-5f9f-439d-9437-212f81c9d5fa"
      - "#/contract/resources/dcd00cf8-cf8f-43ef-9414-390367fc103d"
    - name: "Infos"
      elementOrder:
      - "#/contract/texts/7e1b7000-ff1d-468f-bd51-4b95268f3ac3"
    resources:
      "54a38c99-5f9f-439d-9437-212f81c9d5fa":
        path: "/clients"
        section: "#/contract/sections/623607b1-df7e-42aa-931b-6ca0d97514aa"
        operations:
          b07c7cb0-001a-40b6-a6a2-90e8ac70dd78:
            name: "Obtenir la liste des clients"
            method: "GET"
            description: "Chargement de la liste des clients"
            queryParameters:
            - name: "debut"
              type: "INTEGER"
              description: "La position de départ d'un groupe de clients à obtenir."
              required: true
            - name: "taillePage"
              type: "INTEGER"
              description: "Nombre de clients dans le groupe a obtenir"
              required: true
            responses:
              "4de2dddd-4a3b-422e-847f-cb673746a4ea":
                status: "200"
                bodies:
                - type: "#/contract/types/3b8bf1a3-3ace-40d7-903e-0c26f373f8b8"
                  examples:
                  - value: "{\n\t\"Client\": [{\n\t\t\t\"ID\": \"461140\",\n\t\t\t\"LAST_NAME\": \"Daniel\",\n\t\t\t\"NAME\": \"Thierry\",\n\t\t\t\"EMAIL\": \"tdaniel@test.decivision.com\",\n\t\t\t\"JOB_TITLE\": \"Consultant BI\",\n\t\t\t\"CREDITCARDNUMBER\": \"12345678-13-9876\",\n\t\t\t\"COMPANY\": \"DeciVision\",\n\t\t\t\"CITY\": \"Toulouse\",\n\t\t\t\"COUNTRY\": \"\"\n\t\t}, {\n\t\t\t\"ID\": \"380630\",\n\t\t\t\"LAST_NAME\": \"Legrand\",\n\t\t\t\"NAME\": \"Chantal\",\n\t\t\t\"EMAIL\": \"clegrand@test.decivision.com\",\n\t\t\t\"JOB_TITLE\": \"Consultant BI\",\n\t\t\t\"CREDITCARDNUMBER\": \"12345678-14-9876\",\n\t\t\t\"COMPANY\": \"DeciVision\",\n\t\t\t\"CITY\": \"Lyon\",\n\t\t\t\"COUNTRY\": \"\"\n\t\t}, {\n\t\t\t\"ID\": \"149072\",\n\t\t\t\"LAST_NAME\": \"Durant\",\n\t\t\t\"NAME\": \"Christelle\",\n\t\t\t\"EMAIL\": \"cdurant@test.decivision.com\",\n\t\t\t\"JOB_TITLE\": \"Consultant BI\",\n\t\t\t\"CREDITCARDNUMBER\": \"12345678-15-9876\",\n\t\t\t\"COMPANY\": \"DeciVision\",\n\t\t\t\"CITY\": \"Paris\",\n\t\t\t\"COUNTRY\": \"\"\n\t\t}, {\n\t\t\t\"ID\": \"678157\",\n\t\t\t\"LAST_NAME\": \"Petit\",\n\t\t\t\"NAME\": \"Patrick\",\n\t\t\t\"LAST_NAME\": \"Petit\",\n\t\t\t\"EMAIL\": \"ppetit@test.decivision.com\",\n\t\t\t\"JOB_TITLE\": \"Consultant BI\",\n\t\t\t\"CREDITCARDNUMBER\": \"12345678-16-9876\",\n\t\t\t\"COMPANY\": \"DeciVision\",\n\t\t\t\"CITY\": \"Bordeaux\",\n\t\t\t\"COUNTRY\": \"\"\n\t\t}\t]\n}\n"
          cfa37da1-cd45-42b8-8a3f-71cc5816aa49:
            name: "Creer un client"
            method: "POST"
            description: "Ajouter un nouveau client"
            bodies:
            - type: "#/contract/types/ecefa328-ed13-4070-beda-8f9bc7058a76"
              examples:
              - value: "{\n\t\"ID\": \"461145\",\n\t\"NAME\": \"Pierre\",\n\t\"LAST_NAME\": \"Dupont\",\n\t\"EMAIL\": \"pdupont@test.decivision.com\",\n\t\"JOB_TITLE\": \"Consultant BI\",\n\t\"CREDITCARDNUMBER\": \"12345678-12-9876\",\n\t\"COMPANY\": \"DeciVision\",\n\t\"CITY\": \"Toulouse\",\n\t\"COUNTRY\": \"FR\"\n}"
            responses:
              a3ae07eb-3c4b-4e7e-b41b-ccfc2db2d2e5:
                status: "201"
                description: "Statut 201"
                bodies:
                - type: "#/contract/types/ecefa328-ed13-4070-beda-8f9bc7058a76"
                  examples:
                  - value: "{\n\t\"ID\": \"461145\",\n\t\"NAME\": \"Pierre\",\n\t\"LAST_NAME\": \"Dupont\",\n\t\"EMAIL\": \"pdupont@test.decivision.com\",\n\t\"JOB_TITLE\": \"Consultant BI\",\n\t\"CREDITCARDNUMBER\": \"12345678-12-9876\",\n\t\"COMPANY\": \"DeciVision\",\n\t\"CITY\": \"Toulouse\",\n\t\"COUNTRY\": \"FR\"\n}"
              "0ab3e25b-e2e5-4678-91c1-a47a5fe1692e":
                status: "409"
                description: "409 - Conflct"
                bodies:
                - type: "#/contract/types/aef485ab-5acf-4df7-bfdf-7cdc6f3bf4cf"
                  examples:
                  - value: "{\n\t\"ID\": \"461145\",\n\t\"errorCode\": \"23000\",\n\t\"errorMessage\": \"Entrée '461145' dupliquée comme clé 'PRIMARY' - Line: 0\"\n}"
      dcd00cf8-cf8f-43ef-9414-390367fc103d:
        path: "/clients/{id}"
        section: "#/contract/sections/623607b1-df7e-42aa-931b-6ca0d97514aa"
        pathVariables:
        - name: "id"
          type: "STRING"
          required: true
        operations:
          "30a2e095-9e2d-460b-9989-e994959a42cf":
            name: "Supprimer un client"
            method: "DELETE"
            description: "Supprimer un client"
            responses:
              a3e230ed-6c6f-4667-85fa-39591f296517:
                status: "200"
                description: "Statut 200"
          e4156627-7d6e-44ce-8b78-7f179ce3a07e:
            name: "Mettre a jour un client"
            method: "PUT"
            description: "Maj client"
            bodies:
            - type: "#/contract/types/ecefa328-ed13-4070-beda-8f9bc7058a76"
              examples:
              - value: "{\n\t\"ID\": \"461145\",\n\t\"NAME\": \"Pierre\",\n\t\"LAST_NAME\": \"Dupont\",\n\t\"EMAIL\": \"pdupont@test.decivision.com\",\n\t\"JOB_TITLE\": \"Consultant BI\",\n\t\"CREDITCARDNUMBER\": \"12345678-12-9876\",\n\t\"COMPANY\": \"DeciVision\",\n\t\"CITY\": \"Toulouse\",\n\t\"COUNTRY\": \"FR\"\n}"
            responses:
              "71702ab4-4500-4537-b0c8-7b55e3009229":
                status: "200"
                description: "Statut 200"
                bodies:
                - type: "#/contract/types/ecefa328-ed13-4070-beda-8f9bc7058a76"
                  examples:
                  - value: "{\n\t\"ID\": \"461145\",\n\t\"NAME\": \"Pierre\",\n\t\"LAST_NAME\": \"Dupont\",\n\t\"EMAIL\": \"pdupont@test.decivision.com\",\n\t\"JOB_TITLE\": \"Consultant BI\",\n\t\"CREDITCARDNUMBER\": \"12345678-12-9876\",\n\t\"COMPANY\": \"DeciVision\",\n\t\"CITY\": \"Toulouse\",\n\t\"COUNTRY\": \"FR\"\n}"
    types:
      ecefa328-ed13-4070-beda-8f9bc7058a76:
        name: "Client"
        type: "OBJECT"
        section: "#/contract/sections/dcda5ee9-a90a-4ddb-b5a3-b13bfecc06e3"
        required: false
        properties:
        - name: "ID"
          type: "STRING"
          required: false
        - name: "NAME"
          type: "STRING"
          required: false
        - name: "LAST_NAME"
          type: "STRING"
          required: false
        - name: "EMAIL"
          type: "STRING"
          required: false
        - name: "JOB_TITLE"
          type: "STRING"
          required: false
        - name: "CREDITCARDNUMBER"
          type: "STRING"
          required: false
        - name: "COMPANY"
          type: "STRING"
          required: false
        - name: "CITY"
          type: "STRING"
          required: false
        - name: "COUNTRY"
          type: "STRING"
          required: false
        examples:
        - value: "{\n\t\"ID\": \"461145\",\n\t\"NAME\": \"Pierre\",\n\t\"LAST_NAME\": \"Dupont\",\n\t\"EMAIL\": \"pdupont@test.decivision.com\",\n\t\"JOB_TITLE\": \"Consultant BI\",\n\t\"CREDITCARDNUMBER\": \"12345678-12-9876\",\n\t\"COMPANY\": \"DeciVision\",\n\t\"CITY\": \"Toulouse\",\n\t\"COUNTRY\": \"FR\"\n}"
      "3b8bf1a3-3ace-40d7-903e-0c26f373f8b8":
        name: "Clients"
        type: "ARRAY"
        section: "#/contract/sections/dcda5ee9-a90a-4ddb-b5a3-b13bfecc06e3"
        items:
          type: "#/contract/types/ecefa328-ed13-4070-beda-8f9bc7058a76"
          required: false
      aef485ab-5acf-4df7-bfdf-7cdc6f3bf4cf:
        name: "Erreur"
        type: "OBJECT"
        section: "#/contract/sections/dcda5ee9-a90a-4ddb-b5a3-b13bfecc06e3"
        properties:
        - name: "ID"
          type: "STRING"
          required: true
        - name: "codeErreur"
          type: "INTEGER"
          required: false
          minimum: 400
          maximum: 599
        - name: "messageErreur"
          type: "STRING"
          required: false
    texts:
      "7e1b7000-ff1d-468f-bd51-4b95268f3ac3":
        title: "« API construit avec Talend API Designer"
        content: "API conçu avec Talend API Designer. L'implémentation de l'API Clients a été construite et déployée à l'aide de Talend Cloud"
        section: "#/contract/sections/81da8df4-35c0-422b-9f37-41b6cb8cfb10"
  components: {}
api-tryin: |-
  {
    "version" : 6,
    "entities" : [ {
      "entity" : {
        "type" : "Project",
        "name" : "Customers API 2.0.0",
        "description" : "Une API pour garder une trace de vos clients ",
        "importedFrom" : "178e1ac2-5251-4bdd-b719-62c4beda0c9c"
      },
      "children" : [ {
        "entity" : {
          "type" : "Service",
          "name" : "Objets"
        }
      }, {
        "entity" : {
          "type" : "Service",
          "name" : "Opérations"
        },
        "children" : [ {
          "entity" : {
            "type" : "Request",
            "id" : "b07c7cb0-001a-40b6-a6a2-90e8ac70dd78",
            "name" : "Obtenir la liste des clients",
            "description" : "Chargement de la liste des clients",
            "uri" : {
              "host" : "${\"BaseUrl\"}",
              "path" : "/clients",
              "query" : {
                "delimiter" : "&",
                "items" : [ {
                  "name" : "debut",
                  "value" : "",
                  "enabled" : true
                }, {
                  "name" : "taillePage",
                  "value" : "",
                  "enabled" : true
                } ]
              }
            },
            "method" : {
              "link" : "",
              "name" : "GET"
            },
            "headers" : [ {
              "enabled" : true,
              "name" : "Accept",
              "value" : "application/json"
            } ],
            "headersType" : "Form",
            "uriEditor" : true
          }
        }, {
          "entity" : {
            "type" : "Request",
            "id" : "cfa37da1-cd45-42b8-8a3f-71cc5816aa49",
            "name" : "Creer un client",
            "description" : "Ajouter un nouveau client",
            "uri" : {
              "host" : "${\"BaseUrl\"}",
              "path" : "/clients"
            },
            "method" : {
              "link" : "",
              "name" : "POST",
              "requestBody" : true
            },
            "headers" : [ {
              "enabled" : true,
              "name" : "Content-Type",
              "value" : "application/json"
            }, {
              "enabled" : true,
              "name" : "Accept",
              "value" : "application/json"
            } ],
            "headersType" : "Form",
            "body" : {
              "bodyType" : "Text",
              "textBody" : "{\n\t\"ID\": \"461145\",\n\t\"NAME\": \"Pierre\",\n\t\"LAST_NAME\": \"Dupont\",\n\t\"EMAIL\": \"pdupont@test.decivision.com\",\n\t\"JOB_TITLE\": \"Consultant BI\",\n\t\"CREDITCARDNUMBER\": \"12345678-12-9876\",\n\t\"COMPANY\": \"DeciVision\",\n\t\"CITY\": \"Toulouse\",\n\t\"COUNTRY\": \"FR\"\n}"
            }
          }
        }, {
          "entity" : {
            "type" : "Request",
            "id" : "30a2e095-9e2d-460b-9989-e994959a42cf",
            "name" : "Supprimer un client",
            "description" : "Supprimer un client",
            "uri" : {
              "host" : "${\"BaseUrl\"}",
              "path" : "/clients/{id}"
            },
            "method" : {
              "link" : "",
              "name" : "DELETE"
            },
            "headers" : [ ],
            "headersType" : "Form"
          }
        }, {
          "entity" : {
            "type" : "Request",
            "id" : "e4156627-7d6e-44ce-8b78-7f179ce3a07e",
            "name" : "Mettre a jour un client",
            "description" : "Maj client",
            "uri" : {
              "host" : "${\"BaseUrl\"}",
              "path" : "/clients/{id}"
            },
            "method" : {
              "link" : "",
              "name" : "PUT",
              "requestBody" : true
            },
            "headers" : [ {
              "enabled" : true,
              "name" : "Content-Type",
              "value" : "application/json"
            }, {
              "enabled" : true,
              "name" : "Accept",
              "value" : "application/json"
            } ],
            "headersType" : "Form",
            "body" : {
              "bodyType" : "Text",
              "textBody" : "{\n\t\"ID\": \"461145\",\n\t\"NAME\": \"Pierre\",\n\t\"LAST_NAME\": \"Dupont\",\n\t\"EMAIL\": \"pdupont@test.decivision.com\",\n\t\"JOB_TITLE\": \"Consultant BI\",\n\t\"CREDITCARDNUMBER\": \"12345678-12-9876\",\n\t\"COMPANY\": \"DeciVision\",\n\t\"CITY\": \"Toulouse\",\n\t\"COUNTRY\": \"FR\"\n}"
            }
          }
        } ]
      }, {
        "entity" : {
          "type" : "Service",
          "name" : "Infos"
        }
      } ]
    } ],
    "environments" : [ {
      "name" : "Customers API 2.0.0",
      "importedFrom" : {
        "projectId" : "178e1ac2-5251-4bdd-b719-62c4beda0c9c"
      },
      "variables" : {
        "75779f57-33ab-4e79-a7b6-12e1c39430d3" : {
          "name" : "BaseUrl",
          "value" : "https://76b9lv652cv10lb.eu.api-mocks.com",
          "enabled" : true,
          "private" : false
        }
      }
    } ]
  }
---
