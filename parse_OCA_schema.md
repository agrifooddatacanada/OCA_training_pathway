# Convert from Excel to OCA

The Excel template with the schema information can be parsed into a machine actionable, standard representation of the schema called [Overlays Capture Architecture (OCA)](https://oca.colossi.network/).

[XLS to OCA Converter](https://browser.oca.argo.colossi.network/#/) is currently hosted at Human Colossus Foundation (HCF) in the first phase of development. The Semantic Engine's template is derived from the template found hosted by HCF.

Upload the Excel document into the [parser to create the OCA Bundle](https://browser.oca.argo.colossi.network/#/).

![OCA converter](/pictures/chicken_ready_for_OCA_conversion.PNG)

If there are no problems with the template file that you have created, you will have a successful conversion and you can now download the OCA Schema Bundle using the link.

![download a successful OCA converted file](/pictures/chicken_OCA_download.PNG)

The OCA Bundle contains the Capture Base and associated Overlays as files bundled into an archival (.zip) format.

You can open the archive and view the JSON code of the schema. The "meta.json" file lists is the most human readable and lists all Overlays and Capture Base including their SAID identifiers. The SAID identifiers for Overlays, Capture Base and the entire OCA Bundle are also their filenames. 

![meta.json file contents](/pictures/chicken_OCA_meta.PNG)

After you have created a OCA schema bundle from an Excel template we recommend that you copy the schema bundle SAID identifier onto the 'README' sheet of your Excel template. The schema bundle SAID is the filename of the .zip file.

![OCA Bundle file name](/pictures/chicken_OCA_bundle.PNG)

Copy the file name SAID to your template schema.

![adding the OCA SAID identifier back into the template schema](/pictures/chicken_Excel_with_OCA_SAID.PNG)

# More information about OCA

## OCA is expressed in JSON
Overlays Capture Architecture is a machine-readable way to encode a schema expressed in the JSON scripting language. You can view the JSON file contents using a text editor such as Notepad in Windows but since JSON files do not usually contain line breaks it is easier to read using a [JSON viewer](https://jsonformatter.curiousconcept.com/).

Writing a schema in JSON is not very human-friendly, instead we will fill out the schema information in a template Excel spreadsheet. Then we upload this Excel sheet into the semantic engine OCA schema parser, and it will generate the OCA schema bundle. In the future as we develop the Semantic Engine, we can create easier ways to generate these OCA schemas, but in phase one of development we use the Excel template.

## Advantages of OCA
The advantage of OCA schemas is that they are modular. You can start with a very simple design, and because of the OCA layered architecture you can add more functionality to the schema later. The simplest OCA schema has a Capture Base (CB) which defines the basic structure of the data, and some additional overlays (OL) that help the user understand the data. OCA schemas are also shareable and machine-readable. You can publish your OCA schema with an identifier and others can reference and extend your work.
