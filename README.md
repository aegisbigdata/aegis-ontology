# AEGIS Ontology and Vocabulary

This work is based on the following standards and specifications: 
* DCAT-AP - https://joinup.ec.europa.eu/solution/dcat-application-profile-data-portals-europe
* Frictionless Data - https://frictionlessdata.io/


## Classes


### Catalogue

__Hopsworks counterpart: Project__

|Property|DCAT-AP|User defined|Hopsworks|Mandatory|Info
|---|---|---|---|---|--|
|id|-|no|projectId|yes|integer|
|title|dct:title|yes|projectName|yes|string|
|description|dct:description|yes|description|yes|string|
|publisher|dct:publisher|yes|-|yes|object|
|datasets|dcat:dataset|no|-|yes|array|

- publisher
  - homepage (string)
  - name (string)


### Dataset

__Hopsworks counterpart: Data Set__

System provided

* dcatap:contact_point
* dcatap:distributions
* dcatap:publisher


* hops:folder


|Property|DCAT-AP|User defined|Hopsworks|Mandatory|Info
|---|---|---|---|---|--|
|id|-|no|id|yes|integer|
|title|dct:title|yes|name|yes|string|
|description|dct:description|yes|description|yes|string|
|contact_point|dcat:contactPoint|yes|-|no|object|
|keywords|dcat:keyword|yes|-|yes|array|
|publisher|dct:publisher|yes|-|no|object|
|theme|dcat:theme|yes|-|yes|enum|
|distributions|dcat:distribution|no|-|yes|array|

- contact_point
  - name (string)
  - email (string)
- publisher
  - homepage (string)
  - name (string)
- theme
  - see http://publications.europa.eu/mdr/resource/authority/data-theme/html/data-theme-eng.html



http://ids.semantic-interoperability.org/

### Distribution 

__Hopsworks counterpart: File__

|Property|DCAT-AP|User defined|Hopsworks|Mandatory|Info
|---|---|---|---|---|--|
|id|-|no|id|yes|integer|
|access_url|dcat:accessURL|no|path|yes|string|
|title|dct:title|yes|name|yes|string|
|description|dct:description|yes|-|yes|string|
|format|dct:format|yes|-|yes|string|
|licence|dct:licence|yes|-|yes|enum|
|pricing_scheme|-|yes|-|no|enum

- licence
  - https://www.europeandataportal.eu/en/content/show-license
- pricing_scheme
  - Free, PAYG, Subscription

## URI-Scheme

### Resources

http://www.aegis-bigdata.eu/md/dataset/{dataset_name}

http://www.aegis-bigdata.eu/md/dataset/{dataset_name}/distribution/{distribution_name}

http://www.aegis-bigdata.eu/md/dataset/{dataset_name}/distribution/{distribution_name}/schema

http://www.aegis-bigdata.eu/md/catalog/{catalog_name}

### Vocabulary

http://www.aegis-bigdata.eu/md/def

### Graphs

http://www.aegis-bigdata.eu/md/graphs/dataset/{dataset_name}


