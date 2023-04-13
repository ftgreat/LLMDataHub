# Datasets for Better LLM Training
## What is this?
A guide for the most frequently used datasets for LLM pretrain/instruction finetune/RLHF.
## Open Access Datasets

| Dataset name                                                                                                                                                                                                                                                                       | Release Date(approx.) | Used by                                                                     | Used for                          | Language                             | Size                                                                                    | Description                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------|-----------------------------------------------------------------------------|-----------------------------------|--------------------------------------|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [databricks-dolly-15k](https://github.com/databrickslabs/dolly/tree/master/data)                                                                                                                                                                                                   | 2023-04-12            | DOlly2.0                                                                    | instruction finetune              | English                              | 15K+ entries                                                                            | A dataset of **human-written** prompts and responses, featuring tasks such as open-domain question-answering, brainstorming, summarization, and more.                                        |
| [AlpacaDataCleaned](https://github.com/gururise/AlpacaDataCleaned)                                                                                                                                                                                                                 | 2023-04-11            | Some Alpaca/LLaMA-like models                                               | instruction finetune              | English                              | /                                                                                       | Cleaned version of Alpaca, GPT_LLM and GPTeacher.                                                                                                                                            |
| [GPT-4-LLM Dataset](https://github.com/Instruction-Tuning-with-GPT-4/GPT-4-LLM)                                                                                                                                                                                                    | 2023-04-06            | Some Alpaca-like models                                                     | instruction finetune/RLHF         | English, Chinese                     | 52K entries for English and Chinese respectively <br/> 9K entries unnatural-instruction | NOT the dataset used by GPT-4!! It is generated by GPT-4 and some other LLM for better instruction finetune and RLHF. It includes instruction data as well as comparison data in RLHF style. |
| [GPTeacher](https://github.com/teknium1/GPTeacher)                                                                                                                                                                                                                                 | 2023-04               | /                                                                           | instruction finetune              | English                              | 20k entries                                                                             | A dataset contains targets generated by GPT-4 and includes many of the same seed tasks as the Alpaca dataset, with the addition of some new tasks such as roleplay.                          |
| [Alpaca data](https://github.com/tatsu-lab/stanford_alpaca#data-release) <br/> [Download](https://github.com/tatsu-lab/stanford_alpaca/blob/main/alpaca_data.json)                                                                                                                 | 2023-03-13            | Alpaca, ChatGLM-finetune-LoRA, Koala                                        | dialog/instruction finetune       | English                              | 52K entries<br/>21.4MB                                                                  | A dataset generated by text-davinci-003 to improve language models' ability to follow human instruction.                                                                                     |
| [OIG](https://huggingface.co/datasets/laion/OIG) <br/> [OIG-small-chip2](https://huggingface.co/datasets/0-hero/OIG-small-chip2)                                                                                                                                                   | 2023-03               | Pythia-Chat-Base-7B, GPT-NeoXT-Chat-Base-20B, Koala                         | dialog/instruction finetune       | English, code                        | 44M entries                                                                             | A large conversational instruction dataset with medium and high quality subsets *(OIG-small-chip2)* for multi-task learning.                                                                 |
| [ChatAlpaca data](https://github.com/cascip/ChatAlpaca)                                                                                                                                                                                                                            | 2023-04-10            | /                                                                           | dialog/instruction finetune       | English, Chinese version coming soon | 10k entries<br/>39.5MB                                                                  | A dataset aims to help researchers develop models for instruction-following in multi-turn conversations.                                                                                     |
| [Firefly(流萤)](https://huggingface.co/datasets/YeungNLP/firefly-train-1.1M)                                                                                                                                                                                                         | 2023-04-03            | Firefly(流萤)                                                                 | instruction finetune              | Chinese                              | 1.1M entries<br/>1.17GB                                                                 | A Chinese instruction-tuning dataset with 1.1 million human-written examples across 23 tasks, but no conversation.                                                                           |
| [BELLE](https://github.com/LianjiaTech/BELLE) <br/> [0.5M version](https://huggingface.co/datasets/BelleGroup/train_0.5M_CN) <br/> [1M version](https://huggingface.co/datasets/BelleGroup/train_1M_CN) <br/> [2M version](https://huggingface.co/datasets/BelleGroup/train_2M_CN) | 2023-04               | BELLE series, Chunhua(春华)                                                   | instruction finetune              | Chinese                              | 2.67B in total                                                                          | A Chinese instruction dataset similar to *Alpaca data* constructed by generating answers from seed tasks, but no conversation.                                                               |
| [GuanacoDataset](https://huggingface.co/datasets/JosephusCheung/GuanacoDataset#guanacodataset)                                                                                                                                                                                     | 2023-03               | Guanaco                                                                     | dialog/instruction finetune       | English, Chinese, Japanese           | 534,530 entries                                                                         | A multilingual instruction dataset for enhancing language models' capabilities in various linguistic tasks, such as natural language understanding and explicit content recognition.         |
| [xP3 (and some variant)](https://huggingface.co/datasets/bigscience/xP3)                                                                                                                                                                                                           | 2022-10               | BLOOMZ, mT0                                                                 | instruction finetune              | Multilingual, code                   | 79M entries<br/>88GB                                                                    | An instruction dataset for improving language models' generalization ability, similar to *Natural Instruct*.                                                                                 |
| [OpenAI WebGPT](https://huggingface.co/datasets/openai/webgpt_comparisons)                                                                                                                                                                                                         | 2023-01               | WebGPT's reward model, Koala                                                | RLHF                              | English                              | 19,578 pairs                                                                            | Data set used in WebGPT paper. Used for training reward model in RLHF.                                                                                                                       |
| [OpenAI Summarization Comparison](https://huggingface.co/datasets/openai/summarize_from_feedback)                                                                                                                                                                                  | 2023-01               | Koala                                                                       | RLHF                              | English                              | ~93K entries<br/>420MB                                                                  | A dataset of human feedback which helps training a reward model. The reward model was then used to train a summarization model to align with human preferences.                              |
| [Natural Instruction](https://instructions.apps.allenai.org/) <br/> [GitHub&Download](https://github.com/allenai/natural-instructions)                                                                                                                                             | /                     | tk-instruct series                                                          | instruction finetune, evaluation  | Multilingual                         | /                                                                                       | A benchmark with over 1,600 tasks with instruction and definition for evaluating and improving language models' multi-task generalization under natural language instruction.                |
| [hh-rlhf](https://github.com/anthropics/hh-rlhf) <br/> [on Huggingface](https://huggingface.co/datasets/Anthropic/hh-rlhf)                                                                                                                                                         | 2022-12               | Koala                                                                       | RLHF, Koala                       | English                              | 161k pairs<br/>79.3MB                                                                   | A pairwise dataset for training reward models in reinforcement learning for improving language models' harmlessness and helpfulness.                                                         |
| [Common Crawl](https://commoncrawl.org/)                                                                                                                                                                                                                                           |                       | LLaMA(After some process)                                                   | building other datasets, pretrain | /                                    | /                                                                                       | The most well-known raw dataset, rarely be used directly. One possible preprocess pipeline is [CCNet](https://github.com/facebookresearch/cc_net)                                            |
| [The Pile (V1)](https://pile.eleuther.ai/)                                                                                                                                                                                                                                         |                       | GLM(partly), LLaMA(partly), GPT-J, GPT-NeoX-20B,Cerebras-GPT 6.7B, OPT-175b | pretrain                          | Multilingual, code                   | 825GB                                                                                   | A diverse open-source language modeling dataset consisting of 22 smaller, high-quality datasets that includes many domains and tasks.                                                        |
| C4 <br/> [Huggingface dataset](https://huggingface.co/datasets/c4) <br/> [TensorFlow dataset](https://www.tensorflow.org/datasets/catalog/c4)                                                                                                                                      |                       | Google T5 Series, LLaMA                                                     | pretrain                          | English                              | 305GB                                                                                   | A colossal, cleaned version of Common Crawl's web crawl corpus. Frequently be used.                                                                                                          |
| [ROOTS](https://huggingface.co/bigscience-data)                                                                                                                                                                                                                                    |                       | BLOOM                                                                       | pretrain                          | Multilingual, code                   | 1.6TB                                                                                   | A diverse open-source dataset consisting of sub-datasets like Wikipedia and StackExchange for language modeling.                                                                             |
| [Pushshift reddit](https://files.pushshift.io/reddit/) <br/> [paper](https://arxiv.org/pdf/2001.08435.pdf)                                                                                                                                                                         |                       | OPT-175b                                                                    | pretrain                          | /                                    | /                                                                                       | Raw reddit data, one possible processing pipeline in [this paper](https://aclanthology.org/2021.eacl-main.24.pdf)                                                                            |
| [Gutenberg project](https://www.gutenberg.org/policy/robot_access.html)                                                                                                                                                                                                            |                       | LLaMA                                                                       | pretrain                          | Multilingual                         | /                                                                                       | A book dataset, mostly novels. Not be preprocessed.                                                                                                                                          |
| [CLUECorpus](https://github.com/CLUEbenchmark/CLUE)                                                                                                                                                                                                                                |                       | /                                                                           | pretrain, finetune, evaluation    | Chinese                              | 100GB                                                                                   | A Chinese pretraining Corpus sourced from *Common Crawl*.                                                                                                                                    |

### Possible Overlap

We consider row items as subject.

|                   | OIG     | hh-rlhf  | xP3     | natural instruct | AlpacaDataCleaned | GPT-4-LLM |
|-------------------|---------|----------|---------|------------------|-------------------|-----------|
| OIG               |         | contains | overlap | overlap          | overlap           |           |
| hh-rlhf           | part of |          |         |                  |                   |           |
| xP3               | overlap |          |         | overlap          |                   |           |
| natural instruct  | overlap |          | overlap |                  |                   |           |
| AlpacaDataCleaned | overlap |          |         |                  |                   | overlap   |
| GPT-4-LLM         |         |          |         |                  | overlap           |           |

## Private Datasets
| Dataset name          | Used by            | Used for            | Language                              | Size        | Description                                                                                     |
|-----------------------|--------------------|---------------------|---------------------------------------|-------------|-------------------------------------------------------------------------------------------------|
| ShareGPT-70K          | Vicuna             | Instruction fintune | /                                     | 70K entries | Data shared by user on [ShareGPT](https://sharegpt.com/)                                        |
| WebText(Reddit links) | GPT-2              | pretrain            | English                               | /           | Data crawled from Reddit and filtered for GPT-2 pretraining.                                    |
| MassiveText           | Gopher, Chinchilla | pretrain            | 99% English, 1% other(including code) |             |                                                                                                 |
| WuDao(悟道) Corpora     | GLM                | pretrain            | Chinese                               | 200GB       | A large scale Chinese corpus, Possible component originally open-sourced but not available now. |
