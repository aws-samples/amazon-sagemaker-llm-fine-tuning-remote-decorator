# Interactive fine-tuning of Foundation Models with Amazon SageMaker Training using @remote decorator

In this example we will go through the steps required for interactively fine-tuning foundation models on Amazon SageMaker AI by using @remote decorator for executing Training jobs.

You can run this repository from Amazon SageMaker Studio or from your local IDE.

For additional information, take a look at the AWS Blog [Fine-tune Falcon 7B and other LLMs on Amazon SageMaker with @remote decorator](https://aws.amazon.com/blogs/machine-learning/fine-tune-falcon-7b-and-other-llms-on-amazon-sagemaker-with-remote-decorator/)

### 💡 Important: The scope of these notebook examples is to showcase interactive experience with SageMaker AI capabilities and @remote decorator, for Small/Large Language Models fine-tuning by using different distribution techniques, such as FSDP, and DDP. After your interactive experimentation and testing, the recommended path to prod is through SageMaker [ModelTrainer](https://sagemaker.readthedocs.io/en/stable/api/training/model_trainer.html).

## Table of Contents

- [Prerequisites](#prerequistes)
- [Notebooks](#notebooks)
- [Troubleshoot](#troubleshoot)

## Prerequistes

The notebooks are currently using the latest [PyTorch](https://github.com/aws/deep-learning-containers/blob/master/available_images.md) Training Container available for the region `us-east-1`. If you are running the notebooks in a different region, make sure to update the _ImageUri_ in the file [config.yaml](./config.yaml).

### Make sure the Python version in your local environment matches the one in the used container

Python version used in the training container: Python 3.11

⚠️ Make sure your local Python version is aligned with the Python version in the container.

### If you want to operate in a different AWS region

1. Navigate [Available Deep Learning Containers Images](Available Deep Learning Containers Images)
2. Select the right Hugging Face TGI container for model training based on your selected region
3. Update _ImageUri_ in the file [config.yaml](./config.yaml)

## Notebooks

1. [[Supervised - QLoRA] Falcon-7B](./falcon/falcon-7b-ddp-qlora-remote-decorator_qa.ipynb)
2. [[Supervised - QLoRA, FSDP] Llama-13B](./llama/llama-13b-qlora-fsdp-remote-decorator_qa.ipynb)
3. [[Self-supervised - QLoRA, FSDP] Llama-13B](./llama/llama-13b-qlora-fsdp-remote-decorator_selfsupervised.ipynb)
4. [[Self-supervised - QLoRA] Mistral-7B](./mistral/mistral-7b-qlora-remote-decorator_selfsupervised.ipynb)
5. [[Supervised - QLoRA, FSDP] Mixtral-8x7B](./mistral/mixtral-8x7b-qlora-fsdp-remote-decorator_qa.ipynb)
6. [[Supervised - QLoRA, DDP] Code-Llama 13B](./llama/code-llama-13b-qlora-ddp-remote-decorator.ipynb)
7. [[Supervised - QLORA, DDP] Llama-3 8B](./llama/llama-3-8b-qlora-ddp-remote-decorator_qa.ipynb)
8. [[Supervised - QLoRA, DDP] Llama-3.1 8B](./llama/llama-3.1-8b-qlora-ddp-remote-decorator_qa.ipynb)
9. [[Supervised - QLoRA, DDP] Arcee AI Llama-3.1 Supernova Lite](./arcee-ai/arcee-ai-llama-3.1-supernova-lite-qlora-ddp-remote-decorator_qa.ipynb)
10. [[Supervised - QLoRA] Llama-3.2 1B](./llama/llama-3.2-1b-qlora-remote-decorator_qa.ipynb)
11. [[Supervised - QLoRA] Llama-3.2 3B](./llama/llama-3.2-3b-qlora-remote-decorator_qa.ipynb)
12. [[Supervised - QLoRA, FSDP] Codestral-22B](./codestral-22b-fsdp-qlora-remote-decorator_qa.ipynb)
13. [[Supervised - LoRA] TinyLlama 1.1B](./llama/tiny-llama-1.1b-lora-remote-decorator_qa.ipynb)
14. [[Supervised - LoRA] Arcee Lite 1.5B](./arcee-ai/arcee-ai-arcee-lite-1.5b-lora-remote-decorator_qa.ipynb)
15. [[Supervised - LoRA] SmolLM2-1.7B-Instruct](./huggingface/smollm2-1.7b-lora-remote-decorator_qa.ipynb)
16. [[Supervised - QLORA, FSDP] Qwen 2.5 7B](./qwen/qwen-2.5-7b-qlora-fsdp-remote-decorator_qa.ipynb)
17. [[Supervised - QLORA] Falcon3 3B](./falcon/falcon3-3b-qlora-remote-decorator_qa.ipynb)
18. [[Supervised - QLORA, FSDP] Falcon3 7B](./falcon/falcon3-7b-fsdp-qlora-remote-decorator_qa.ipynb)
19. [[Supervised - QLORA, FSDP] Llama-3.1 70B](./llama/llama-3.1-70b-fsdp-qlora-remote-decorator_qa.ipynb)
20. [[Self-supervised - DoRA, FSDP] Mistral-7B v0.3](./mistral/mistral-7b-fsdp-dora-remote-decorator_qa.ipynb)
21. [[Supervised - QLORA, FSDP] Llama-3.3 70B](./llama/llama-3.3-70b-fsdp-qlora-remote-decorator_qa.ipynb)
22. [[Supervised - QLORA, FSDP] OpenCoder-8B-Instruct](./infly/opencoder-8b-fsdp-qlora-remote-decorator_qa.ipynb)
23. [[Supervised - QLORA, FSDP] DeepSeek-R1-Distill-Qwen-32B](./deepseek/deepseek-r1-distilled-qwen-32b-fsdp-qlora-remote-decorator_qa.ipynb)
24. [[Supervised - QLORA, FSDP] DeepSeek-R1-Distill-Llama-70B](./deepseek/deepseek-r1-distilled-llama-70b-fsdp-qlora-remote-decorator_qa.ipynb)
25. [[Supervised - QLORA, FSDP] DeepSeek-R1-Distill-Llama-8B](./deepseek/deepseek-r1-distilled-llama-8b-fsdp-qlora-remote-decorator_qa.ipynb)
26. [[Supervised - QLORA, DDP] DeepSeek-R1-Distill-Qwen-1.5B](./deepseek/deepseek-r1-distilled-qwen-1.5b-qlora-remote-decorator_qa.ipynb)
27. [[Supervised - QLORA, FSDP] DeepSeek-R1-Distill-Qwen-7B](./deepseek/deepseek-r1-distilled-qwen-7b-fsdp-qlora-remote-decorator_qa.ipynb)
28. [[Supervised - QLORA, FSDP] Qwen3-32B](./qwen/qwen-3-32b-qlora-fsdp-remote-decorator_qa.ipynb)
29. [[Supervised - QLORA, FSDP] Qwen3-8B](./qwen/qwen-3-8b-qlora-fsdp-remote-decorator_qa.ipynb)

---

## Troubleshoot

### Issue 1 - Error cloudpickle.\_function_setstate

```
return cloudpickle.loads(bytes_to_deserialize)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Traceback (most recent call last): in deserialize return cloudpickle.loads(bytes_to_deserialize)
YYYY-MM-DDThh:mm:ss
AttributeError: Can't get attribute '_function_setstate' on <module 'cloudpickle.cloudpickle' from '/opt/conda/lib/python3.11/site-packages/cloudpickle/cloudpickle.py'>
```

#### Solution

Align your `cloudpickle` local version to the container one, by including in your `requirements.txt`:

```yaml
cloudpickle==x.x.x
```

Where x.x.x is the version you want to install.

---

### Issue 2 - Error: TypeError when deserializing bytes from S3

```
Error when deserializing bytes downloaded from s3:////exception/payload.pkl:
TypeError('unpickle_exception() takes 4 positional arguments but 7 were given').
NOTE: this may be caused by inconsistent sagemaker python sdk versions where remote function runs versus the one used on client side.
If the sagemaker versions do not match, a warning message would be logged starting with 'Inconsistent sagemaker versions found'.
Please check it to validate.
```

#### Solution

This behavior may happen when you are executing the @remote training job from a local environment with CPU, and run the training workload with GPU instances. This reported exception is not related to SageMaker Python SDK.

The error message shown above is not the actual exception. To investigate the real issue:

1. Check the CloudWatch logs generated by the training job
2. Look for detailed error messages in the logs that will provide more insight into what's actually failing

Note that environment mismatches between local and remote execution environments can sometimes cause serialization/deserialization issues that manifest with this error.

### Issue 3 ModuleNotFoundError No module named 'torch.accelerator'

```
ModuleNotFoundError("No module named \'torch.accelerator\'"). NOTE: this may be caused by inconsistent sagemaker python sdk versions where remote function runs versus the one used on client side. If the sagemaker versions do not match, a warning message would be logged starting with \'Inconsistent sagemaker versions found\'. Please check it to validate.')
```

#### Solution

This error happens when your local `torch` version is not aligned with the version used in the SageMaker Training container. Make sure you have installed in your development environment the same `torch` version used in the Image specified in the file `config.yaml`.
