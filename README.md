# A pathway for creating data schemas

Schemas are a way to document your data and help make it more FAIR (Findable, Accessible, Interoperable, Reusable). Creating a schema is a process of continuous improvement. You don't need to create the most perfect and complete schema at the beginning. Instead, follow this pathway to gradual improvement where each step produces something usable for researchers.

[Feedback for creating a schema can be done in this Form](https://forms.office.com/Pages/ResponsePage.aspx?id=K6Fivq0soUml-oX08xVqfcxKJkze2nVHnEbvp9MCrIhUMjY3R0tTUDRTTU42RlBXMlAzRzdTSlo3RiQlQCN0PWcu).

# 1. Introduction to the rationale
<iframe width="560" height="315" src="https://www.youtube.com/embed/s4F1kEYeVEc" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

# 2. What is a schema

[Learn what a schema is](what_is_a_schema.md) and how it can apply to your research.

# 3. Write your first schema in Excel

[Following these instructions](create_first_schema.md) you will download the schema template (an Excel file), and based on the dataset you are describing you will enter in minimal schema information in this first iteration.

## What can you do with this schema?
* With this Excel document that you create you can store it beside (but separate from) your dataset. 
* You can share the Excel schema file when you share data.
* If your lab or collaborators use similar data you can collaborate together to define and write a schema and save it in a shared folder.
* IF you are a lab manager or leader you can request or require your students to use standard lab schemas in their research.
* You can use this Excel schema and convert it into a machine-readable format (OCA). Once you have a machine-readable schema, there are many more tools you can use and build to help you work with data.

This first Excel schema will meet a lot of user needs, but how can you be sure you are all using the *same* version? This is something that is addressed with the OCA schema standard and the use of SAID identifiers.

# 4. What is the Semantic Engine

Read our [introduction to schemas and the Semantic Engine](semantic_engine.md).

# 5. Create an OCA schema from your Excel schema

Using the Excel schema that you created when you wrote your first schema, you can [use the OCA parser to generate the OCA Schema Bundle](parse_OCA_schema.md).

Your Excel schema is still a human readable version of the schema, but the OCA Schema Bundle is a machine actionable version of your schema and includes special SAID identifiers helpful for schema versioning and referencing.

## What can you do with OCA

[What can you do with OCA](what_can_you_do_with_OCA.md), both current and future possibilities.

# 6. Learn about SAID identifiers

Read about [Identifiers and SAID identifiers](identifiers_and_saids.md), how they relate to the OCA schema, and how they are unique digital fingerprints of your schemas.

# 7. Deposit your schema in a repository

Read our advice and instructions on multiple ways to [deposit and/or publish your schema](deposit_schema.md) for archiving and public reference.

You can deposit your schema together with your data, or you can put it separately in a repository.

Be sure to deposit both the Excel Template that you created and the OCA schema bundle. The Excel Template will eventually be depreciated as we continue to build the Semantic Engine, but for now it is the best human-readable version of the schema.

# 8. Reference your schema in your documentation

# 9. Create a data entry sheet in Excel

# 10. Add drop down menu choices

You may want to create a schema that only allows data entries from a select list that you define. For example, you may want to limit gender choices to a few and you don't want some entries to say 'M' and other entries 'male' and other entries 'masculine' etc. This would make your analysis more difficult, especially if you are creating a data schema for use by other researchers. The solution is to [create custom dropdown lists in your schema](drop_down_list_instructions.md).

When you create a 'data entry' sheet in Excel using your OCA schema, it will automatically create the necessary dropdown lists which will simplify your data entry.

# 11. Add format and data validation 


