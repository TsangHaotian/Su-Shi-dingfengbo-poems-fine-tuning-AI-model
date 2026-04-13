# Su-Shi-Dingfengbo-Poems-Fine-Tuning-AI-Model

## Introduction

This project introduces an AI large model fine-tuned based on 168 knowledge points from "Ding Feng Bo" (定风波). The model aims to understand and generate text content related to "Ding Feng Bo," providing in-depth poetry analysis and creative capabilities.

## Model Architecture

- **Model Name**: DeepSeek-LLM-7B-Chat
- **Training Data**: 168 knowledge points of "Ding Feng Bo"
- **Training Framework**: LlamaFactory
- **Training Date**: April 21, 2025

## Training Process

### Training Loss Graph
![5b7eb732f41e7a9693021489bb76120](https://github.com/user-attachments/assets/464b350e-2e23-47a5-8976-5a6df1d70c44)

### Training Result Run Graph
<img width="1067" alt="41f5f573cee062530e41cef9e9f32c7" src="https://github.com/user-attachments/assets/e14c99e5-8d63-4466-b038-55e52a388d1e" />
### Training Logs

Below are excerpts from the training logs, showing key metrics such as loss, learning rate, and gradient norm:

```
INFO[2025-04-21 13:43:13] llamafactory.train.callbacks:143 >> {'loss': 0.9834, 'learning_rate': 1.3581e-04, 'epoch': 1.54, 'throughput': 5.25}
INFO[2025-04-21 13:45:57] llamafactory.train.callbacks:143 >> {'loss': 0.9444, 'learning_rate': 1.2021e-04, 'epoch': 1.67, 'throughput': 37.22}
...
```

## Training Data

The training data includes 168 knowledge points related to "Ding Feng Bo," covering poetry appreciation, background knowledge, author introduction, and more. Here are some example data entries:

```json
{
  "summary": "这首词作于宋神宗元丰五年（公元1082年）春，当时是苏轼因“乌台诗案”被贬为黄州团练副使的第三个春天。",
  "content": "#定风波 #苏轼#主题思想",
  "summary": "此词为醉归遇雨抒怀之作。词人借雨中潇洒徐行之举动，表现了虽处逆境屡遭挫折而不畏惧不颓丧的倔强性格和旷达胸怀。"
},
...
{
  "content": "#定风波 #苏轼#赏析 #首句",
  "summary": "首句“莫听穿林打叶声”，一方面渲染出雨骤风狂，另一方面又以“莫听”二字点明外物不足萦怀之意。"
},
```

## Model Inference

Below are examples of model inference, demonstrating the model's understanding and generation capabilities regarding "Ding Feng Bo":

```
问题: 定风波
回答: 定风波·莫听穿林打叶声
这首词是苏轼在贬谪时期所作，表达了他在逆境中的豁达与超然。诗中的“莫听穿林打叶声”一句，是对逆境的超然态度的生动写照。
```

## Model Performance

The model demonstrated good convergence during training, with the loss value gradually decreasing from an initial 2.0 to around 0.3, indicating significant progress in understanding and generating content related to "Ding Feng Bo."

## Usage Instructions

1. **Install Dependencies**:
   ```bash
   pip install llamafactory transformers
   ```

2. **Load Model**:
   ```python
   from llamafactory import LLMFactory

   factory = LLMFactory()
   model = factory.load_model("path/to/your/model")
   ```

3. **Perform Inference**:
   ```python
   question = "定风坡"
   answer = model.generate(question)
   print(answer)
   ```

## Contribution

Contributions to this project are welcome. Please submit PRs or Issues to improve the model or add more knowledge points.


## Contact

For any questions, please contact: TsangHaotian@hotmail.com

---

Thank you for your attention and support!
