# What to do with your OCA bundle

## View the contents of the bundle
You can view the contents of an Overlays Capture Architecture (OCA) bundle by opening the .zip file and viewing the included JSON files using a text editor such as Windows Notepad, but since JSON files do not usually contain line breaks it is easier to read using a [JSON viewer](https://jsonformatter.curiousconcept.com/).

## Archive the OCA bundle together with the associated data
The simplest thing you can do with your OCA schema is to save the bundle and Excel template with your data on a local or lab associated drive. This will help you or others understand your data when referenced later. When it comes time to submit data into a repository or journal you will be able to quickly and accurately describe the data using the requested format by looking at the OCA schema.

We recommend you record the [SAID](identifiers_and_saids.md) associated with the schema bundle with each dataset which will give you cryptographic verifiability about exactly what schema Capture Base and Overlays you were using with your data.

## Share the OCA bundle with collaborators
The OCA schema bundle (together with Excel template) can be shared with your collaborators. Sharing the schemas early in the collaboration means that it will be easier to harmonize the data during analysis. You can collectively improve the schema by updating the template together and creating new schema bundles.

You can confirm that you and your collaborators are using the same schemas by comparing in the [SAIDs](identifiers_and_saids.md) associated with each bundle or individual Capture Base or Overlay.

## Generate a DOI and publish the OCA schema bundle separately in a repository
[Deposit and/or publish your schema](deposit_schema.md) in the University of Guelph Borealis repository. This gives your schema a DOI (i.e. persistent identifier) that can be referenced in publications. Be sure to include the SAID of the schema bundle in the title of the schema.

## Publish the OCA schema bundle in an OCA specific repository
This is a feature that is currently under development at ADC and we are looking for feedback from researchers about requirements. We seek to create an OCA repository model, that can be federated across Canada so that other instutitions can host a schema repository to meet their user needs but remain connected with all other OCA repositories. 

An OCA specific respository will enable additional functionalities of the OCA schema such as creation of additional overlays by other authors and deeper search functionality.

An OCA repository will be compatible with depositing the schema in other locations as well because of the properties of the [SAIDs](identifiers_and_saids.md) (self-addressing identifiers). Any schema will have an identifier that is computationally calculated from the content. If the content changes in any small way, the identifier (the SAID) is completely different. If you find two schemas in two different locations but they have the same SAID you can be confident that they are identical.

## Generate a form from the OCA schema bundle
Currently [under development](https://browser.oca.argo.colossi.network/#/preview).

## Generate an Excel sheet for data entry based on the schema
Currently in development, when you create your OCA schema using the [XLS to OCA Converter](https://browser.oca.argo.colossi.network/#/) there is an checkbox option 
to "Generate Data Entry File". This will create an Excel file suitable for data entry which conforms to the schema that you uploaded.

This feature is under development and we are seeking feedback from researchers.

## Validate your data with an OCA schema bundle
With the creation of an OCA schema bundle, ADC will create the ability to validate a dataset according to the schema bundle specifications. For example, validation would check that dates are written in the way specified by the schema, or that there are no text values (like the letter O) instead of the number zero in a number field.

This feature is under development and we are seeking feedback from researchers.

# More information about OCA

## OCA is expressed in JSON
Overlays Capture Architecture is a machine-readable way to encode a schema expressed in the JSON scripting language. You can view the JSON file contents using a text editor such as Notepad in Windows but since JSON files do not usually contain line breaks it is easier to read using a [JSON viewer](https://jsonformatter.curiousconcept.com/).

Writing a schema in JSON is not very human-friendly, instead we will fill out the schema information in a template Excel spreadsheet. Then we upload this Excel sheet into the semantic engine OCA schema parser, and it will generate the OCA schema bundle. In the future as we develop the Semantic Engine, we can create easier ways to generate these OCA schemas, but in phase one of development we use the Excel template.

## Advantages of OCA
The advantage of OCA schemas is that they are modular. You can start with a very simple design, and because of the OCA layered architecture you can add more functionality to the schema later. The simplest OCA schema has a Capture Base (CB) which defines the basic structure of the data, and some additional overlays (OL) that help the user understand the data. OCA schemas are also shareable and machine-readable. You can publish your OCA schema with an identifier and others can reference and extend your work.
