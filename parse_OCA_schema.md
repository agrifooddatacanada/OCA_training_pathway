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

After you have created a OCA schema bundle from an Excel template we recommend that you copy the schema bundle SAID identifier onto the 'README' sheet of your Excel template.

![adding the OCA SAID identifier back into the template schema](/pictures/chicken_Excel_with_OCA_SAID.PNG)
