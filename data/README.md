## Data Dictionary

### task_1.csv

Manual data santization removed over 200 mentions related to specific foundation names, email addresses, phone numbers, sensitive geographical refrences, and overly descriptive GMS names. This file is as is and has no associated script.

| left_context | right_context | value | identifier |
| --- | --- | --- | --- |
| Context prior the question (`value`) that is particularly informative for understanding the intent and aim of the question. May be null. | Context following the question (`value`) that is particularly informative for understanding the intent and aim of the question. May be null. | The actual question itself. Never null. | Value related identifier. Never null. |


### task_2_and_3.csv

Scripting that uses [Google's USE](https://research.google.com/pubs/archive/46808.pdf) to calculate pairwise similarity and SciPy's dendogram clustering (`fcluster1`) of pairwise similarity creates this data set. This is created by running `1.0-kpr-pairwise-and-cluster.ipynb`. It depends on `./data/interim` and `./data/processed` files. May take up to an hour to run.

| left_context | right_context | value | group | the_cutoff |
| --- | --- | --- | --- | --- |
| Context prior the question (`value`) that is particularly informative for understanding the intent and aim of the question. May be null. | Context following the question (`value`) that is particularly informative for understanding the intent and aim of the question. May be null. | The actual question itself. Never null. | The [dendogram](https://en.wikipedia.org/wiki/Dendrogram) group the qustion belongs to. Never null. | The [dendogram](https://en.wikipedia.org/wiki/Dendrogram) threshold used to read off groups * Never null. |

\* For more information about cutoff and theshold see the [SciPy `fcluster` API and the `t` parameter]().

size: 3611348 bytes

CRC hash: `3542748097`

### qualitative_non_similar.csv and qualitative_similar.csv

Exported tabular data from data triangulation process. Many column names were specific, ad hoc, and restricted to internal tasks, such as assement and canonical and non-canonical theme references. Only the `value` and `Theme` columns, as well as the `value` and context columns, are utilized. The value and context columns. Note some columns include mispellings (e.g. Theme related columns); this dataset is released for completeness and is not an product for end use.

| left_context | right_context | ... | value | ... | Theme convereted areas OR Theme Converted Areas | 
| --- | --- | --- | --- | --- | --- |
| Context prior the question (`value`) that is particularly informative for understanding the intent and aim of the question. May be null. | Context following the question (`value`) that is particularly informative for understanding the intent and aim of the question. May be null. | ... | The actual question itself. Never null. | ... | Associated theme derived from the data triangulation. This theme should strongly match the `value` through on of its sub-part questions described in the [TAG whitepaper](https://cdn.ymaws.com/www.tagtech.org/resource/resmgr/reports/TAGCommonGrantQuestions.pdf) and [technical report](https://www.tagtech.org/resource/resmgr/reports/TAG-GrantSimilarity-Analysis.pdf) | 


### task_5_i_ii.csv

Scripting that merges the data trangulation mixed method output creates this file. This joins clustered pairwise similarity to fixed associated themes. The mapping from form field to associated provides a significant reduction of over 3,500 questions to 20 question. This is created by running `2.0-kpr-join-data-triangulation.ipynb`. It depends on a `./data/processed` file. Should run within 5 minutes or less.

The associated themes significantly match the `value` through one of its sub-part questions described in the [TAG whitepaper](https://cdn.ymaws.com/www.tagtech.org/resource/resmgr/reports/TAGCommonGrantQuestions.pdf). The [technical report here](https://www.tagtech.org/resource/resmgr/reports/TAG-GrantSimilarity-Analysis.pdf) provide additional detail.

| left_context | right_context | value | group | the_cutoff | hash | Theme |
| --- | --- | --- | --- | --- | --- | --- |
| Context prior the question (`value`) that is particularly informative for understanding the intent and aim of the question. May be null. | Context following the question (`value`) that is particularly informative for understanding the intent and aim of the question. May be null. | The actual question itself. Never null. | The [dendogram](https://en.wikipedia.org/wiki/Dendrogram) group the qustion belongs to. Never null. | The [dendogram](https://en.wikipedia.org/wiki/Dendrogram) threshold used to read off groups *. Never null. | A data hash of `value`, using [Pandas.util.hash](https://pandas.pydata.org/docs/reference/api/pandas.util.hash_pandas_object.html). Never null. | Associated theme derived from the data triangulation. This theme should strongly match the `value` through on of its sub-part questions described in the [TAG whitepaper](https://cdn.ymaws.com/www.tagtech.org/resource/resmgr/reports/TAGCommonGrantQuestions.pdf) and [technical report](https://www.tagtech.org/resource/resmgr/reports/TAG-GrantSimilarity-Analysis.pdf) |

\* For more information about cutoff and theshold see the [SciPy `fcluster` API and the `t` parameter]().

size: 5889619 bytes

CRC hash: `3176681241`