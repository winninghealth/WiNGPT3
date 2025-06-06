## WiNGPT-3.0

\[[Report](https://arxiv.org/abs/2505.17387)\] \[[ZH](https://github.com/winninghealth/WiNGPT-3.0/blob/main/README-zh.md/)\]

WiNGPT is a large language model tailored for the medical field, designed to integrate professional medical knowledge, healthcare information, and data to provide intelligent medical Q&A, diagnostic support, and medical knowledge services, thereby enhancing the efficiency of diagnosis and treatment as well as the quality of medical services.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [How to Use](#how-to-use)
- [Training Process](#training-process)
- [Model Card](#model-card)
- [Evaluation](#evaluation)
- [Applications](#applications)
- [Limitations and Disclaimer](#limitations-and-disclaimer)
- [Contact Us](#contact-us)

## Introduction

To further enhance the capabilities of vertical domain large language models, we focus on four aspects: introducing long chains of reasoning to improve model inference ability, enhancing dataset quality during post-training, constructing datasets based on medical questions, and incorporating reinforcement learning methods.

## Features

- **Core Functions**

  - **Enhanced Medical Reasoning**: Improves structured and verifiable clinical reasoning capabilities through multi-stage training (supervised fine-tuning + reinforcement learning) and a Long Chain-of-Thought (Long CoT) dataset.
  - **Deep Integration with Medical Systems**: Seamlessly embeds into hospital workflows (e.g., WiNEX system), offering physician review, structured knowledge base support, and customizable rule templates to ensure clinical applicability and compliance.
  
- **Main Features**

  - **Efficient Parameter Scale & Training**: Built on the 32B-parameter Qwen-2.5 architecture, balancing performance and deployment feasibility via multi-stage training (general reasoning → medical alignment → clinical reinforcement).
  - **Evidence-Driven Knowledge Fusion**: Combines evidence chain simulation (e.g., diagnostic process emulation) with knowledge base retrieval mechanisms to reduce model hallucinations and enhance answer traceability and clinical reliability.
  - **Iterative Optimization**: Continuously collects and learns the latest medical research to continuously improve model performance and system functionality.

## How to Use

[Apply for a key through the WiNGPT test platform or contact us](https://wingpt.winning.com.cn/)

## Training Process

<img src="https://github.com/user-attachments/assets/fa236a78-7b55-45ef-8259-d14b69d48bf0" alt="Description Text" style="width:50%;"/>

## Model Card

- Model Parameters: 32B
- Precision: BF16
- Context Length: 24576

## Evaluation

| Model                        | CMMLU     |  Math500  |  MedCalc  | MedReMCQ | MedQA-USLME | MedMCQA  | **PubMedQA** |
| ---------------------------- | --------- | :-------: | :-------: | -------- | :---------: | :------- | ------------ |
| DeepSeek-R1-Distill-Qwen-32B | 83.02     |   96.32   |   57.70   | 65.3     |    81.85    | 65.5     | 76.1         |
| OpenThinker2-32B             | 86.15     |   96.64   |   58.52   | 68.8     |    85.07    | 68.7     | 78.0         |
| Light-R1-32B-DS              | 86.21     |   97.20   |   48.74   | 70.3     |    83.74    | 67.9     | 76.2         |
| QwQ-32B                      | **87.43** | **97.48** |   51.37   | 73.5     |  **85.78**  | 71.2     | 77.9         |
| WiNGPT-3.0-S3                | 85.07     |   93.96   | **66.63** | **74.7** |    85.70    | 69.9     | **78.2**     |
| WiNGPT-3.0-S3-Merged         | 86.1      |   95.6    |   66.2    | 74.0     |  **87.1**   | **71.6** | 78.0         |

## Applications

### 1. Patient Recruitment

<details><summary>Clinical trials have complex inclusion and exclusion criteria; use WiNGPT to automatically screen patients in databases for eligibility.</summary><img src="https://github.com/user-attachments/assets/61962411-7a3f-4296-957d-c56d5b4117c3"/></details>

### 2. Clinical Diagnostic Reasoning

<details><summary>Simulate clinical diagnostic reasoning—diagnostic assistance.</summary>
<img src="https://github.com/user-attachments/assets/24e37279-4652-48be-992e-3e58ac19c04b"/>
</details>

### 3. MedEvidence

<details><summary>Evidence-Based Search Integration.</summary>
  <img src="https://github.com/user-attachments/assets/d94738a9-d5d3-4267-86f4-ff39404a4840"/>
</details>

## Limitations and Disclaimer

(a) WiNGPT-3.0 is a professional medical domain large language model that can provide general users with humanized AI doctor consultation and Q&A functions, as well as general medical knowledge Q&A. For professional medical personnel, WiNGPT-3.0 offers suggestions regarding patient conditions, diagnoses, medication, and health advice for reference only.

(b) You should understand that WiNGPT-3.0 provides information and suggestions and cannot replace the opinions, diagnoses, or treatment recommendations of medical professionals. Before using information from WiNGPT-3.0, please seek advice from a doctor or other medical professional and independently evaluate the provided information.

(c) Information from WiNGPT-3.0 may contain errors or inaccuracies. Winning Health makes no express or implied warranties regarding the accuracy, reliability, completeness, quality, safety, timeliness, performance, or applicability of WiNGPT-3.0. The results and decisions arising from the use of WiNGPT-3.0 are borne by you. Third-party causes resulting in damage are not covered.

## Citation

```bibtex
@article{zhuang2025wingpt,
  title={WiNGPT-3.0 Technical Report},
  author={Zhuang, Boqin and Song, Chenxiao and Lu, Huitong and Qiao, Jiacheng and Liu, Mingqian and Yu, Mingxing and Hong, Ping and Li, Rui and Song, Xiaoxia and Xu, Xiangjun and others},
  journal={arXiv preprint arXiv:2505.17387},
  year={2025}
}
```

## Contact Us

Website: https://www.winning.com.cn

Email: wair@winning.com.cn
