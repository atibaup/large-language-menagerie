# Large Language Menagerie

A Taxonomy of open-source and/or open-weights LLMs.

At the current pace of innovation, this table can become quickly outdated. Feel free to open PRs to improve it or keep it up-to-date.

| Model Name   | Institution | First release date | License | Dataset Size | Dataset Language(s)  | Model Size | Base Model | Training modality | Comments |
|--------------|-------------|--------------------|---------|--------------|----------------------|------------|--------------|--------------------|----------|
| [Flan-T5-{}](https://huggingface.co/google/flan-t5-xl) | Google    | October 2022  | Apache 2.0 | N/A   | Many languages | 80M-11B | T5 |   Instruction fine-tuned  |    |
| [GPT4All](https://github.com/nomic-ai/gpt4all)          | Nomic-ai | March 2023      | Apache License 2.0 | 800k examples | English | 11B Params | GPT-J | Instruction & dialog fine-tuned  | |
| [LLaMA](https://github.com/facebookresearch/llama)          | Meta | February 2023      | GPL-3 (though gated weights) | >1 tokens | 20 languages | 7B, 13B, 33B, and 65B  | N/A | Causal LM   | First highly performant "small" LLM |
| [Alpaca](https://github.com/tatsu-lab/stanford_alpaca)          | Stanford | April 2023   | CC BY NC 4.0 | 54k examples | English | 7B, 13B | LLaMA | Instruction fine-tuned  | A LLaMA with similar qualitative performance as OpenAI's text-davinci-003, fine-tuned at a cost of ~600USD |
