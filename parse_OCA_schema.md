# Convert from Excel to OCA

The Excel template with the schema information can be parsed into a machine actionable, standard representation of the schema called [Overlays Capture Architecture (OCA)](https://oca.colossi.network/).

The [SemanticEngine.org](https://www.semanticengine.org) website is where you will find the [XLS to OCA Converter](https://www.semanticengine.org/#/develop) which converts the Excel Template to the OCA Bundle.

![OCA converter](/pictures/chicken_ready_for_OCA_conversion.PNG)

If there are no problems with the template file that you have created, you will have a successful conversion and you can now download the OCA Schema Bundle using the link.

![download a successful OCA converted file](/pictures/chicken_OCA_download.PNG)

The OCA Bundle contains the Capture Base and associated Overlays as files bundled into an archival (.zip) format.

You can open the archive and view the JSON code of the schema. The "meta.json" file lists is the most human readable and lists all Overlays and Capture Base including their SAID identifiers. 

![meta.json file contents](/pictures/chicken_OCA_meta.PNG)

After you have created a OCA schema bundle from an Excel template we recommend that you copy the root SAID identifier onto the 'README' sheet of your Excel template. The root SAID  is the SAID of the Capture Base. In the future it is better to use the SAID of the entire bundle but currently this is not available.

Note: the filename of the .zip bundle is a RANDOMLY GENERATED name. If you parse the same schema again you will get a different .zip filename. It looks like it should be a SAID but it is not. For OCA schemas, all SAIDs begin with 'E'.

![adding the OCA SAID identifier back into the template schema](/pictures/chicken_Excel_with_OCA_SAID.PNG)

# More information about OCA

## OCA is expressed in JSON
Overlays Capture Architecture is a machine-readable way to encode a schema expressed in the JSON scripting language. You can view the JSON file contents using a text editor such as Notepad in Windows but since JSON files do not usually contain line breaks it is easier to read using a [JSON viewer](https://jsonformatter.curiousconcept.com/) or in the JSON viewer when you [validate your schema bundle](https://www.semanticengine.org/#/validate).

Writing a schema in JSON is not very human-friendly, instead we will fill out the schema information in a template Excel spreadsheet. Then we upload this Excel sheet into the semantic engine OCA schema parser, and it will generate the OCA schema bundle. In the future as we develop the Semantic Engine, we can create easier ways to generate these OCA schemas, but in phase one of development we use the Excel template.

## Advantages of OCA
The advantage of OCA schemas is that they are modular. You can start with a very simple design, and because of the OCA layered architecture you can add more functionality to the schema later. The simplest OCA schema has a Capture Base (CB) which defines the basic structure of the data, and some additional overlays (OL) that help the user understand the data. OCA schemas are also shareable and machine-readable. You can publish your OCA schema with an identifier and others can reference and extend your work.
