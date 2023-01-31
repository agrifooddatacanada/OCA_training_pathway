## Limiting data entry to a choice from a list (i.e. drop-down menu)
You might have a dataset where one of the columns can only be one of a few items. For example, you might have three sampling locations (Farm A, Farm B, Farm C) and you want to make sure the names entered are always the same ('Farm A', and not 'A', or 'FarmA' or 'FarmZ' by mistake).

The way you limit the choices to only a few is via paired overlays: 'Entry Code' and language specific tab 'Entry'.

The reason these overlays are paired is because the OCA schema lets users create different language drop-down menus (via 'Entry') that all record the same entry code 'Entry Code' for the data.

To limit data input to only a select number of choices use the following:

1. Attribute Type: use [text] or [numeric] for the Attribute Type (for single selection, for multiple selection use array[text] or array[numeric])
3. Entry Code: write short names or numbers coding for the items in the list (separated by the pipe &#124; symbol)
4. In each language tab for Entry give more human-readable labels matching each Entry Code to a language specific label

>Example 1: to limit gender entry to one of three choices
>1. Attribute Type: [text] 
>3. Entry codes: M&#124;F&#124;X 
>4. In the language tab for Entry: “M:Male&#124;F:Female&#124;X:Other” for English and “M:Masculin&#124;F:Féminin&#124;X:Autre” for French

>Example 2: to limit bee types to only two choices, with a code (501 or 527) for the actual data, but french or english names available for the data entry.
>1. Attribute Type: [Numeric]
>3. Entry codes: 501&#124;527
>4. In the language tab for Entry: "501:Carniolan honey bee&#124;527:Russian honey bee" for English and "501:Abeille de Carniole&#124;527:Abeille russe" for French
