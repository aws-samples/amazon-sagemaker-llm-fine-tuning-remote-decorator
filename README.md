# Fine-tune Foundation Models on Amazon SageMaker using @remote decorator

In this example we will go through the steps required for fine-tuning foundation models on Amazon SageMaker by using @remote decorator for executing SageMaker Training jobs.

You can run this repository from Amazon SageMaker Studio or from your local IDE.

For additional information, take a look at the AWS Blog [Fine-tune Falcon 7B and other LLMs on Amazon SageMaker with @remote decorator](https://aws.amazon.com/blogs/machine-learning/fine-tune-falcon-7b-and-other-llms-on-amazon-sagemaker-with-remote-decorator/)

This notebook is inspired by [Philipp Schmid Blogs](https://www.philschmid.de/)

## Prerequistes

The notebooks are currently using the latest [HuggingFace](https://github.com/aws/deep-learning-containers/blob/master/available_images.md) Training Container available for the region `us-east-1`. If you are running the notebooks in a different region, make sure to update the *ImageUri* in the file [config.yaml](./config.yaml).

### If you want to operate in a different AWS region

1. Navigate [Available Deep Learning Containers Images](Available Deep Learning Containers Images)
2. Select the right Hugging Face TGI container for model training based on your selected region
3. Update *ImageUri* in the file [config.yaml](./config.yaml)

## Dataset

### [train.csv.gz](./train.csv.gz)

The dataset is the content of [AmazonQA: A Review-Based Question Answering Task](https://github.com/amazonqa/amazonqa?tab=readme-ov-file) from row 0 to 200

| question | answers |
|-------|-------|
| What ISO range is covered when in set on auto-... | I believe it is 12800 or 25600 by default. I s... |
| Will this fit the Nordic Ware 13x18 Baking Pan...	| YES!!! I purchased both and I was a bit conc... |
| Will these fit 35"-36" inseam? | I use a 32" and I would say a 34" would be the... |
| How long does it take for flowers to blossom? | 1 to 3 minutes. |
| Will these fit a 1997 Dodge 2500 4wd pickup? | No, the kit you need is made specifically for ... |


### [train_2.csv.gz](./train_2.csv.gz)

The dataset is the content of [AmazonQA: A Review-Based Question Answering Task](https://github.com/amazonqa/amazonqa?tab=readme-ov-file) from row 201 to 401

| question | answers |
|-------|-------|
| Does this frame fit on risers? | Yes, but underbed storage boxes fit without them |
| how does the case stay closed (with keyboard a...	| Hi Nate. It is slightly magnetized without the... |
| I have Left & Right JVC MX GT88 speakers both ...	| The RCA output jack is for the subwoofer only.... |
| I want to use my fizz giz with a large co2tank...	| I asked MrFizz the same question in a email an... |
| What are the dimensions of this item?	| Specifications: * 300 watts RMS @ 0.5% THD int... |

### [train_3.csv.gz](./train_3.csv.gz)

The dataset is the content of [AmazonQA: A Review-Based Question Answering Task](https://github.com/amazonqa/amazonqa?tab=readme-ov-file) from row 402 to 602

| question | answers |
|-------|-------|
| Is this TV 120Hz or 240hz actually? Because I ...	| I think is a 120 Hz I wish and hope you guys c... |
| What type of voltage does this use? is it dual...	| 110 volts |
| This thing seems to be designed for the big 20...	| the unit works very well with the small canisters |
| Is there a setting to automatically start trac...	| No. As soon as you turn the power switch to on... |
| Is she a viened reborn? | No |

## Notebooks

1. [[Supervised - QLoRA] Falcon-7B](./falcon-7b-qlora-remote-decorator_qa.ipynb)
2. [[Supervised - QLoRA] Llama-13B](./llama-13b-qlora-remote-decorator_qa.ipynb)
3. [[Self-supervised - QLoRA] Llama-13B](./llama-13b-qlora-remote-decorator_selfsupervised.ipynb)
4. [[Self-supervised - QLoRA] Mistral-7B](./mistral-7b-qlora-remote-decorator_selfsupervised.ipynb)
5. [[Supervised - QLoRA] Mixtral-8x7B](./mixtral-8x7b-qlora-remote-decorator_qa.ipynb)
6. [[Supervised - QLoRA] Code-Llama 13B](./code-llama-13b-qlora-remote-decorator.ipynb)
7. [[Supervised - QLORA, DDP] Llama-3 8B](./llama-3-8b-qlora-remote-decorator_qa.ipynb)
8. [[Supervised - QLoRA, DDP] Llama-3.1 8B](./llama-3.1-8b-qlora-remote-decorator_qa.ipynb)
9. [[Supervised - QLoRA, DDP] Arcee AI Llama-3.1 Supernova Lite](./arcee-ai-llama-3.1-supernova-lite-qlora-remote-decorator_qa.ipynb)
10. [[Supervised - QLoRA] Llama-3.2 1B](./llama-3.2-1b-qlora-remote-decorator_qa.ipynb)
11. [[Supervised - QLoRA] Llama-3.2 3B](./llama-3.2-3b-qlora-remote-decorator_qa.ipynb)
12. [[Supervised - QLoRA, FSDP] Codestral-22B](./codestral-22b-fsdp-qlora-remote-decorator_qa.ipynb)
13. [[Supervised - LoRA] TinyLlama 1.1B](./tiny-llama-1.1b-lora-remote-decorator_qa.ipynb)
14. [[Supervised - LoRA] Arcee Lite 1.5B](./arcee-ai-arcee-lite-1.5b-lora-remote-decorator_qa.ipynb)
15. [[Supervised - LoRA] SmolLM2-1.7B-Instruct](./smollm2-1.7b-lora-remote-decorator_qa.ipynb)
16. [[Supervised - QLORA, FSDP] Qwen 2.5 7B](./qwen-2.5-7b-qlora-remote-decorator_qa.ipynb)