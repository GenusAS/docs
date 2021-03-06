---
title: Import and export JSON data in Genus Apps
description: Article describing how to configure a data mapping to transfer data between JSON and a data source
author: henrikmj
---

# Import and export JSON data

## The Data Mapping object

In order to import or export data on JSON format to and from different sources into a data source in Genus, an object called a Data Mapping is used. A Data Mapping is an object consisting of a template and a set of bindings to a data source that describes how data will be transferred to and from JSON.

## The Data Mapping Editor

The Data Mapping Editor us used to configure a Data Mapping by creating a template for a JSON document and create bindings to the data source. The main view displays the structure of the JSON data, with bindings to data sources indicated on objects and properties. 

The following example displays a structure which maps a set of Person objects to JSON:

    [
      { Person
        "FirstName" : Person.FirstName
        "LastName" : Person.LastName
      }
    ]


## Import data from JSON

In order to import data from JSON, create a template in the Data Mapping Editor that reflects the structure of the JSON data. It is possible to use an existing JSON string to generate the template, or use the commands available in the editor to build the structure.

In order to create new objects in the data source, create a binding to a JSON object in the template. If the JSON object is within an array, one object will be created in the data source for each JSON object. To save JSON values into fields in the data source, create a binding to the desired field. A binding is created by dragging the field onto the corresponding element in the template.

## Export data to JSON

_The contents of this article is under construction. We are sorry for the inconvenience._
