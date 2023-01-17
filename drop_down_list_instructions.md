## Limiting data entry to a choice from a list (i.e. drop-down menu)
To limit data input to only a select number of choices (like in a drop-down menu) for an attribute use:

1. Attribute Type: use [text] or [numeric] for the Attribute Type (for single selection, for multiple selection use array[text] or array[numeric])
2. Format: the format for the entry code
3. Entry Code: write short names or numbers coding for the items in the list (separated by the pipe &#124; symbol)
4. In each language tab for Entry give more human-readable labels matching each Entry Code to a language specific label

>Example 1: to limit gender entry to one of three choices
>1. Attribute Type: [text] 
>2. Format: [A-Z]{1}
>3. Entry codes: M&#124;F&#124;X 
>4. In the language tab for Entry: “M:Male&#124;F:Female&#124;X:Other” for English and “M:Masculin&#124;F:Féminin&#124;X:Autre” for French

>Example 2: to limit bee types to only two choices
>1. Attribute Type: [Numeric]
>2. Format: [0-9]{3}
>3. Entry codes: 501&#124;527
>4. In the language tab for Entry: "501:Carniolan honey bee&#124;527:Russian honey bee" for English and "501:Abeille de Carniole&#124;527:Abeille russe" for French
