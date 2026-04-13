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
  "summary": "This poem was written in the spring of the fifth year of Yuanfeng of Emperor Shenzong of Song (1082 AD), when Su Shi was demoted to Huangzhou as a military assistant for the third spring due to the 'Wutai Poetry Case'.",
  "content": "#DingFengBo #SuShi #ThemeThought",
  "summary": "This poem is a work expressing feelings after getting drunk and encountering rain. The poet used the act of walking leisurely in the rain to show his stubborn character and open-mindedness despite being in adversity and facing repeated setbacks."
},
{
  "content": "#DingFengBo #SuShi #Appreciation #FirstLine",
  "summary": "The first line 'Do not listen to the sound of rain beating against the leaves', on one hand, depicts the stormy weather, and on the other, uses the words 'do not listen' to indicate that external things should not disturb one's mind."
},
...
```

## Model Inference

Below are examples of model inference, demonstrating the model's understanding and generation capabilities regarding "Ding Feng Bo":

```
Question: Ding Feng Bo
Answer: Ding Feng Bo · Do Not Listen to the Sound of Rain Beating Against the Leaves
This poem was written by Su Shi during his period of demotion, expressing his open-mindedness and transcendence in adversity. The line "Do not listen to the sound of rain beating against the leaves" is a vivid portrayal of an attitude of transcendence towards adversity.
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
   question = "Ding Feng Bo"
   answer = model.generate(question)
   print(answer)
   ```

## Contribution

Contributions to this project are welcome. Please submit PRs or Issues to improve the model or add more knowledge points.


## Contact

For any questions, please contact: TsangHaotian@hotmail.com

---

Thank you for your attention and support!
