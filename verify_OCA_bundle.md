# Verifying an OCA Bundle

Before the first use of an [OCA Bundle](/parse_OCA_schema.md) after modification, it should be checked for errors such as incomplete or mismatched overlays. This avoids the misuse of accessing and analyzing data from corrupted OCA Bundles.

A function of the [OCA Browser](https://browser.oca.argo.colossi.network/#/), currently hosted at the Human Colossus Foundation (HCF), can perform an integrity check of the OCA Bundle and provide information about any problems identified. Upload the OCA Bundle archive (.zip) file to the [Validate Tab](https://browser.oca.argo.colossi.network/#/validate).

![OCA validate function](/pictures/validate_upload.png)

If the integrity check passes, you will receive a Passed message with a brief overview of the overlays and JSON file information.

![OCA Bundle passed integrity check](/pictures/validate_passed.png)

Otherwise, you will receive an error message. Common issues include missing files...

![OCA Bundle failed with missing files](/pictures/validate_missing_file.png)

...or mismatched [SAIDs](/identifiers_and_saids.md). In the case below, the SAID of the capture base in an overlay file does not match the capture base JSON file.

![OCA Bundle failed with mismatched SAIDs](/pictures/validate_mismatched_said.png)

Also, if you manually edited any of the JSON files, the hash value of the file contents would change. Then it will not match the stored [SAID digest](/identifiers_and_saids.md), leading to a malformed SAID problem.

![OCA Bundle failed with malformed SAIDs](/pictures/validate_malformed_said.png)

If the integrity check fails, you may want to re-download/re-generate the OCA Bundle or restore any manual modifications to the JSON files. Normally any JSON file in an OCA Bundle should not be manually added, edited, or deleted.
