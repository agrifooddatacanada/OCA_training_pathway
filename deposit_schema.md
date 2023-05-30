# Saving, Depositing and/or Publishing your Schema

You will want to ensure your schema is available for reference and/or reuse. Here are several options:
* You can save your schema together with your data
* You can deposit your schema together with a dataset when you put your dataset in a repository
* You can publish your schema separately, where it is given an identifier you can use to associate the schema with your datasets.

## Save your schema with your data

The first, and easiest way to save your schema for future reference is together with the dataset that it is associated with it. This is most useful for schemas that are very specific to your dataset and where you haven't created the schema with an eye towards reuse.

We suggest that you save your schema both as the Excel template and the OCA bundle. The OCA bundle is a machine-readable version and is a published standard. This should be the most future-proof version of your schema. The Excel Template is a human readable version and also useful to save with your data. As we develop the Semantic Engine we will depreciate the Excel Template and use other tools to generate OCA schemas.

## Deposit your schema separately in a repository

Schemas can be written to be useful for multiple datasets. A well written schema can be very useful for a research community because it can make it easier to share and understand data, and save the work of documentation.

You can deposit a schema separately in the University of Guelph's Borealis repository and this will give your schema a citable DOI. You can share and publish this DOI and reference it when you publish your data. Other researchers can reference your schema for their own data collection and publication.

Obtaining a DOI via Borealis:
1. [Log in to Borealis](https://borealisdata.ca/loginpage.xhtml), A Canadian Dataverse Repository using your U of G username and password.
2. Request permission to deposit in the U of G Research Data Repositories at [lib.research@uoguelph.ca](mailto:lib.research@uoguelph.ca).
3. Once access has been granted, navigate to the Agri-environmental Research Data Repository - [Agri-food Data Canada – Schemas  collection](https://borealisdata.ca/dataverse/adcSchema/).
4. Click on ‘Add Data’ button and select ‘New Dataset’ from the drop-down menu.
5. In the Dataset Template  section, make sure that ‘ADC Schema’ is selected from the drop-down menu.
6. In the Citation Metadata section, complete the required information (e.g., title, author, contact, description, keywords, depositor name).
    * Include the SAID of your schema bundle (the schema bundle SAID is the name of your .zip file without the .zip ending) in your title.
    * ![SAID identifier of the schema bundle](/pictures/chicken_OCA_bundle.PNG)
8. Prepare your OCA Schema Bundle by 'zipping' the \*.zip file, That is, create a zip archive of the original zip archive. The OCA Schema Bundle should now be 'double-zipped'.
    * This step is necessary because Borealis automatically unzips zipped archives and the OCA Schema Bundle must be in zipped format.
9. Under the Files section, drag and drop your OCA Schema Bundle in (\*.zip) format and the schema template file in MS Excel (\*.xlsx) format. 
    * Note that, depending on the structure of the MS Excel file, the repository software may convert the file to tabular (\*.tab) format upon upload. If this occurs, Library staff will revert the file back to .xlsx format when they review the dataset submission. 
10. Click Save Dataset. 
    * After saving the dataset, a DOI is created and reserved for the record.
11. Edit the draft record (e.g., descriptive information (metadata) or files) as required.
12. Click on the ‘Publish Dataset’ button and select ‘Submit for Review’.
13. Repository staff (at the Library) will review and publish the record.
    * Upon publication, the DOI is resolved and becomes a working link. 

For reference: Research & Scholarship, 2020, "How to deposit research data in the Agri-environmental Research Data Repository or the University of Guelph Research Data Repository", https://doi.org/10.5683/SP2/CPHFGA, Borealis

### Versioning

For **minor updates** (like correcting typos) we recommend that you use the replacement feature of the Repository. 
* Use the Replace function. This replaces the file in the record and versions the record.
* Previous versions of the file are still accessible using the Versions tab in the record.
* Remember to change the SAID identifier which should be included in your title.

For **major updates** we recommend that you create another DOI and deposit the updated schema there. Add the citation (including DOI and SAID) to the original version of the schema into the ‘Related Datasets’ field in the record metadata.

## OCA Repository

Agri-food Data Canada, together with the Human Colossus Foundation is currently developing a specialized repository for OCA Schema creation.
