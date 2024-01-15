# chatbot
Natural Language Processing Group Assignment at Wuhan University

## 任务流程如下所示

![image](https://github.com/Summu77/chatbot/assets/115442864/ef125f8f-a108-4087-a01a-8884cf4066b4)

## 配置说明

### Chinese-Vicuna部署

参考资料：[Chinese-Vicuna](https://github.com/Facico/Chinese-Vicuna/blob/master/docs/readme-zh.md)
部署时间：2024年1月15日19:07🕞
硬件环境：RTX 3090(24GB) * 1

- 第一步：创建环境python==3.8
- 第二步：git clone 项目
- 第三步：pip install -r requirements.txt
> 注意：其中会出现两个不兼容的问题，请修改 requirements.txt 将相应包的指定版本号去掉，默认会自动匹配版本
- 第四步：修改generate.sh中的BASE_MODEL和LORA_PATH
> 注意：我们需要配置的是基于llama-7b的医疗对话模型Chinese-Vicuna-continue-finetune-7epoch-cMedQA2
>
> BASE_MODEL="huggyllama/llama-7b"
>
> LORA_PATH="Chinese-Vicuna/Chinese-Vicuna-continue-finetune-7epoch-cMedQA2"
