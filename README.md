# Generative AI App

This is a boilerplate repo for aws sam

## Prerequisite
* https://github.com/kiki-miumiu/aws-kendra-sam
* https://github.com/kiki-miumiu/aws-sagemaker-sam

## Deploy Local

### Setup
```bash
git clone https://github.com/kiki-miumiu/Generative-AI-App.git
cd Generative-AI-App
# Install the dependencies
pip install -r src/requirements.txt
```
### Run App Locally
```bash
export AWS_REGION="<YOUR-AWS-REGION>"
export KENDRA_INDEX_ID="<YOUR-KENDRA-INDEX-ID>"
export FLAN_XL_ENDPOINT="<YOUR-SAGEMAKER-ENDPOINT-FOR-FLAN-T-XL>" # sagemaker endpoint name. e.g jumpstart-dft-hf-text2text-flan-t5-xl

#export OPENAI_API_KEY="<YOUR-OPEN-AI-API-KEY>"
streamlit run src/app.py flanxl
```

#### Run sample from the command line[optinal]
```bash
python src/kendra_retriever_flan_xl.py
```

# Notes
* at the time of writing, ml.gd family is not available in ap-southeast-2, you can use ml.g4dn family. you can also find info of which is avilable or not in a region via checking service quote in aws condle
# Reference
[Quickly build high-accuracy Generative AI applications on enterprise data using Amazon Kendra, LangChain, and large language models](https://aws.amazon.com/blogs/machine-learning/quickly-build-high-accuracy-generative-ai-applications-on-enterprise-data-using-amazon-kendra-langchain-and-large-language-models/)

[amazon-kendra-langchain-extensions](https://github.com/aws-samples/amazon-kendra-langchain-extensions)