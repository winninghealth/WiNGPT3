## WiNGPT-3.0

\[[Report](https://arxiv.org/abs/2505.17387)\] \[[EN](https://github.com/winninghealth/WiNGPT3/blob/main/README.md/)\]

WiNGPT是一个医疗垂直领域大模型，旨在将专业的医学知识、医疗信息、数据融会贯通，为医疗行业提供智能化的医疗问答、诊断支持和医学知识等信息服务，提高诊疗效率和医疗服务质量。

## 目录

- [介绍](#介绍)
- [特点](#特点)
- [如何使用](#如何使用)
- [训练流程](#训练流程)
- [模型卡](#模型卡)
- [评测](#评测)
- [应用](#应用)
- [局限性与免责声明](#局限性与免责声明)
- [联系我们](#联系我们)

## 介绍

为了进一步提升垂直领域大语言模型的能力，我们在四个方面进行增强：引入长思维链增加模型推理能力，提升后训练过程中数据集质量，基于医学的问题构建数据集以及引入强化学习的方法。


## 特点

- **核心功能**
  - **医疗推理增强**：通过多阶段训练（监督微调+强化学习）和长链思维（Long CoT）数据集，提升结构化、可验证的临床推理能力。
  - **深度集成医疗系统**：无缝嵌入医院工作流（如WiNEX系统），提供医生审核、结构化知识库支持及可定制规则模板，确保临床适用性与合规性。
- **主要特点**
  - **高效参数规模与训练**：基于32B参数的Qwen-2.5架构，通过多阶段训练（通用推理→医疗对齐→临床强化）平衡性能与部署可行性。
  - **证据驱动与知识融合**：整合证据链模拟（如诊断流程仿真）与知识库检索机制，减少模型幻觉，提升回答的可追溯性和临床可靠性。
  - **迭代优化**：持续搜集和学习最新的医学研究，不断提高模型性能和系统功能。

## 如何使用

[通过WiNGPT测试平台申请密钥或与我们取得联系](https://wingpt.winning.com.cn/)

## 训练流程

<img src="https://github.com/user-attachments/assets/fa236a78-7b55-45ef-8259-d14b69d48bf0" alt="描述文字" style="width:50%;"/>

## 模型卡
 - 模型参数  32B
 - 精度 bf16
 - 上下文长度  24576

## 评测

| Model                        | CMMLU     |  Math500  |  MedCalc  | MedReMCQ | MedQA-USLME | MedMCQA  | **PubMedQA** |
| ---------------------------- | --------- | :-------: | :-------: | -------- | :---------: | :------- | ------------ |
| DeepSeek-R1-Distill-Qwen-32B | 83.02     |   96.32   |   57.70   | 65.3     |    81.85    | 65.5     | 76.1         |
| OpenThinker2-32B             | 86.15     |   96.64   |   58.52   | 68.8     |    85.07    | 68.7     | 78.0         |
| Light-R1-32B-DS              | 86.21     |   97.20   |   48.74   | 70.3     |    83.74    | 67.9     | 76.2         |
| QwQ-32B                      | **87.43** | **97.48** |   51.37   | 73.5     |  **85.78**  | 71.2     | 77.9         |
| WiNGPT-3.0-S3                | 85.07     |   93.96   | **66.63** | **74.7** |    85.70    | 69.9     | **78.2**     |
| WiNGPT-3.0-S3-Merged         | 86.1      |   95.6    |   66.2    | 74.0     |  **87.1**   | **71.6** | 78.0         |

## 应用

### 1. 患者招募

<details><summary>临床实验有复杂的入组和排除标准，通过WiNGPT自动对数据库中的患者进行纳排。</summary><img src="https://github.com/user-attachments/assets/61962411-7a3f-4296-957d-c56d5b4117c3"/></details>

### 2. 临床诊断推理

<details><summary>模拟临床诊断推理-诊断辅助。</summary>
<img src="https://github.com/user-attachments/assets/24e37279-4652-48be-992e-3e58ac19c04b"/>
</details>

### 3. MedEvidence


<details><summary>基于证据的医学信息检索。</summary>
  <img src="https://github.com/user-attachments/assets/d94738a9-d5d3-4267-86f4-ff39404a4840"/>
</details>

## 局限性与免责声明

(a) WiNGPT-3.0 是一个专业医疗领域的大语言模型，可为一般用户提供拟人化AI医生问诊和问答功能，以及一般医学领域的知识问答。对于专业医疗人士，WiNGPT-3.0 提供关于患者病情的诊断、用药和健康建议等方面的回答的建议仅供参考。

(b) 您应理解 WiNGPT-3.0 仅提供信息和建议，不能替代医疗专业人士的意见、诊断或治疗建议。在使用 WiNGPT-3.0 的信息之前，请寻求医生或其他医疗专业人员的建议，并独立评估所提供的信息。

(c) WiNGPT-3.0 的信息可能存在错误或不准确。卫宁健康不对 WiNGPT-3.0 的准确性、可靠性、完整性、质量、安全性、及时性、性能或适用性提供任何明示或暗示的保证。使用 WiNGPT-3.0 所产生的结果和决策由您自行承担。第三方原因而给您造成的损害结果承担责任。

## 引用

```bibtex
@article{zhuang2025wingpt,
  title={WiNGPT-3.0 Technical Report},
  author={Zhuang, Boqin and Song, Chenxiao and Lu, Huitong and Qiao, Jiacheng and Liu, Mingqian and Yu, Mingxing and Hong, Ping and Li, Rui and Song, Xiaoxia and Xu, Xiangjun and others},
  journal={arXiv preprint arXiv:2505.17387},
  year={2025}
}
```

## 联系我们

网站：https://www.winning.com.cn

邮箱：wair@winning.com.cn
