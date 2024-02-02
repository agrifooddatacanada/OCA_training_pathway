# Convert from Excel to OCA

The Excel template with the schema information can be parsed into a machine actionable, standard representation of the schema called [Overlays Capture Architecture (OCA)](https://oca.colossi.network/).

Agri-food Data Canada hosts an [XLS to OCA Converter](http://parser.semanticengine.org) which converts the Excel Template to the OCA Bundle. Click on the arrow to expand the parsing function, then click "Try it out" and then upload your Excel Template for parsing.

![OCA converter](/pictures/parser_start.PNG)

After you have uploaded your Excel Template you will "Execute" the parsing and if there are no problems with the template file that you have created, you will have a successful conversion.

To download the schema bundle JSON file, click on the "Download" button to download your new schema bundle.

![download a successful OCA converted file](/pictures/parser_download.PNG)

The OCA Bundle contains the Capture Base and associated Overlays as a single JSON file.

You can open the file to view the contents including the SAID identifiers of the entire schema, the capture base and each overlay.

![meta.json file contents](/pictures/schemas_json_SAIDs.PNG)


# More information about OCA

## OCA is expressed in JSON
Overlays Capture Architecture is a machine-readable way to encode a schema expressed in the JSON scripting language. You can view the JSON file contents using a text editor such as Notepad in Windows but since JSON files do not usually contain line breaks it is easier to read using a [JSON viewer](https://jsonformatter.curiousconcept.com/).

Writing a schema in JSON is not very human-friendly, instead we will fill out the schema information in a template Excel spreadsheet. Then we upload this Excel sheet into the semantic engine OCA schema parser, and it will generate the OCA schema bundle..

## Advantages of OCA
The advantage of OCA schemas is that they are modular. You can start with a very simple design, and because of the OCA layered architecture you can add more functionality to the schema later. The simplest OCA schema has a Capture Base (CB) which defines the basic structure of the data, and some additional overlays (OL) that help the user understand the data. OCA schemas are also shareable and machine-readable. You can publish your OCA schema with an identifier and others can reference and extend your work.
