# Fine-tune Foundation Models on Amazon SageMaker using @remote decorator

In this example we will go through the steps required for fine-tuning foundation models on Amazon SageMaker by using @remote decorator for executing SageMaker Training jobs.

You can run this repository from Amazon SageMaker Studio or from your local IDE.

## Prerequistes

The notebooks are currently using the latest [HuggingFace](https://github.com/aws/deep-learning-containers/blob/master/available_images.md) Training Container available for the region `eu-west-1`. If you are running the notebooks in a different region, make sure to update the *ImageUri* in the file [config.yaml](./config.yaml).

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

| question | answers |
|-------|-------|
| What new Anthropic model is now available on Amazon Bedrock?   | Claude 2.1 foundation model is now available on Amazon Bedrock.  |
| What are the two types of model evaluation available in Amazon Bedrock?   | Amazon Bedrock offers a choice of automatic evaluation and human evaluation. |
| What kind of metrics can you use for automatic evaluation? | You can use automatic evaluation with predefined metrics such as accuracy, robustness, and toxicity. |
| What does Guardrails for Amazon Bedrock allow developers to do? | Guardrails for Amazon Bedrock (preview) to promote safe interactions between users and your generative AI applications by implementing safeguards customized to your use cases and responsible AI policies. |

## Notebooks

1. [[Supervised - Q&A] Falcon-7B](./falcon-7b-qlora-remote-decorator_qa.ipynb)
2. [[Supervised - Q&A] Llama-13B](./llama-13b-qlora-remote-decorator_qa.ipynb)
3. [[Unsupervised - chat] Llama-13B](./llama-13b-qlora-remote-decorator_unsupervised.ipynb)
4. [[Unsupervised - Instruct] Mistral-7B](./mistral-7b-qlora-remote-decorator_unsupervised.ipynb)
5. [[Supervised - Instruct] Mixtral-8x7B](./mixtral-8x7b-qlora-remote-decorator_qa.ipynb)