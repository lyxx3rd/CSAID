# CSAID

**CSAID** is a Chinese statute retrieval dataset designed for **complex legal queries with implicit semantics and multiple legal issues**.  
Each query is annotated with **multiple applicable statutory articles**, making it suitable for evaluating advanced legal retrieval systems.

CSAID is introduced in the paper:

> **LegalMALR: Multi-Agent Query Understanding and LLM-Based Reranking for Chinese Statute Retrieval**

---

# Dataset Overview

Legal statute retrieval in real-world scenarios often involves:

- **Implicit legal intent**
- **Multiple legal issues in a single query**
- **Colloquial or non-technical descriptions of legal situations**

To better evaluate retrieval systems under these challenges, we construct **CSAID**, a dataset focusing on **difficult statute retrieval queries** that require deeper legal reasoning.

Key characteristics:

- Complex real-world legal queries
- Multiple relevant statutes per query
- Larger statute corpus compared with existing benchmarks
- Designed for evaluating **multi-stage retrieval and reasoning systems**

---

# Download

CSAID can be downloaded using **ModelScope**:

```python
from modelscope.msdatasets import MsDataset

ds = MsDataset.load(
    'l424102993/CSAID',
    cache_dir="./data/"
)
````

The dataset will be automatically downloaded to the specified directory.

---

# Usage Example

A simple usage example is provided in:

```
csaid_example.ipynb
```

The notebook demonstrates:

* Loading the dataset
* Inspecting query–statute pairs
* Running retrieval experiments

---

# Dataset Statistics

| Statistic              |  STARD |  CSAID |
| :--------------------- | :----: | :----: |
| Train queries          |  1,234 |   ---  |
| Test queries           |   309  |   118  |
| Avg. query length      |  27.31 |  39.66 |
| Avg. statute length    | 126.80 | 170.77 |
| Statute corpus size    | 55,348 | 79,055 |
| Avg. relevant statutes |  1.76  |  7.16  |

**Table:** Summary statistics of the datasets used in this study.
Statute length refers to the **character length of statutory articles**, and *relevant statutes* denotes the number of **gold-annotated applicable statutes per query**.

Compared with STARD, CSAID contains:

* **Longer and more complex queries**
* **A larger statute corpus**
* **Significantly more relevant statutes per query**

These properties make CSAID a **more challenging benchmark for statute retrieval systems**.

---

# Citation

If you use CSAID in your research, please cite:

```bibtex
@misc{li2026legalmalrmultiagentqueryunderstandingllmbased,
  title={LegalMALR: Multi-Agent Query Understanding and LLM-Based Reranking for Chinese Statute Retrieval},
  author={Yunhan Li and Mingjie Xie and Gaoli Kang and Zihan Gong and Gengshen Wu and Min Yang},
  year={2026},
  eprint={2601.17692},
  archivePrefix={arXiv},
  primaryClass={cs.IR},
  url={https://arxiv.org/abs/2601.17692}
}
```

---

# License

The dataset is released for **research purposes only**.
Please refer to the repository license for usage restrictions.


