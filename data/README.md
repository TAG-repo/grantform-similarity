## Data Dictionary

### task_2_and_3.csv
| left_context | right_context | value | group | the_cutoff |
| --- | --- | --- | --- | --- |
| Context prior the question (`value`) that is particularly informative for understanding the intent and aim of the question. May be null. | Context following the question (`value`) that is particularly informative for understanding the intent and aim of the question. May be null. | The actual question itself. Never null. | The [dendogram](https://en.wikipedia.org/wiki/Dendrogram) group the qustion belongs to. Never null. | The [dendogram](https://en.wikipedia.org/wiki/Dendrogram) threshold used to read off groups^* Never null. |

* For more information about cutoff and theshold see the [SciPy `fcluster` API and the `t` parameter]().

size: 3611348 bytes
CRC hash: `3542748097`

### task_5_i_ii.csv
left_context,right_context,value,group,the_cutoff,hash,Theme
| left_context | right_context | value | group | the_cutoff | hash | Theme |
| --- | --- | --- | --- | --- | --- | --- |
| Context prior the question (`value`) that is particularly informative for understanding the intent and aim of the question. May be null. | Context following the question (`value`) that is particularly informative for understanding the intent and aim of the question. May be null. | The actual question itself. Never null. | The [dendogram](https://en.wikipedia.org/wiki/Dendrogram) group the qustion belongs to. Never null. | The [dendogram](https://en.wikipedia.org/wiki/Dendrogram) threshold used to read off groups^*. Never null. | A data hash of `value`, using [Pandas.util.hash](https://pandas.pydata.org/docs/reference/api/pandas.util.hash_pandas_object.html). Never null. | Associated theme derived from the data triangulation. This theme should strongly match the `value` through on of its sub-parts |

* For more information about cutoff and theshold see the [SciPy `fcluster` API and the `t` parameter]().

size: 5889619 bytes
CRC hash: `3176681241`