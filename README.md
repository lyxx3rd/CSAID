# CSAID
CSAID: A Chinese statute retrieval dataset with implicit, multi-issue legal queries annotated with multiple applicable statutes.

## 1. Download data

```
from modelscope.msdatasets import MsDataset
ds =  MsDataset.load('l424102993/CSAID', cache_dir="./data/")
```

## use example

use example in csaid_example.ipynb

## info of CSAID

| Statistic | STARD | CSAID |
| :--- | :--- | :--- |
| Train queries | 1,234 | --- |
| Test queries | 309 | 118 |
| Avg. query len. | 27.31 | 39.66 |
| Avg. statute len. | 126.80 | 170.77 |
| Statute corpus size | 55,348 | 79,055 |
| Avg. relevant statutes | 1.76 | 7.16 |

*Summary statistics of the datasets used in this study. Statute length refers to the character length of statutory articles, and "relevant statutes" denotes the number of gold-annotated applicable statutes per query.*
