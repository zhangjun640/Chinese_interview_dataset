# Chinese_interview_dataset: A High-Quality Chinese Interview Question Dataset

[![Hugging Face Datasets](https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-Datasets-yellow)](https://huggingface.co/datasets?search=zhangjun640/Chinese_interview)
[![License: Apache 2.0](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

Hello everyone, I'm excited to introduce the **High-Quality Chinese Interview Dataset** that I have compiled and open-sourced.

This is a comprehensive dataset designed to support fine-tuning Large Language Models (LLMs), interview preparation, and Natural Language Processing research. All data is sourced from top-tier Chinese job-seeking and technical communication platforms like **Nowcoder (牛客网) and CSDN**, ensuring the authenticity, timeliness, and broad coverage of the questions.

---

### Dataset Links

To meet the needs of various computational resources and application scenarios, I have provided three versions of the dataset with different sizes:

* **Small(16.1K)**: 
    * [🤗 zhangjun640/Chinese_interview_small](https://huggingface.co/datasets/zhangjun640/Chinese_interview_small)
* **Medium(59K)**:
    * [🤗 zhangjun640/Chinese_interview_medium](https://huggingface.co/datasets/zhangjun640/Chinese_interview_medium)
* **Large(158K)**:
    * [🤗 zhangjun640/Chinese_interview_large](https://huggingface.co/datasets/zhangjun640/Chinese_interview_large)

### ✨ Key Features

* **Driven by Real Scenarios**: All question-answer pairs are meticulously collected and curated from real interview scenarios and technical discussions, avoiding "toy data" to address real-world challenges.
* **Multiple Scales**: Available in Small, Medium, and Large versions, allowing users to flexibly choose based on their computing power, time constraints, and model size. Whether for quick validation or pursuing maximum performance, there is a suitable version.
* **Broad Domain Coverage**: The dataset covers core knowledge points across popular technical fields such as Computer Science, Software Engineering, Data Science, and Algorithms.
* **Optimized for Chinese**: The content is natively in Chinese, conforming to Chinese linguistic context and technical expression habits, making it excellent corpus for fine-tuning Chinese language models.

### Data Format

The dataset follows the standard instruction fine-tuning format, containing fields like `instruction`, `input`, and `output`. This format can be seamlessly integrated into most mainstream LLM fine-tuning frameworks.

Here is a data sample:

```json
{
  "instruction": "请解释一下什么是TCP的“三次握手”过程？ (Please explain the TCP 'Three-Way Handshake' process?)",
  "input": "",
  "output": "TCP的“三次握手”是建立一个TCP连接时，客户端和服务器之间总共发送三个包的确认过程。具体步骤如下：..."
}
```

### How to Use

**Note:** Accessing this dataset may require you to be logged into your Hugging Face account. You can log in via the command line:
```bash
huggingface-cli login
```

#### Using the `datasets` Library (Recommended)
This is the standard way to load and interact with the dataset for training models.

```python
from datasets import load_dataset

# Login using e.g. `huggingface-cli login` to access this dataset
ds = load_dataset("zhangjun640/Chinese_interview_small")

# Print dataset information
print(ds)

# View the first sample
print(ds['train'][0])
```

#### Using `pandas` to Load Raw Files
This method is useful for quick data analysis or if you want to load a specific file directly into a pandas DataFrame.

```python
import pandas as pd

# Define the path to a specific file in the dataset repository
file_path = "hf://datasets/zhangjun640/Chinese_interview_small/qa_dataset_part2_new.json"

# Login using e.g. `huggingface-cli login` to access this dataset
df = pd.read_json(file_path)

# Display the first few rows of the DataFrame
print(df.head())
```

### 🌟 Use Cases

* **LLM Fine-tuning**: Use as a high-quality instruction dataset to fine-tune Chinese language models.
* **Interview Preparation Tools**: Develop AI interviewers, intelligent chatbots, etc.
* **Information Retrieval and Q&A Systems**: Build an intelligent system capable of accurately answering technical interview questions.
* **NLP Academic Research**: For research in areas such as dialogue systems and text generation.

### Citation

If you use this dataset in your research or work, please consider citing it:

```bibtex
@misc{zhangjun640_chinese_interview,
  author = {zhangjun640},
  title = {Chinese Interview Dataset},
  year = {2025},
  publisher = {Hugging Face},
  journal = {Hugging Face repository},
  howpublished = {\url{[https://huggingface.co/datasets/zhangjun640/Chinese_interview_large](https://huggingface.co/datasets/zhangjun640/Chinese_interview_large)}},
}
```

### License

This dataset is licensed under the [Apache License 2.0](https://opensource.org/licenses/Apache-2.0).

---
---

# Chinese_interview_dataset: 高质量中文面试问题数据集

[![Hugging Face Datasets](https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-Datasets-yellow)](https://huggingface.co/datasets?search=zhangjun640/Chinese_interview)
[![License: Apache 2.0](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

大家好，非常荣幸向大家介绍我整理并开源的**高质量中文面试问题数据集 (Chinese Interview Dataset)**。

这是一个旨在为大型语言模型（LLM）微调、面试准备、以及自然语言处理研究提供支持的综合性数据集。所有数据均源自中文互联网头部求职与技术交流平台，如**牛客网、CSDN**等，确保了问题的真实性、时效性和覆盖面。

---

### 数据集链接

为了满足不同计算资源和应用场景的需求，我提供了三种不同规模的数据集：

* **Small (小型版)**: 
    * [🤗 zhangjun640/Chinese_interview_small](https://huggingface.co/datasets/zhangjun640/Chinese_interview_small)
* **Medium (中型版)**:
    * [🤗 zhangjun640/Chinese_interview_medium](https://huggingface.co/datasets/zhangjun640/Chinese_interview_medium)
* **Large (大型版)**:
    * [🤗 zhangjun640/Chinese_interview_large](https://huggingface.co/datasets/zhangjun640/Chinese_interview_large)

### ✨ 数据集特色

* **真实场景驱动**: 所有问答对均从真实的面试场景和技术讨论中精心收集和整理，拒绝“玩具数据”，直面真实世界的挑战。
* **多规模选择**: 提供 Small, Medium, Large 三种版本，方便用户根据自身算力、时间和模型规模灵活选择。
* **领域覆盖广泛**: 数据集涵盖了计算机科学、软件工程、数据科学、算法等多个热门技术领域的核心知识点。
* **专为中文优化**: 数据内容原生为中文，符合中文语境和技术表达习惯，是微调中文语言模型的绝佳语料。

### 数据格式

本数据集遵循标准的指令微调格式，包含 `instruction`, `input`, 和 `output` 等字段。这种格式可以无缝对接到大多数主流的 LLM 微调框架中。

一个数据样例如下：

```json
{
  "instruction": "请解释一下什么是TCP的“三次握手”过程？",
  "input": "",
  "output": "TCP的“三次握手”是建立一个TCP连接时，客户端和服务器之间总共发送三个包的确认过程。具体步骤如下：..."
}
```

### 如何使用

**请注意：** 访问此数据集可能需要您登录 Hugging Face 账户。您可以使用以下命令在终端登录：
```bash
huggingface-cli login
```

#### 使用 `datasets` 库 (推荐)
这是加载和处理数据集以用于模型训练的标准方法。

```python
from datasets import load_dataset

# 使用 huggingface-cli login 等方式登录后，即可访问此数据集
ds = load_dataset("zhangjun640/Chinese_interview_small")

# 打印数据集信息
print(ds)

# 查看第一条样本
print(ds['train'][0])
```

#### 使用 `pandas` 加载原始文件
如果您想进行快速的数据分析，或希望将某个特定文件直接加载到 pandas DataFrame 中，可以使用此方法。

```python
import pandas as pd

# 定义数据集中某个特定文件的路径
file_path = "hf://datasets/zhangjun640/Chinese_interview_small/qa_dataset_part2_new.json"

# 使用 huggingface-cli login 等方式登录后，即可访问此数据集
df = pd.read_json(file_path)

# 显示 DataFrame 的前几行
print(df.head())
```

### 🌟 应用场景

* **LLM 微调**: 作为高质量的指令数据集，用于微调中文语言模型。
* **面试准备工具**: 开发AI面试官、智能问答机器人等。
* **信息检索与问答系统**: 构建一个能够精准回答技术面试问题的智能系统。
* **NLP学术研究**: 用于对话系统、文本生成等相关领域的研究。

### 引用

如果您在您的研究或工作中使用了本数据集，请考虑引用：

```bibtex
@misc{zhangjun640_chinese_interview,
  author = {zhangjun640},
  title = {Chinese Interview Dataset},
  year = {2025},
  publisher = {Hugging Face},
  journal = {Hugging Face repository},
  howpublished = {\url{[https://huggingface.co/datasets/zhangjun640/Chinese_interview_large](https://huggingface.co/datasets/zhangjun640/Chinese_interview_large)}},
}
```

### 许可证

本数据集采用 [Apache License 2.0](https://opensource.org/licenses/Apache-2.0) 许可证。
