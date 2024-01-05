# LLMPapers
包含当前自己能收集到的LLM的论文以及相关代码和演示demo路径。持续更新中。
# Instruct-Imagen: Image Generation with Multi-modal Instruction
谷歌最新发布的Instruct-Imagen：使用多模态指令生成图像
### 简介
这是一种处理异构图像生成任务并推广看不见的任务的模型。我们引入了用于图像生成的*多模态指令*，这是一种精确地表达一系列生成意图的任务表示。它使用自然语言来合并不同的模态（例如，文本、边缘、样式、主题等），以便可以以统一的格式标准化丰富的生成意图。然后，我们通过使用两阶段框架微调预训练的文本到图像扩散模型来构建 instruct-imagen。首先，我们使用检索增强训练来调整模型，以增强模型的能力，使其生成基于外部多模态上下文。随后，我们对需要视觉语言理解的各种图像生成任务（例如，主题驱动生成等）进行了调整模型的微调，每个任务都与封装任务本质的多模态指令配对。对各种图像生成数据集的人工评估表明，instruct-imagen 在域内匹配或超越了先前特定于任务的模型，并展示了对看不见和更复杂任务的有前途的泛化。
### 代码地址（暂未发布）

# LLaMA Pro: Progressive LLaMA with Block Expansion
腾讯发布LLaMA Pro：具有模块化扩展功能的渐进式 LLaMA
### 简介
人类通常会在不妥协旧技能的情况下获得新技能;然而，大型语言模型（LLM）则相反，例如，从LLaMA到CodeLLaMA。为此，我们提出了一种新的LLM后预训练方法，并扩展了Transformer模块。我们只使用新的语料库来调整扩展的块，有效地提高模型的知识，而不会发生灾难性的遗忘。在本文中，我们在代码和数学语料库上进行了实验，产生了LLaMA Pro-8.3B，这是一个从LLaMA2-7B初始化的通用基础模型，在一般任务、编程和数学方面表现出色。LLaMA Pro及其指令遵循对应物（LLaMA Pro-Instruct）在各种基准测试中实现了先进的性能，展示了优于LLaMA系列中现有的开放模型，以及作为智能代理推理和处理各种任务的巨大潜力。我们的研究结果为集成自然语言和编程语言提供了宝贵的见解，为开发在各种环境中有效运行的高级语言代理奠定了坚实的基础。
### 代码地址（未发布代码，静候中...)
https://github.com/TencentARC/LLaMA-Pro

# TinyLlama: An Open-Source Small Language Model
TinyLlama：开源小型语言模型
### 简介
译文：我们提出了TinyLlama，一个紧凑的11亿语言模型，在大约3个时代的大约1万亿个token上进行了预训练。TinyLlama以Llama 2 (Touvron等人，2023b)的架构和标记器为基础，利用开源社区贡献的各种进步(例如，FlashAttention (Dao, 2023))，实现更好的计算效率。尽管它的体积相对较小，但TinyLlama在一系列下游任务中表现出色。它的性能明显优于现有同等大小的开源语言模型。
### 代码地址
https://github.com/jzhang38/TinyLlama

# ODIN: A Single Model for 2D and 3D Perception
Microsoft、斯坦福大学和CMU推出： ODIN: 用于 2D 和 3D 感知的单一模型
### 简介
ScanNet 等当代 3D 感知基准上的先进模型使用并标记数据集提供的 3D 点云，这些点云是通过对感知的多视图 RGB-D 图像进行后处理获得的。它们通常在域内进行训练，放弃了大规模的 2D 预训练，并且优于以 RGB-D 多视图图像为特色的替代方案。使用摆图的方法与后处理的 3D 点云之间的性能差距促使人们相信 2D 和 3D 感知需要不同的模型架构。在本文中，我们挑战了这一观点，并提出了ODIN（Omni-Dimensional INstance segmentation），该模型可以使用在2D内视图和3D跨视图信息融合之间交替的Transformer架构，对2D RGB图像和3D点云进行分割和标记。我们的模型通过所涉及的令牌的位置编码来区分 2D 和 3D 特征操作，这些编码捕获 2D 面片令牌的像素坐标和 3D 特征令牌的 3D 坐标。ODIN 在 ScanNet200、Matterport3D 和 AI2THOR 3D 实例分割基准测试中实现了最先进的性能，并在 ScanNet、S3DIS 和 COCO 上实现了具有竞争力的性能。当使用感应的 3D 点云代替从 3D 网格采样的点云时，它的性能远远优于以前的所有作品。当在可指导的具身智能体架构中用作 3D 感知引擎时，它在 TEACh 对话中的动作基准上设定了新的最先进的技术。
### 代码地址
https://odin-seg.github.io

# LLaVA-φ: Efficient Multi-Modal Assistant with Small Language Model
LLaVA-φ：基于小语言模型的高效多模态助手
### 简介
我们介绍了LLaVA-phi (LLaVA-phi)，一个高效的多模态助手，它利用了最近先进的小型语言模型Phi-2的功能来促进多模态对话。LLaVA-Phi标志着紧凑型多模态模型领域的显著进步。它表明，即使是更小的语言模型，只有2.7个参数，也可以有效地参与整合文本和视觉元素的复杂对话，只要他们接受过高质量语料库的培训。我们的模型在包括视觉理解、推理和基于知识的感知在内的公开基准上提供了值得称赞的性能。除了在多模态对话任务中的出色表现外，我们的模型还为需要实时交互的时间敏感环境和系统(如具身代理)中的应用开辟了新的途径。它强调了较小的语言模型在保持更高的资源效率的同时实现复杂级别的理解和交互的潜力。
### 代码地址
https://github.com/zhuyiche/llava-phi
