# Su-Shi-dingfengbo-poems-fine-tuning-AI-model

## 简介

本项目介绍了一个基于《定风波》168个知识点微调训练的AI大模型。该模型旨在理解和生成与《定风波》相关的文本内容，提供深入的诗词分析和创作能力。

## 模型架构

- **模型名称**: DeepSeek-LLM-7B-Chat
- **训练数据**: 168个《定风波》知识点
- **训练框架**: LlamaFactory
- **训练时间**: 2025年4月21日

## 训练过程

### 训练损失图
![5b7eb732f41e7a9693021489bb76120](https://github.com/user-attachments/assets/464b350e-2e23-47a5-8976-5a6df1d70c44)

### 训练结果运行图
<img width="1067" alt="41f5f573cee062530e41cef9e9f32c7" src="https://github.com/user-attachments/assets/e14c99e5-8d63-4466-b038-55e52a388d1e" />


### 训练日志

以下是部分训练日志，展示了损失值、学习率、梯度范数等关键指标：

```
INFO[2025-04-21 13:43:13] llamafactory.train.callbacks:143 >> {'loss': 0.9834, 'learning_rate': 1.3581e-04, 'epoch': 1.54, 'throughput': 5.25}
INFO[2025-04-21 13:45:57] llamafactory.train.callbacks:143 >> {'loss': 0.9444, 'learning_rate': 1.2021e-04, 'epoch': 1.67, 'throughput': 37.22}
...
```

## 训练数据

训练数据包含《定风波》相关的168个知识点，涵盖诗词赏析、背景知识、作者介绍等多个方面。以下是部分示例数据：

```json
{
  "summary": "这首词作于宋神宗元丰五年（公元1082年）春，当时是苏轼因“乌台诗案”被贬为黄州团练副使的第三个春天。",
  "content": "#定风波 #苏轼#主题思想",
  "summary": "此词为醉归遇雨抒怀之作。词人借雨中潇洒徐行之举动，表现了虽处逆境屡遭挫折而不畏惧不颓丧的倔强性格和旷达胸怀。"
},
{
  "content": "#定风波 #苏轼#赏析 #首句",
  "summary": "首句“莫听穿林打叶声”，一方面渲染出雨骤风狂，另一方面又以“莫听”二字点明外物不足萦怀之意。"
},
...
```

## 模型推理

以下是模型推理的示例，展示了模型对《定风波》的理解和生成能力：

```
问题: 定风波
回答: 定风波·莫听穿林打叶声
这首词是苏轼在贬谪时期所作，表达了他在逆境中的豁达与超然。诗中的“莫听穿林打叶声”一句，是对逆境的超然态度的生动写照。
```

## 模型性能

模型在训练过程中表现出良好的收敛性，损失值从初始的2.0逐渐下降到0.3左右，表明模型在理解和生成《定风波》相关内容方面取得了显著进展。

## 使用方法

1. **安装依赖**:
   ```bash
   pip install llamafactory transformers
   ```

2. **加载模型**:
   ```python
   from llamafactory import LLMFactory

   factory = LLMFactory()
   model = factory.load_model("path/to/your/model")
   ```

3. **进行推理**:
   ```python
   question = "定风波"
   answer = model.generate(question)
   print(answer)
   ```

## 贡献

欢迎对本项目进行贡献，提交PR或Issue以改进模型或添加更多知识点。

## 许可证

本项目采用MIT许可证，详见LICENSE文件。

## 联系方式

如有任何问题，请联系：TsangHaotian@hotmail.com

---

感谢您的关注和支持！
