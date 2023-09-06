# Measuring and Mitigating Reasoning Shortcuts in Machine Reading Comprehension


## Related Survey papers
- [Beyond Leaderboards: A survey of methods for revealing weaknesses in Natural Language Inference data and models](https://arxiv.org/abs/2005.14709) - arXiv 2020. ([Updated version on Cambridge.org](https://www.cambridge.org/core/journals/natural-language-engineering/article/survey-of-methods-for-revealing-and-overcoming-weaknesses-of-datadriven-natural-language-understanding/BC8EBADC7D8E5CFC67FC1FE5958E13CC))
- [Shortcut learning in deep neural networks](https://www.nature.com/articles/s42256-020-00257-z) - Nature Machine Intelligence 2020.
- [Measure and Improve Robustness in NLP Models: A Survey](https://aclanthology.org/2022.naacl-main.339/) - NAACL 2022.
- [Shortcut Learning of Large Language Models in Natural Language Understanding](https://arxiv.org/abs/2208.11857) - Communications of the ACM (CACM) 2023


## Measuring Shortcuts

### Adversarial data evaluation

#### Label-Changed 
|Paper| Add/Edit Level | Creation Method | Original Dataset | Naturalness | 
|---|---| --- |--- |--- | 
|Consistency [Ribeiro et al. 2019](https://aclanthology.org/P19-1621/) |question| auto | SQuAD |Yes| 
| Contrast Sets [Gardner et al. 2020](https://aclanthology.org/2020.findings-emnlp.117/) | word | experts | DROP, Quoref, .. | No | 
| SAM [Schlegel et al. 2021](https://ojs.aaai.org/index.php/AAAI/article/view/17622)| word | auto | SQuAD, HotpotQA, DROP, NewsQA | No | 
| Break, Perturb, Build [Geva et al. 2022](https://direct.mit.edu/tacl/article/doi/10.1162/tacl_a_00450/109471/Break-Perturb-Build-Automatic-Perturbation-of) | question | auto | DROP, HotpotQA, IIRC | Yes | 
| **Unanswerable Questions** |
| Not-answerable Questions [Nakanishi et al. 2018](https://aclanthology.org/C18-1083/) | context | auto | SQuAD | Yes |  
| SQuADRUn [Rajpurkar et al. 2018](https://aclanthology.org/P18-2124/)| question | crowdworkers |SQuAD | Yes | 
| Disconnected Reasoning [Trivedi et al. 2020](https://aclanthology.org/2020.emnlp-main.712/)| context| auto | HotpotQA |Yes | 
| MuSiQue [Trivedi et al. 2022](https://direct.mit.edu/tacl/article/doi/10.1162/tacl_a_00475/110996/MuSiQue-Multihop-Questions-via-Single-hop-Question)|context| auto |MuSiQue-Ans| Yes | 


### Artifact-based models


### Intermediate task evaluation
|Paper| Form | Purpose | Task | Github | Dataset | Note | 
|---|---| --- |---|---| --- |---|
| [Inoue et al. 2020](https://aclanthology.org/2020.acl-main.602/) | Triple | Evaluation & Training  | Derivation generation | [URL](https://github.com/naoya-i/r4c) | R4C  | based on HotpotQA |
| [Ho et al. 2020](https://aclanthology.org/2020.coling-main.580/) | Triple | Evaluation & Training  | Evidence generation | [URL](https://github.com/Alab-NII/2wikimultihop) |  2WikiMultiHopQA | |
| [Wolfson et al. 2020](https://direct.mit.edu/tacl/article/doi/10.1162/tacl_a_00309/43549/Break-It-Down-A-Question-Understanding-Benchmark) |  QDMR | Training |  - | [URL](https://github.com/tomerwolgithub/Break) | Break it down  | based on ten datasets (e.g., HotpotQA & DROP) |
| [Tang et al. 2021](https://aclanthology.org/2021.eacl-main.283/) |Sub-question| Evaluation |QA about sub-questions| [URL](https://github.com/yxxytang/subqa) | 1000 samples | based on HotpotQA|
|[Geva et al. 2021](https://direct.mit.edu/tacl/article/doi/10.1162/tacl_a_00370/100680/Did-Aristotle-Use-a-Laptop-A-Question-Answering)|Sub-question| Evaluation & Training |QA about sub-questions|[URL](https://github.com/eladsegal/strategyqa)| StrategyQA |implicit questions|
|[Ho et al. 2022](https://aclanthology.org/2022.aacl-short.58/) |Sub-question| Evaluation & Training |QA about sub-questions|[URL](https://github.com/Alab-NII/HieraDate)| HieraDate | only for comparison about Date information|
|[Trivedi et al. 2022](https://direct.mit.edu/tacl/article/doi/10.1162/tacl_a_00475/110996/MuSiQue-Multihop-Questions-via-Single-hop-Question)|Sub-question| Evaluation & Training | QA about sub-questions |[URL](https://github.com/stonybrooknlp/musique)| MuSiQue | |
| [Dalvi et al. 2021](https://aclanthology.org/2021.emnlp-main.585/)  | Entailment Tree| Evaluation & Training |tree generation| [URL](https://github.com/allenai/entailment_bank/)| EntailmentBank | based on ARC and WorldTree V2 |
|[Ribeiro et al. 2023](https://openreview.net/forum?id=1C_kSW1-k0)|a graph | Evaluation & Training |graph generation|[URL](https://github.com/amazon-science/street-reasoning)| STREET | based on ARC, SCONE, GSM8K, AQUA-RAT, and AR-LSAT|

### Language skills evaluation



## Mitigating Shortcuts

### Training on adversarial data

### Altering the training process

### Utilizing intermediate tasks

### Regularization
