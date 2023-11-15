# Fine-tune Foundation Models on Amazon SageMaker using @remote decorator

In this example we will go through the steps required for fine-tuning foundation models on Amazon SageMaker by using @remote decorator for executing SageMaker Training jobs.

You can run this repository from Amazon SageMaker Studio or from your local IDE.

## Dataset

The dataset is the content of all AWS FAQ pages, downloaded from: https://aws.amazon.com/faqs/

| service | question | answers |
|-------|-------|-------|
| /ec2/autoscaling/faqs/     | What is Amazon EC2 Auto Scaling?   | Amazon EC2 Auto Scaling is a fully managed ser...  |
| /ec2/autoscaling/faqs/    | When should I use Amazon EC2 Auto Scaling vs. ...   | You should use AWS Auto Scaling to manage scal... |
| /ec2/autoscaling/faqs/   | How is Predictive Scaling Policy different fro... | Predictive Scaling Policy brings the similar p... |
| /ec2/autoscaling/faqs/ | What are the benefits of using Amazon EC2 Auto... | Amazon EC2 Auto Scaling helps to maintain your... |

## Notebooks

1. [[Supervised - Q&A] Falcon-7B](./falcon-7b-qlora-remote-decorator_qa.ipynb)
2. [[Supervised - Q&A] Llama-13B](./llama-13b-qlora-remote-decorator_qa.ipynb)
3. [[Unsupervised - chat] Llama-13B](./llama-13b-qlora-remote-decorator_unsupervised.ipynb)
4. [[Unsupervised - Instruct] Mistral-7B](./mistral-7b-qlora-remote-decorator_unsupervised.ipynb)