# Large Language Menagerie

A Taxonomy of open-source and/or open-weights LLMs.

At the current pace of innovation, this table can become quickly outdated. Feel free to open PRs to improve it or keep it up-to-date.

| Model Name   | Institution | First release date | Source Code License | Weights License | Dataset License | Dataset Size | Dataset Language(s)  | Model Size | Base Model | Training modality | <div style="width:290px"> Comments </div>|
|--------------|-------------|--------------------|---------------------|-----------------|-----------------|--------------|----------------------|------------|--------------|--------------------|----------|
| [Flan-T5-{}](https://huggingface.co/google/flan-t5-xl) | Google    | October 2022  | Apache 2.0 | Apache 2.0 | N/A | N/A | Many languages | 80M-11B | T5 |   Instruction fine-tuned  |    |
| [GPT4All](https://github.com/nomic-ai/gpt4all)          | Nomic-ai | March 2023      | Apache License 2.0 | | | 800k examples | English | 11B Params | GPT-J | Instruction & dialog fine-tuned  | |
| [LLaMA](https://github.com/facebookresearch/llama)          | Meta | February 2023      | GPL-3  | Non-commercial bespoke license | N/A | >1T tokens | 20 languages | 7B, 13B, 33B, and 65B  | N/A | Causal LM   | First highly performant "small" LLM |
| [Alpaca](https://github.com/tatsu-lab/stanford_alpaca)          | Stanford | March 2023   |Apache License 2.00 | CC BY NC 4.0 (LLaMA weigth diff) | Claims CC BY NC 4.0 but not clear it is!| 54k examples | English | 7B, 13B | LLaMA | Instruction fine-tuned  | [Alpaca](#alpaca)|
| [Vicuña](https://github.com/lm-sys/FastChat) |  UC Berkeley, UCSD, CMU, MBZUAI | March 2023   | Apache License 2.0 | Apache License 2.0 (LLaMA weigth diff) | N/A | 70k examples | N/A | 13B | LLaMA | Instruction & dialog fine-tuned  | [Vicuna](#vicuna) |
| [Koala](https://bair.berkeley.edu/blog/2023/04/03/koala/) | BAIR (Berkeley) | April 2023 | Apache License 2.0 | Unclear [1](#1) | N/A | >350k examples | N/A | 13B | LLaMA | Instruction & dialog fine-tuned  | [Koala](#koala) |
| [FastChat-T5](https://huggingface.co/lmsys/fastchat-t5-3b-v1.0) | UC Berkeley, UCSD, CMU, MBZUAI  | April 2023 | Apache License 2.0 | Unclear [2](#2) | N/A | 70k examples | N/A | 3B | T5-flan-XL | Dialog fine-tuned  |  |
| [Pythia](https://github.com/EleutherAI/pythia) | EleutherAI  | April 2023 | Apache License 2.0 | Apache License 2.0 | "open source" [3](#3) | 300B tokens | Mostly English (though multiple languages) | 70M-12B | GPT-neoX | Causal LM |  |
| [StableLM-Alpha](https://github.com/Stability-AI/StableLM) | Stability-AI  | April 2023 | N/A | CC BY-SA-4.0 | N/A | 1.5T tokens | Mostly English (though multiple languages) | 3B-7B | GPT-neoX | Causal LM | 4k context window, training code not available |
| [Dolly-v2](https://github.com/databrickslabs/dolly) | Databricks | March 2023 | Apache License 2.0 | Apache License 2.0 | CC BY-SA 3.0 | 15k examples | English | 3B-12B | Pythia | Instruction fine-tuned | Not state-of-the-art, first one of the first commercially licensed. |
| [CerebrasGPT](https://www.cerebras.net/blog/cerebras-gpt-a-family-of-open-compute-efficient-large-language-models/) | Cerebras | March 2023 | N/A | Apache License 2.0 | "open source" [3](#3) | 300B tokens | Mostly English (though multiple languages)| 111M-13B | GPT-2 | Causal LM | Developed mostly as demo of cerebra's hardware capabilities, performance sub-par |
| [WizardLM-{7/13/15/30}](https://github.com/nlpxucan/WizardLM) | [WizardLM](https://twitter.com/WizardLM_AI) | April 2023 | [Apache License 2.0](https://github.com/nlpxucan/WizardLM/blob/main/WizardLM/CODE_LICENSE) | Attribution-NonCommercial 4.0 International  | Attribution-NonCommercial 4.0 International (LLaMA weight diff) | 70k instructions | Mostly English | 7, 13, 15, 30B | LLaMA | Causal LM |  |
| [MPT-7B](https://github.com/mosaicml/llm-foundry) | Mosaic ML | May 2023 | Apache License 2.0 | Apache License 2.0 | Various datasets [4](#4) | 300B tokens | Mostly English (though multiple languages)| 7B | MPT | Causal LM | Commercially usable, comparable performance to LLaMA, up to 64k context length |
| [Falcon-7B/40B](https://huggingface.co/tiiuae/falcon-40b) | Technology Innovation Institute UAE | May 2023 | N/A | [TII Falcon LLM License](https://huggingface.co/tiiuae/falcon-7b/raw/main/LICENSE.txt) | [Apache License 2.0](https://huggingface.co/datasets/tiiuae/falcon-refinedweb) + other | 1T tokens | English, German, Spanish, French | 7B, 40B |  | Causal LM | Commercially usable up to capped revenues, top-performer on [OpenLLM](https://huggingface.co/spaces/HuggingFaceH4/open_llm_leaderboard) leaderboard as of date of launch |
| [Orca-13B](https://aka.ms/orca-lm) | Microsoft Research | June 2023 | Unclear, but likely non-commercial | N/A | N/A | 6M examples| Mostly English | 13B | Presumably LLaMA | Causal LM | Pending publication of artifacts & their licenses, but likely restrictive since seems to be based on LLaMA |

<a name="1"></a> [1] Claimed to be "subject to the model License of LLaMA, Terms of Use of the data generated by OpenAI, and Privacy Practices of ShareGPT. Any other usage of the model weights, including but not limited to commercial usage, is strictly prohibited. "

<a name="2"></a> [2] Uses ShareGPT data, which comes form users posting data from ChatGPT, whose terms and conditions are restrictive...

<a name="3"></a> [3] The code to generate the pile is MIT-licensed, and the data itself can be downloaded, no-strings-attached from [here](https://pile.eleuther.ai/). But nowhere it says what the actual license for the dataset is, other than claiming it is "open-source".

<a name="4"></a> [4] Included a [variety of data sources](https://www.mosaicml.com/blog/mpt-7b#appendix-data): mC4, C4, RedPajama, The Stack, Semantic Scholar, mostly public datasets from public data but each with possibly different licenses.

## Comments

- <a name="alpaca"></a>Alpaca: First evidence that small-high quality data can make a relatively small LLM competitive with much bigger models, LLaMA fine-tuned at a cost of ~600USD (dataset gen + training)
- <a name="vicuna"></a>Vicuna: Another LLaMA with model, which GPT-4 grades better than ChatGPT and Alpaca.  Fine-tuned at a cost of ~300USD 
- <a name="koala"></a> Koala: Another LLaMA with model fine-tuned on large, partially propietary dialog dataset, with comparable performance to Alpaca according to human evaluators.
