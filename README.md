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

The dataset is the content of all AWS FAQ pages, downloaded from: https://aws.amazon.com/faqs/

| service | question | answers |
|-------|-------|-------|
| /ec2/autoscaling/faqs/     | What is Amazon EC2 Auto Scaling?   | Amazon EC2 Auto Scaling is a fully managed ser...  |
| /ec2/autoscaling/faqs/    | When should I use Amazon EC2 Auto Scaling vs. ...   | You should use AWS Auto Scaling to manage scal... |
| /ec2/autoscaling/faqs/   | How is Predictive Scaling Policy different fro... | Predictive Scaling Policy brings the similar p... |
| /ec2/autoscaling/faqs/ | What are the benefits of using Amazon EC2 Auto... | Amazon EC2 Auto Scaling helps to maintain your... |

### [train_2.csv.gz](./train_2.csv.gz)

The synthetic dataset is the content of official AWS Generative AI Blogs

| question | answers |
|-------|-------|
| What new Anthropic model is now available on Amazon Bedrock?   | Claude 2.1 foundation model is now available on Amazon Bedrock.  |
| What are the two types of model evaluation available in Amazon Bedrock?   | Amazon Bedrock offers a choice of automatic evaluation and human evaluation. |
| What kind of metrics can you use for automatic evaluation? | You can use automatic evaluation with predefined metrics such as accuracy, robustness, and toxicity. |
| What does Guardrails for Amazon Bedrock allow developers to do? | Guardrails for Amazon Bedrock (preview) to promote safe interactions between users and your generative AI applications by implementing safeguards customized to your use cases and responsible AI policies. |

## Notebooks

1. [[Supervised - Q&A] Falcon-7B](./falcon-7b-qlora-remote-decorator_qa.ipynb)
2. [[Supervised - Q&A] Llama-13B](./llama-13b-qlora-remote-decorator_qa.ipynb)
3. [[Self-supervised - chat] Llama-13B](./llama-13b-qlora-remote-decorator_selfsupervised.ipynb)
4. [[Self-supervised - Instruct] Mistral-7B](./mistral-7b-qlora-remote-decorator_selfsupervised.ipynb)
5. [[Supervised - Instruct] Mixtral-8x7B](./mixtral-8x7b-qlora-remote-decorator_qa.ipynb)
6. [[Supervised - Instruct] Code-Llama 13B](./code-llama-13b-qlora-remote-decorator.ipynb)
7. [[Supervised - Instruct] Llama-3 8B](./llama-3-8b-qlora-remote-decorator_qa.ipynb)
8. [[Supervised - Instruct] Llama-3.1 8B](./llama-3.1-8b-qlora-remote-decorator_qa.ipynb)
9. [[Supervised - Instruct] Arcee AI Llama-3.1 Supernova Lite](./arcee-ai-llama-3.1-supernova-lite-qlora-remote-decorator_qa.ipynb)
10. [[Supervised - Instruct] Llama-3.2 1B](./llama-3.2-1b-qlora-remote-decorator_qa.ipynb)
11. [[Supervised - Instruct] Llama-3.2 3B](./llama-3.2-3b-qlora-remote-decorator_qa.ipynb)