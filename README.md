# OSSBIG AI engineering team 2024

This is the central repository for the OSSBIG AI engineering team.

## General Informations

### Useful Links

- Benchmark Referenz: https://nicholas.carlini.com/writing/2024/my-benchmark-for-large-language-models.html
- Neue Veröffentlichung: https://opencodeinterpreter.github.io/#example
- GPT from Numpy: https://jaykmody.com/blog/gpt-from-scratch/

### Karpathy - Build GPT From Scratch

Very informative videos about the internals of a LLM. A real step by step description were everything is expained in detail.

- Lets build the GPT Tokenizer: https://youtu.be/zduSFxRajkE?si=oiY3IYLJjNB3nR86
- The spelled-out intro to language modeling: building makemore: https://youtu.be/PaCmpygFfXo?si=Xo-7vP22l-I6l028
- Building makemore Part 2: MLP: https://youtu.be/TCH_1BHY58I?si=Ozu9nNz6EAiBMAFP
- Building makemore Part 3: Activations & Gradients, BatchNorm: https://youtu.be/P6sfmUTpUmc?si=qNfH2TI5QzDh4gVa
- Building makemore Part 4: Becoming a Backprop Ninja: https://youtu.be/q8SA3rM6ckI?si=_50lnWJpjG4iwknc

## OSSBIG

A link collection to the code and data that was generated for the OSSBIG.

### Workbooks and Repositories

- Modified IDEA Plugin (Branch KRM) to work with LLMs. Builded versions are in the OSSBIG cloud: https://github.com/mankra/llm-intellij

#### CUDA

- CUDA acceleration in C: https://colab.research.google.com/drive/1N50mFGvlg0CFGDONdsS0ZQL2NyJEAMMt#scrollTo=HLdoj4cz-xal
- CUDA code repository (Branch CUDA): https://github.com/mankra/llama2.c

#### Finetuning workbooks and repositories

- Source of the following experiments https://huggingface.co/blog/personal-copilot
- Finetuning Code Repository (Data preperation, training): https://github.com/mankra/finetune
- Full finetuning workbook for endless-sky: https://colab.research.google.com/drive/1d99cUGdeHpu06pCMT-ioapw97EkR7ha1#scrollTo=zqtjrruXXKu9
- Full finetuning workbook for fltk: https://colab.research.google.com/drive/1u7PLPCE3bKHzhkSdxhcrFqko-k26pPfw#scrollTo=zqtjrruXXKu9
- PEFT finetuning workbook for endless-sky: https://colab.research.google.com/drive/18XqYBVkJv9lqwrnWuoI06ZUxQUuwiR1U#scrollTo=4AXJGt-ag4l5
- PEFT finetuning workbook for fltk: https://colab.research.google.com/drive/1dXruWXemEYI7srTbNAjEe_ESEvRFGBBT#scrollTo=v8MG0g-eEW9X
- Merge PEFT Layer with base model: https://colab.research.google.com/drive/1GWCLdRmZNXh6CbOMAwou4FRQCe19K-8x#scrollTo=dOIeFZfbiQmz
- WanDB finetuning results (manfredkral9 at gmail account needed to view): https://wandb.ai/ossbig/huggingface

### Hugging Face

The datasets and models are set to private, so a login in the OSSBIG-HF account (Franz's-OSSBIG-email) is required.

#### Datasets

- endless-sky dataset for finetuning: https://huggingface.co/datasets/ossbig2024/endless-sky-master
- fltk dataset for finetuning: https://huggingface.co/datasets/ossbig2024/fltk-1.4.x

#### Models

- Full finetuned starcoder model with endless-sky: https://huggingface.co/ossbig2024/starcoderbase1b-personal-copilot-A100-40GB-colab-endless-sky
- Full finetuned starcoder model with fltk: https://huggingface.co/ossbig2024/starcoderbase1b-personal-copilot-A100-40GB-colab-fltk-1.4.x
- PEFT-Layer finetuned with endless-sky. A custom handler was necessary to get it loaded as inference endpoint (https://huggingface.co/ossbig2024/starcoder-LORA-endless-sky/blob/main/handler.py). It seems that the tokenizer is not configured correctly: https://huggingface.co/ossbig2024/starcoder-LORA-endless-sky
- Merged PEFT-Layer with base model (seems like this did not work, because the model is still pretty small): https://huggingface.co/ossbig2024/starcoder-LORA-endless-sky-merged

#### Inference Endpoints

- List of all OSSBIG inference endpoints: https://ui.endpoints.huggingface.co/ossbig2024/endpoints/dedicated
- starcoder (not modified): https://dg6m2lge10naythk.us-east-1.aws.endpoints.huggingface.cloud
- starcoder finetuned with fltk: https://wzggtcyqoo8yqru1.us-east-1.aws.endpoints.huggingface.cloud
- starcoder finetuned with endless-sky: https://qoge3l92yjotbvkl.us-east-1.aws.endpoints.huggingface.cloud
- starcoder base model: https://dq9aq8vpwch1ox86.us-east-1.aws.endpoints.huggingface.cloud
- code llamaa 7b: https://w31t8m73lcjkl8in.us-east-1.aws.endpoints.huggingface.cloud
- code llamaa 7b Instruct: https://aar1w1cxytqfah8l.us-east-1.aws.endpoints.huggingface.cloud

