# Med-ChatBot

This project is the final assignment of the natural language processing course and is completed by a group of four people.

SCHOOL OF CYBER SCIENCE AND ENGINEERING-WHU

The following are the original requirements for the experiment:

l **Description**

A conversational bot is a program that converses through dialogue or text. For a piece of input text, the conversational bot is able to generate a corresponding response. Models for building conversational bots can often be divided into retrieval-based models and generative models. A retrieval-based model that uses a database of predefined responses and some sort of heuristic inference to select the appropriate response based on input and context does not produce any new text, simply selecting a reply from a fixed set. Generative models, on the other hand, do not rely on predefined responses and generate new responses entirely from scratch.

l **Requirements**

1. Implement a dialogue generation algorithm 

2. Demo demonstration using GUI or web page 

3. Enter a sentence and give a corresponding reply

l **Paper recommendation**

... (It has nothing to do with this project and will not be displayed)

l **Dataset recommendation**

... (It has nothing to do with this project and will not be displayed)

## Goal

General-purpose models, such as ChatGPT, perform well in a wide range of scenarios but have some shortcomings in terms of specialization in the medical field. Medical conversations often involve complex medical knowledge and terminology, requiring an in-depth understanding of the patient’s symptoms, medical history, and more to provide accurate advice. Therefore, the goal of this experiment is to train a more professional "doctor model" by fine-tuning the general model, so that users can obtain more in-depth and professional medical diagnosis and advice. This model will have extensive medical knowledge, be able to understand the condition description provided by the patient, and provide users with targeted medical information.

## Result

In order to make our model have stronger practical value, we integrate multiple data sets for training. Generally speaking, online Q&A medical data sets are relatively extensive but cannot cover most medical problems, and the content is highly repetitive. For this, we propose a data collection and integration scheme that combines three data sets, aiming to learn from each other's strengths and enhance the model's medical dialogue capabilities.

![image](https://github.com/Summu77/chatbot/assets/115442864/d72f50cc-1f64-4060-931e-86eea009404a)


For details about the dataset, see the Dataset section. An example of the format of the dataset:

![image](https://github.com/Summu77/chatbot/assets/115442864/2d4a7493-ae74-4fa8-aaaa-6269d28d3e86)


ChatGPT generated data set case display：

(How to generate data through ChatGPT is described in the Datasets section.)

![image](https://github.com/Summu77/chatbot/assets/115442864/aed56278-d9a1-4c7e-9a2d-a95d2092e03c)


Before training, we observed the characteristics of the data. Dataset word cloud analysis:

![image](https://github.com/Summu77/chatbot/assets/115442864/53c19f0d-b494-4402-b9b3-cb5f7a81f2a8)


The effect of the fine-tuning model is displayed：

(The page of the model display is built based on the streamlit library.)

![image](https://github.com/Summu77/chatbot/assets/115442864/3db01754-e1a7-4d43-abae-40e68aa48e0f)


The above is only a partial display, please refer to our experiment report for details.

We provide a PDF version of the report for reference !

If there are any issues with the report, please contact us !

## Requirements

You can use Transformers to quickly deploy code and use PEFT for fine-tuning.

Network issues need to be solved by yourself, and you can pre-download the corresponding model in advance.

The second way is that you can deploy it through the github project of each model. Each model comes with fine-tuning code and tools, which makes it easy to fine-tune the model !

We provide a partially  environment, please be sure to use the latest environment of the corresponding github project !

- protobuf>=4.25.1  
- transformers>=4.36.2  
- cpm_kernels>=1.0.11  
- torch>=2.1.0  
- sentencepiece>=0.1.99
- streamlit\>=1.29.0
- fastapi\>=0.108.0 
- loguru∼0.7.2

In this project, most of the code is borrowed from the excellent projects of previous generations, so we do not provide code.

If you have any questions, please feel free to ask.

## Datasets

l **Chinese medical dialogue data  **

Chinese medical dialogue data: There are doctor-patient dialogues in six departments, namely: andrology (94596 question and answer pairs), internal medicine (220606 question and answer pairs), obstetrics and gynecology (183751 question and answer pairs) , Oncology (75553 Q&A pairs), Pediatrics (101602 Q&A pairs), Surgery 115991 Q&A pairs, total 792099 pieces of data.

l **CHIP-STS    **

Ping An Medical Technology's disease question and answer transfer learning data set is the second evaluation task in CHIP 2019. The main goal of this evaluation task is to conduct transfer learning between disease types based on Chinese disease question and answer data. In the real world, problems in the medical field involve a wide range of diseases and medical knowledge, thus placing higher requirements on the medical question and answer capabilities of large language models. This data set is designed to help models understand the connections between different diseases in order to better answer various medical-related questions.

l **Self-managed datasets    **

We try to reproduce the idea of the paper " Self-Instruct: Aligning Language Models with Self-Generated Instructions (Wang et al., ACL 2023) ", by calling the API of gpt-3.5-turbo-instruct and combining it with medical expertise to build structured data ourselves. set.

? If you have any questions about this, please refer to our lab report.

## More Info about Method

The content is still being created...

Please refer to the following link for the principle of model tuning.  [PEFT:微调总结 - Whu-Summu77](https://summu77.github.io/自然语言处理/常见的微调方法/)

Please refer to the following link for the principle of the related model. [常见大模型 - Whu-Summu77](https://summu77.github.io/自然语言处理/常见大模型原理/)

![image](https://github.com/Summu77/chatbot/assets/115442864/de65b74b-2fca-4df8-b123-cb92898a3bef)


We have elaborated in detail in the experiment report, so you can read it if you are interested!



