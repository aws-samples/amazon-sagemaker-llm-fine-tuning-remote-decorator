# Fine-tune Foundation Models on Amazon SageMaker using @remote decorator

In this example we will go through the steps required for fine-tuning foundation models on Amazon SageMaker by using @remote decorator for executing SageMaker Training jobs.

You can run this repository from Amazon SageMaker Studio or from your local IDE.

For additional information, take a look at the AWS Blog [Fine-tune Falcon 7B and other LLMs on Amazon SageMaker with @remote decorator](https://aws.amazon.com/blogs/machine-learning/fine-tune-falcon-7b-and-other-llms-on-amazon-sagemaker-with-remote-decorator/)

This notebook is inspired by [Philipp Schmid Blogs](https://www.philschmid.de/)

## Prerequistes

The notebooks are currently using the latest [PyTorch](https://github.com/aws/deep-learning-containers/blob/master/available_images.md) Training Container available for the region `us-east-1`. If you are running the notebooks in a different region, make sure to update the *ImageUri* in the file [config.yaml](./config.yaml).

### If you want to operate in a different AWS region

1. Navigate [Available Deep Learning Containers Images](Available Deep Learning Containers Images)
2. Select the right Hugging Face TGI container for model training based on your selected region
3. Update *ImageUri* in the file [config.yaml](./config.yaml)

## Notebooks

1. [[Supervised - QLoRA] Falcon-7B](./falcon-7b-ddp-qlora-remote-decorator_qa.ipynb)
2. [[Supervised - QLoRA, FSDP] Llama-13B](./llama-13b-qlora-fsdp-remote-decorator_qa.ipynb)
3. [[Self-supervised - QLoRA, FSDP] Llama-13B](./llama-13b-qlora-fsdp-remote-decorator_selfsupervised.ipynb)
4. [[Self-supervised - QLoRA] Mistral-7B](./mistral-7b-qlora-remote-decorator_selfsupervised.ipynb)
5. [[Supervised - QLoRA, FSDP] Mixtral-8x7B](./mixtral-8x7b-qlora-fsdp-remote-decorator_qa.ipynb)
6. [[Supervised - QLoRA, DDP] Code-Llama 13B](./code-llama-13b-qlora-ddp-remote-decorator.ipynb)
7. [[Supervised - QLORA, DDP] Llama-3 8B](./llama-3-8b-qlora-ddp-remote-decorator_qa.ipynb)
8. [[Supervised - QLoRA, DDP] Llama-3.1 8B](./llama-3.1-8b-qlora-ddp-remote-decorator_qa.ipynb)
9. [[Supervised - QLoRA, DDP] Arcee AI Llama-3.1 Supernova Lite](./arcee-ai-llama-3.1-supernova-lite-qlora-ddp-remote-decorator_qa.ipynb)
10. [[Supervised - QLoRA] Llama-3.2 1B](./llama-3.2-1b-qlora-remote-decorator_qa.ipynb)
11. [[Supervised - QLoRA] Llama-3.2 3B](./llama-3.2-3b-qlora-remote-decorator_qa.ipynb)
12. [[Supervised - QLoRA, FSDP] Codestral-22B](./codestral-22b-fsdp-qlora-remote-decorator_qa.ipynb)
13. [[Supervised - LoRA] TinyLlama 1.1B](./tiny-llama-1.1b-lora-remote-decorator_qa.ipynb)
14. [[Supervised - LoRA] Arcee Lite 1.5B](./arcee-ai-arcee-lite-1.5b-lora-remote-decorator_qa.ipynb)
15. [[Supervised - LoRA] SmolLM2-1.7B-Instruct](./smollm2-1.7b-lora-remote-decorator_qa.ipynb)
16. [[Supervised - QLORA, FSDP] Qwen 2.5 7B](./qwen-2.5-7b-qlora-fsdp-remote-decorator_qa.ipynb)
17. [[Supervised - QLORA] Falcon3 3B](./falcon3-3b-qlora-remote-decorator_qa.ipynb)
18. [[Supervised - QLORA, FSDP] Falcon3 7B](./falcon3-7b-fsdp-qlora-remote-decorator_qa.ipynb)
19. [[Supervised - QLORA, FSDP] Llama-3.1 70B](./llama-3.1-70b-fsdp-qlora-remote-decorator_qa.ipynb)
20. [[Self-supervised - DoRA, FSDP] Mistral-7B v0.3](./mistral-7b-fsdp-dora-remote-decorator_qa.ipynb)
21. [[Supervised - QLORA, FSDP] Llama-3.3 70B](./llama-3.3-70b-fsdp-qlora-remote-decorator_qa.ipynb)