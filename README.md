# 医学影像与深度学习交叉方向 -- 顶刊论文全流程写作模板

> **适用范围**：IEEE TMI、Medical Image Analysis、NeuroImage、IEEE JBHI、MICCAI 等中科院一区/二区医学影像领域期刊及会议**写作语言**：英文（模板以英文句式为主，注释说明为中文）**核心原则**：严谨学术、规避口语化、逻辑递进、证据驱动

* * *

# 模块一：Abstract

## 1.1 写作框架指引

    【必备写作要点】
    - 全文控制在 200-250 词（期刊）或 150-200 词（会议）
    - 覆盖：疾病/任务背景 → 现有方法不足 → 本文方法概述 → 关键技术细节 → 实验验证结果
    - 不引用参考文献、不使用缩写首次出现不加括号全称
    - 避免主观评价词（如 "very", "extremely"），使用客观量化表述
    
    【核心覆盖内容】
    ① 临床问题/疾病的严重性与诊断需求
    ② 现有技术在该任务上的关键瓶颈（2-3 个要点）
    ③ 本文方法的名称、核心思想与整体架构
    ④ 关键模块/创新点的具体描述（2-3 个步骤）
    ⑤ 在公开数据集上的定量验证结果（准确率、AUC 等）
    
    【写作逻辑顺序】
    Background（1-2 句）→ However（1-2 句）→ To address（1 句）→ Specifically（2-3 句）→ Results（1-2 句）

## 1.2 完整可复用模板

> **句式功能标注**：`[BG]` = 背景句 | `[PB]` = 问题句 | `[MT]` = 方法句 | `[DT]` = 细节句 | `[RS]` = 结果句

    [BG] [Target disease/condition] is an [irreversible/prevalent/crucial/progressive] [disease type] that affects [affected population/organ], and its [early/accurate] diagnosis is of paramount importance for [clinical benefit, e.g., timely intervention/improved prognosis].
    
    [BG] [Imaging modality, e.g., structural MRI/PET/CT] has emerged as a promising [imaging technique/modality] for [clinical task, e.g., detecting biomarkers/assessing disease severity], providing [specific information, e.g., morphological/functional/metabolic] insights into [pathological changes].
    
    [PB] However, the inherent [variability/heterogeneity/complexity] of [data characteristic, e.g., multimodal imaging data/lesion appearances] and the [limited/scarcity] of [resource, e.g., annotated samples/clinical prior knowledge] significantly hinder the [performance/efficacy/generalizability] of existing [method category, e.g., conventional deep learning approaches/single-modality methods].
    
    [PB] Moreover, most current methods [specific limitation, e.g., overlook the complementary information across modalities/fail to model long-range spatial dependencies/lack interpretability in clinical decision-making], which limits their [practical utility/clinical applicability].
    
    [MT] To address these challenges, we propose a novel [method name], a [framework type, e.g., multi-modal fusion framework/generative adversarial network/hybrid learning architecture] for [task, e.g., early diagnosis of Alzheimer's disease/synthetic medical image generation].
    
    [DT] Specifically, we first [design/propose/introduce] a [module name A], which effectively [captures/extracts/fuses] [feature type, e.g., cross-modal complementary features/hierarchical spatial-temporal representations] via [technical mechanism, e.g., attention-guided convolution/probabilistic state transition]. Next, a [module name B] is developed to [function, e.g., model the non-linear relationships between modalities/enhance the discriminative power of feature representations]. Based on [module B], we further propose a [module name C] that [function, e.g., adaptively weights the contribution of each modality/provides clinically interpretable attention maps].
    
    [DT] The proposed [method name] seamlessly integrates [key components] into an [end-to-end/trainable] framework, enabling [overall advantage, e.g., robust multi-modal feature learning/clinically reliable predictions].
    
    [RS] Extensive experiments on [dataset name(s), e.g., ADNI/OASIS/BraTS] demonstrate that our method achieves [specific metric, e.g., an accuracy of XX.X% / an AUC of 0.XXX], outperforming [comparison scope, e.g., state-of-the-art methods/several representative baselines] by [improvement, e.g., X.X% in accuracy / X.X% in AUC].
    
    [RS] This article not only provides [contribution 1, e.g., a principled framework for multi-modal medical image analysis] but also offers [contribution 2, e.g., interpretable diagnostic evidence for clinical decision support].

## 1.3 高频专业句式库

| 功能  | 句式模板 | 适用场景 |
| --- | --- | --- |
| 背景句 | `X is an irreversible/prevalent/crucial/progressive Y that affects Z, and its early diagnosis is of paramount importance for W.` | 疾病/任务背景引入 |
| 背景句 | `[Modality] has emerged as a promising imaging technique for [task], providing [information type] insights into [pathology].` | 成像模态介绍 |
| 问题句 | `However, the inherent variability of [data] and the limited availability of [resource] significantly hinder the performance of existing approaches.` | 现有方法不足 |
| 问题句 | `Moreover, most current methods [limitation], which limits their clinical applicability.` | 补充局限 |
| 方法句 | `To address these challenges, we propose a novel [method], a [framework type] for [task].` | 方法引入 |
| 细节句 | `Specifically, we first [step 1]. Next, [step 2]. Based on [step 2], [step 3] is proposed.` | 技术细节展开 |
| 细节句 | `A novel [module] is proposed to effectively capture/identify [feature] via [mechanism].` | 模块功能描述 |
| 结果句 | `Extensive experiments on [dataset] demonstrate that our method achieves [metric], outperforming state-of-the-art methods by [improvement].` | 实验验证 |
| 结果句 | `This article not only provides [C1] but also offers [C2].` | 贡献总结 |

## 1.4 完整填表示例

> **示例场景**：基于多模态 MRI 的阿尔茨海默病早期诊断方法（虚构方法 "MMF-Net"）

    Alzheimer's disease (AD) is an irreversible neurodegenerative disorder that affects millions of elderly individuals worldwide, and its early diagnosis is of paramount importance for timely intervention and improved prognosis. Structural magnetic resonance imaging (sMRI) has emerged as a promising imaging modality for detecting brain atrophy patterns associated with AD progression, providing morphological insights into neuropathological changes. However, the inherent heterogeneity of multimodal neuroimaging data and the scarcity of clinically annotated samples significantly hinder the performance of existing deep learning approaches. Moreover, most current methods overlook the complementary information across modalities and fail to provide interpretable diagnostic evidence, which limits their clinical applicability. To address these challenges, we propose a novel Multi-Modal Fusion Network (MMF-Net), a hierarchical cross-modal attention framework for early diagnosis of Alzheimer's disease. Specifically, we first design a Modality-Specific Feature Encoder that effectively extracts hierarchical representations from structural MRI and fluorodeoxyglucose positron emission tomography (FDG-PET) via 3D convolutional architectures. Next, a Cross-Modal Attention Module is developed to model the non-linear complementary relationships between structural and metabolic features. Based on this module, we further propose an Interpretable Classification Head that adaptively weights regional contributions and generates saliency maps for clinical interpretation. Extensive experiments on the ADNI dataset demonstrate that our method achieves an accuracy of 92.3% and an AUC of 0.956 for AD vs. NC classification, outperforming state-of-the-art methods by 3.1% in accuracy and 2.4% in AUC. This article not only provides a principled multi-modal fusion framework for neuroimaging-based diagnosis but also offers interpretable evidence to support clinical decision-making.

* * *

# 模块二：Introduction

## 2.1 写作框架指引

    【必备写作要点】
    - 全文控制在 800-1200 词（视期刊要求调整）
    - 段落逻辑清晰，每段聚焦一个核心主题
    - 引用文献需覆盖：经典方法（≥3 年前）、近期进展（近 3 年）、相关工作（≥15 篇）
    - 最后一段以贡献列表结尾，条目化呈现
    - 避免在 Introduction 中展开数学公式或实验细节
    
    【核心覆盖内容】
    P1: 临床问题/疾病的流行病学背景与诊断紧迫性
    P2: 相关技术（深度学习/影像分析）在该任务上的研究基础与进展
    P3: 现有方法的关键挑战之一（技术瓶颈/数据层面）
    P4: 现有方法的另一关键挑战（方法论层面/临床需求层面）
    P5: 本文方法的整体概述、核心思想与架构概览
    P6: 贡献列表（条目化，通常 3-4 条）
    P7（可选）: 论文组织结构概述
    
    【写作逻辑顺序】
    临床背景（P1）→ 技术背景（P2）→ 挑战分析（P3-P4）→ 方法概述（P5）→ 贡献列表（P6）→ 结构概览（P7）

## 2.2 完整可复用模板（按段落划分）

* * *

### 第一段：临床问题背景

> **核心功能**：建立研究动机，阐述疾病/任务的临床重要性与诊断需求**推荐句式**：疾病流行病学描述、临床诊断紧迫性、影像学检查的临床价值

    [Target disease/condition] is one of the most [prevalent/devastating/leading cause of] [health impact, e.g., mortality/disability worldwide], affecting approximately [statistics] individuals globally as of [year]. According to recent epidemiological studies [Ref], the [prevalence/incidence] of [disease] is projected to [trend, e.g., double/triple] by [year], posing an [enormous/significant] burden on [healthcare systems/society]. The [early/precise/accurate] diagnosis of [disease] is therefore of critical clinical importance, as [clinical benefit, e.g., early intervention can significantly slow disease progression / timely treatment substantially improves patient outcomes / accurate staging enables personalized therapeutic strategies].
    
    In clinical practice, [imaging modality/modalities, e.g., structural MRI, PET, CT, X-ray] serves as a cornerstone for [clinical task, e.g., disease diagnosis/staging/treatment planning], providing [specific clinical information, e.g., in vivo visualization of pathological changes/quantitative biomarkers for disease assessment]. [Optional: Specifically, [specific imaging marker/finding] has been widely recognized as a reliable indicator for [clinical significance] [Ref].] Despite the widespread adoption of [imaging modality], the [manual/visual] interpretation of [imaging data] remains [challenging/time-consuming/subject to inter-observer variability], underscoring the need for [automated/computer-aided/intelligent] diagnostic approaches.

* * *

### 第二段：技术背景与研究基础

> **核心功能**：综述相关技术（深度学习/影像分析）在该任务上的应用进展**推荐句式**：技术发展脉络、代表性方法概述、技术优势与趋势

    Over the past decade, deep learning has achieved remarkable breakthroughs in [broad domain, e.g., medical image analysis/computer-aided diagnosis], demonstrating [superior capability, e.g., unprecedented feature extraction ability / powerful representation learning capacity] for various clinical tasks [Ref]. In the context of [specific task/disease], [method category, e.g., convolutional neural networks (CNNs) / vision transformers (ViTs)] have been widely employed to [specific function, e.g., automatically extract hierarchical features from medical images / identify disease-relevant patterns from neuroimaging data].
    
    [Optional: For example, [Author] et al. [Ref] proposed [method name], which leveraged [technique] to achieve [result] for [task]. Subsequently, [Author] et al. [Ref] introduced [method name] that incorporated [technique] for improved [performance aspect].] These methods have demonstrated the [potential/efficacy] of [technology] in [task domain], achieving [general achievement, e.g., promising diagnostic performance / competitive segmentation accuracy] on [benchmark datasets, e.g., ADNI/BraTS/ChestX-ray14].
    
    [Transition sentence]: Nevertheless, despite these encouraging advances, several fundamental challenges remain to be addressed before [technology] can be reliably translated into [clinical practice/routine clinical workflow].

* * *

### 第三段：挑战一 -- 技术瓶颈/数据层面

> **核心功能**：深入分析现有方法的第一个关键局限**推荐句式**：数据异质性、模态融合困难、样本稀缺、特征表达不充分

    One prominent challenge lies in the [specific challenge, e.g., inherent heterogeneity of multimodal imaging data / high variability of lesion appearances across patients / limited availability of annotated medical images]. [Elaboration, e.g., In clinical settings, patients are typically examined using multiple imaging modalities (e.g., T1-weighted MRI, T2-FLAIR MRI, and FDG-PET), each capturing complementary pathological information. However, effectively fusing these heterogeneous modalities remains a non-trivial problem due to their distinct physical properties and varying spatial resolutions.]
    
    Existing [method category, e.g., early-fusion approaches / late-fusion strategies] typically [specific limitation, e.g., simply concatenate multi-modal features at the input level, failing to capture cross-modal interactions / treat each modality independently, overlooking the complementary relationships between modalities]. [Author] et al. [Ref] attempted to address this issue by [approach], yet their method [remaining limitation, e.g., still relies on hand-crafted fusion rules / cannot adaptively balance the contributions of different modalities]. Consequently, [consequence, e.g., the discriminative power of the fused representation is compromised / the full potential of multi-modal information remains underexploited].

* * *

### 第四段：挑战二 -- 方法论层面/临床需求层面

> **核心功能**：深入分析现有方法的第二个关键局限（与第三段互补）**推荐句式**：可解释性不足、泛化能力弱、计算效率低、临床部署困难

    Another critical limitation of current approaches is [second challenge, e.g., the lack of interpretability in model predictions / the insufficient modeling of spatial-temporal dependencies / the poor generalization to unseen clinical centers]. [Elaboration, e.g., While deep learning models have achieved impressive accuracy, their black-box nature poses a significant barrier to clinical adoption, as physicians require transparent and interpretable diagnostic evidence to trust automated predictions.]
    
    [Author] et al. [Ref] proposed [method] to [attempted solution], which [partial achievement]. However, this approach [remaining limitation, e.g., provides only post-hoc explanations that may not faithfully reflect the model's decision process / requires additional computational overhead that limits its deployment in resource-constrained clinical environments]. Furthermore, [additional concern, e.g., most existing methods are evaluated on single-center datasets, raising concerns about their generalizability across different clinical sites with varying imaging protocols and patient demographics].
    
    Therefore, there is a pressing need for a [desired method characteristic, e.g., unified framework that can simultaneously achieve high diagnostic accuracy and provide clinically interpretable evidence / robust approach capable of effectively leveraging multi-modal information while maintaining computational efficiency].

* * *

### 第五段：本文方法概述

> **核心功能**：介绍本文方法的核心思想、整体架构与关键技术模块**推荐句式**：方法引入、架构概述、模块描述、技术优势

    To address the aforementioned challenges, we propose a novel [method name], a [framework type, e.g., end-to-end multi-modal fusion framework / generative model with conditional constraints / hybrid architecture combining CNN and Transformer] for [task, e.g., early diagnosis of [disease] / [specific clinical application]]. The overarching philosophy of [method name] is to [core idea, e.g., adaptively exploit complementary information across modalities while preserving clinically interpretable decision pathways / learn robust feature representations through probabilistic modeling of disease progression states].
    
    The overall architecture of [method name] consists of [N] key components: (1) [Module A name], which [function, e.g., extracts modality-specific hierarchical features through a 3D convolutional backbone]; (2) [Module B name], designed to [function, e.g., model cross-modal interactions via a dual-stream attention mechanism]; and (3) [Module C name], which [function, e.g., generates interpretable diagnostic predictions with region-level saliency maps].
    
    [Optional: Technical highlight paragraph] A distinctive aspect of our approach is [key innovation, e.g., the introduction of a [specific technique, e.g., probabilistic state transition mechanism] that explicitly models the [specific characteristic, e.g., continuous disease progression trajectory], enabling [advantage, e.g., more biologically plausible feature learning / robust handling of inter-subject variability]]. Unlike previous methods that [contrast with existing work], our [module name] [specific advantage, e.g., jointly optimizes feature fusion and interpretability in a unified learning objective].

* * *

### 第六段：贡献列表

> **核心功能**：条目化总结本文的核心贡献，突出创新点与学术价值**推荐句式**：标准化贡献陈述，每条贡献以动词不定式开头

    The main contributions of this paper are summarized as follows:
    
    1) **We propose [method name]**, a novel [framework type] for [task], which effectively [core advantage, e.g., integrates multi-modal imaging information through an adaptive cross-modal attention mechanism / models disease progression via conditional probabilistic state transitions]. To the best of our knowledge, this is the first work that [novelty claim, e.g., simultaneously addresses multi-modal fusion and interpretability in a unified framework for [task] / introduces [specific technique] into the domain of [application]].
    
    2) **We design [module name A]**, which [specific function and innovation, e.g., captures hierarchical spatial-temporal features from 3D medical images via a [specific mechanism, e.g., deformable attention module], effectively addressing the [specific challenge] identified in existing approaches]. [Optional: This module is theoretically grounded in [theory/concept], providing [advantage].]
    
    3) **We develop [module name B]**, a [module type] that [specific function and innovation, e.g., adaptively models the complementary relationships between [modalities/components] via [mechanism], enabling [advantage, e.g., more discriminative fused representations / robust feature learning under limited annotation scenarios]].
    
    4) **We conduct extensive experiments on [N] public benchmarks** (i.e., [dataset names]), demonstrating the [superiority/effectiveness] of our method over [comparison scope, e.g., state-of-the-art approaches / N representative baselines]. Specifically, our method achieves [key result, e.g., improvements of X.X% in accuracy and X.X% in AUC over the best-performing competing method]. [Optional: Furthermore, qualitative visualization and ablation studies provide [additional insight, e.g., interpretable evidence supporting the clinical plausibility of our model's predictions].]

* * *

### 第七段（可选）：论文组织结构

> **核心功能**：概述论文后续章节的内容安排**推荐句式**：标准论文结构描述

    The remainder of this paper is organized as follows. Section II reviews the related work on [topic areas]. Section III describes the proposed methodology in detail, including the architecture design and key technical components. Section IV presents the experimental setup, datasets, and evaluation metrics. Section V reports the experimental results and provides comprehensive analysis and discussion. Finally, Section VI concludes this paper and outlines directions for future work.

* * *

## 2.3 标准学术过渡连接词库

| 位置  | 过渡连接词/短语 | 示例  |
| --- | --- | --- |
| 段首（递进） | Furthermore, Moreover, In addition, Additionally, Besides | `Furthermore, most existing methods are evaluated on single-center datasets...` |
| 段首（转折） | However, Nevertheless, Despite this, Nonetheless, Conversely | `Nevertheless, despite these encouraging advances, several fundamental challenges remain...` |
| 段首（因果） | Therefore, Consequently, Accordingly, As a result, Thus | `Therefore, there is a pressing need for a unified framework...` |
| 段中（举例） | For example, For instance, Specifically, In particular, Notably | `Specifically, [Author] et al. proposed [method]...` |
| 段中（对比） | In contrast, Unlike, Whereas, While, On the other hand | `Unlike previous methods that simply concatenate features, our approach...` |
| 段中（强调） | Importantly, Significantly, Crucially, Notably, Of particular note | `Importantly, the proposed module can be seamlessly integrated into existing pipelines...` |
| 引出方法 | To address these challenges, Motivated by these observations, In light of the above, Building upon these insights | `To address these challenges, we propose a novel framework...` |
| 总结贡献 | In summary, In conclusion, Collectively, Taken together | `Collectively, these contributions advance the state-of-the-art in...` |

## 2.4 贡献列表标准格式模板

    The main contributions of this paper are summarized as follows:
    
    1) We propose [方法名称], a novel [框架类型] for [任务名称], which effectively [核心优势].
       [可选：To the best of our knowledge, this is the first work that [新颖性声明].]
    
    2) We design [模块A名称], which [具体功能与创新点], effectively addressing [具体挑战].
    
    3) We develop [模块B名称], a [模块类型] that [具体功能与创新点], enabling [技术优势].
    
    4) We conduct extensive experiments on [N] public benchmarks (i.e., [数据集名称]),
       demonstrating the superiority of our method over [比较范围]. Specifically, our method
       achieves [关键结果指标].

**格式要点**：

* 贡献条目以 **粗体动词短语** 开头（"We propose / We design / We develop / We conduct"）
* 每条贡献聚焦一个独立创新点，避免内容重叠
* 第一条贡献描述整体方法与核心创新，后续条目描述具体模块或实验验证
* 贡献条目通常为 3-4 条，不宜过多或过少
* 最后一条贡献固定为实验验证，包含具体量化指标

## 2.5 完整填表示例

> **示例场景**：基于条件概率状态转移 GAN 的多模态医学图像合成方法（虚构方法 "CPST-GAN-Med"）

* * *

**P1 - 临床问题背景：**

    Alzheimer's disease (AD) is one of the most prevalent neurodegenerative disorders worldwide, affecting approximately 55 million individuals globally as of 2023. According to recent epidemiological studies [1], the prevalence of AD is projected to triple by 2050, posing an enormous burden on healthcare systems and society. The early and accurate diagnosis of AD is therefore of critical clinical importance, as timely pharmacological and non-pharmacological interventions can significantly slow disease progression and improve patient quality of life. In clinical practice, structural magnetic resonance imaging (sMRI) and fluorodeoxyglucose positron emission tomography (FDG-PET) serve as cornerstones for AD diagnosis, providing in vivo visualization of brain atrophy patterns and metabolic changes associated with neurodegeneration. Despite the widespread adoption of these imaging modalities, the manual interpretation of multimodal neuroimaging data remains time-consuming and subject to inter-observer variability, underscoring the need for intelligent diagnostic approaches.

**P2 - 技术背景与研究基础：**

    Over the past decade, deep learning has achieved remarkable breakthroughs in medical image analysis, demonstrating unprecedented feature extraction capabilities for various clinical tasks [2-4]. In the context of neuroimaging-based AD diagnosis, convolutional neural networks (CNNs) and vision transformers (ViTs) have been widely employed to automatically identify disease-relevant patterns from structural and functional brain images. For example, Zhang et al. [5] proposed a 3D DenseNet-based framework that leveraged multi-scale cortical features to achieve an accuracy of 91.2% for AD vs. NC classification on the ADNI dataset. Subsequently, Li et al. [6] introduced a cross-modal attention mechanism that improved multi-modal fusion performance by modeling inter-modal dependencies. These methods have demonstrated the potential of deep learning in neuroimaging-based diagnosis, achieving promising results on benchmark datasets. Nevertheless, despite these encouraging advances, several fundamental challenges remain to be addressed before deep learning can be reliably translated into routine clinical workflow.

**P3 - 挑战一（数据层面）：**

    One prominent challenge lies in the inherent heterogeneity of multimodal neuroimaging data. In clinical settings, patients are typically examined using multiple imaging modalities (e.g., T1-weighted MRI, T2-FLAIR MRI, and FDG-PET), each capturing complementary pathological information. However, effectively fusing these heterogeneous modalities remains a non-trivial problem due to their distinct physical properties, varying spatial resolutions, and misaligned feature distributions. Existing early-fusion approaches typically simply concatenate multi-modal features at the input level, failing to capture cross-modal interactions at a deep semantic level [7]. Late-fusion strategies [8] treat each modality independently and combine predictions at the decision level, overlooking the complementary relationships between modalities. Consequently, the discriminative power of the fused representation is compromised, and the full potential of multi-modal information remains underexploited.

**P4 - 挑战二（方法论层面）：**

    Another critical limitation of current approaches is the lack of interpretability in model predictions. While deep learning models have achieved impressive diagnostic accuracy, their black-box nature poses a significant barrier to clinical adoption, as physicians require transparent and interpretable diagnostic evidence to trust automated predictions [9]. Wang et al. [10] proposed a gradient-based visualization method to generate saliency maps for AD classification, yet their approach provides only post-hoc explanations that may not faithfully reflect the model's decision process. Furthermore, most existing methods are evaluated on single-center datasets, raising concerns about their generalizability across different clinical sites with varying imaging protocols and patient demographics [11]. Therefore, there is a pressing need for a unified framework that can simultaneously achieve high diagnostic accuracy and provide clinically interpretable evidence.

**P5 - 本文方法概述：**

    To address the aforementioned challenges, we propose a novel Conditional Probabilistic State Transition GAN for Medical Imaging (CPST-GAN-Med), an end-to-end multi-modal fusion and interpretation framework for early diagnosis of Alzheimer's disease. The overarching philosophy of CPST-GAN-Med is to adaptively exploit complementary information across modalities while preserving clinically interpretable decision pathways through probabilistic modeling of disease progression states. The overall architecture consists of three key components: (1) a Modality-Specific Feature Encoder, which extracts hierarchical representations from sMRI and FDG-PET through parallel 3D convolutional backbones; (2) a Conditional State Transition Module, designed to model the continuous disease progression trajectory via a probabilistic state space formulation; and (3) an Interpretable Attention-Based Classifier, which generates region-level saliency maps to provide diagnostic evidence. A distinctive aspect of our approach is the introduction of a conditional probabilistic state transition mechanism that explicitly models the stochastic progression from normal cognition to AD, enabling more biologically plausible feature learning. Unlike previous methods that treat disease classification as a deterministic mapping, our formulation captures the inherent uncertainty in disease progression, leading to more robust predictions.

**P6 - 贡献列表：**

    The main contributions of this paper are summarized as follows:
    
    1) We propose CPST-GAN-Med, a novel conditional probabilistic framework for early AD diagnosis, which effectively integrates multi-modal imaging information through a state transition mechanism. To the best of our knowledge, this is the first work that simultaneously addresses multi-modal fusion and interpretability through probabilistic disease progression modeling.
    
    2) We design a Conditional State Transition Module that captures the stochastic trajectory of neurodegeneration via a learnable probabilistic state space, effectively addressing the challenge of modeling heterogeneous disease progression patterns.
    
    3) We develop an Interpretable Attention-Based Classifier that adaptively weights regional brain contributions and generates clinically meaningful saliency maps, enabling transparent diagnostic evidence for physicians.
    
    4) We conduct extensive experiments on three public benchmarks (i.e., ADNI-1, ADNI-2, and OASIS-3), demonstrating the superiority of our method over twelve state-of-the-art approaches. Specifically, our method achieves improvements of 3.7% in accuracy and 2.9% in AUC over the best-performing competing method for AD vs. NC classification.

**P7 - 论文组织结构（可选）：**

    The remainder of this paper is organized as follows. Section II reviews the related work on multi-modal neuroimaging fusion and interpretable deep learning for AD diagnosis. Section III describes the proposed CPST-GAN-Med methodology in detail, including the conditional state transition formulation and the interpretable attention mechanism. Section IV presents the experimental setup, datasets, evaluation metrics, and implementation details. Section V reports the experimental results and provides comprehensive analysis, including ablation studies and visualization. Finally, Section VI concludes this paper and outlines directions for future work.

* * *

# 模块三：Related Works

## 3.1 写作框架指引

    【必备写作要点】
    - 本章节须对与本文方法直接相关的前沿工作进行系统性梳理与批判性分析，而非简单罗列。
    - 每个子节须形成"列举代表工作 → 指出共同不足 → 自然引出本文方法"的三段式闭环逻辑。
    - 综述须覆盖本文方法所涉及的所有核心技术维度（如：多模态融合、特征表示学习、生成模型等），确保无遗漏。
    - 所有引用文献须为近五年（优先近三年）的高影响力工作，避免引用过时或低相关性文献。
    - 须明确区分"已有工作的贡献"与"尚未解决的关键问题"，为本文方法的提出建立充分的合理性。
    
    【核心覆盖内容】
    - 与本文任务直接相关的代表性方法（至少涵盖3个以上不同技术路线）
    - 各技术路线的核心思想、优势与局限性
    - 当前领域存在的共性技术瓶颈或研究空白
    - 本文方法相对于已有工作的差异化定位与创新切入点
    
    【写作逻辑顺序】
    - 开篇总览句（概述本节从哪几个方面展开综述）
    - 子节A：第一个技术维度（如：基于XX的方法）
    - 子节B：第二个技术维度（如：基于YY的方法）
    - 子节C：第三个技术维度（如：基于ZZ的方法，可选）
    - 末尾总结段：综合评述现有不足，引出本文方法的整体动机

## 3.2 章节总览句模板

    This section briefly reviews related studies from [数量] aspects:
    [子节A名称], [子节B名称], and [子节C名称].

**变体表达**：

    This section provides a comprehensive review of related works from the following
    [数量] perspectives: [子节A名称], [子节B名称], and [子节C名称].

    To better position our work, we review existing literature from [数量] key aspects:
    [子节A名称], [子节B名称], and [子节C名称].

## 3.3 子节三段式写作模板

### 第一段：列举代表工作

**功能**：系统梳理某一技术维度的代表性方法，展示作者对该方向的深入了解。

**句式模板**：

    [技术维度] has attracted considerable attention in [应用领域] due to its
    [优势特征]. For example, [Author1] et al. proposed [Method1] that [核心功能/技术特点].
    [Author2] et al. introduced [Method2], which [核心功能/技术特点].
    Subsequently, [Author3] et al. developed [Method3] to [核心功能/技术特点].

**变体表达**：

    A number of studies have explored [技术维度] for [任务].
    [Author1] et al. designed [Method1] that leverages [技术手段] to achieve [目标].
    [Author2] et al. presented [Method2], which employs [技术手段] for [目标].
    More recently, [Author3] et al. proposed [Method3] that incorporates [技术手段] to [目标].

    In the context of [技术维度], various approaches have been investigated.
    [Author1] et al. proposed [Method1], which [核心功能].
    Following this line, [Author2] et al. extended the idea by [扩展内容] in [Method2].
    In addition, [Author3] et al. introduced [Method3] that [核心功能].

* * *

### 第二段：指出共同不足

**功能**：批判性分析上述方法的共性局限，为本文方法的提出建立合理性。

**句式模板**：

    The above studies [融合/利用/采用] [技术/信息] from a single aspect; however,
    they [具体不足，如：fail to capture the multi-scale contextual information /
    ignore the spatial-temporal correlation / overlook the domain shift problem],
    which limits their performances in [具体场景/任务].

**变体表达**：

    Although the aforementioned methods have achieved promising results,
    they share a common limitation: [共性不足].
    Specifically, most of them [具体不足描述，如：rely on hand-crafted features /
    treat each modality independently / lack the ability to model long-range dependencies].
    Consequently, their generalization capability remains suboptimal when facing
    [挑战场景，如：complex anatomical structures / heterogeneous imaging protocols].

    Despite the progress made by these approaches,
    several critical issues remain unaddressed.
    First, [不足1]. Second, [不足2].
    Third, [不足3].
    These limitations hinder the further improvement of [性能指标/应用效果].

    However, [关键问题/因素] has often been overlooked in the existing literature,
    limiting the performances of [方法类别] in [具体任务/场景].
    In particular, [详细说明为何该问题重要].

* * *

### 第三段：自然引出本文方法

**功能**：从已有不足平滑过渡到本文方法的提出，建立逻辑因果关系。

**句式模板**：

    To address this limitation, we introduce [本文方法名称] to [解决的具体问题/实现的目标].
    Specifically, our method [核心创新点简述].

**变体表达**：

    In this study, we propose [本文方法名称] to overcome the aforementioned limitations.
    Our key insight is that [核心洞察/创新思路],
    which enables [预期效果/优势].

    Motivated by these observations, we design [本文方法/模块名称] that
    [核心设计思想]. By [具体技术手段], our approach can effectively [预期效果].

    To bridge this gap, we develop [本文方法名称], which [核心创新概述].
    The proposed method is capable of [能力描述], thereby [预期效果].

* * *

## 3.4 综述对比专用语句与过渡连接词

### 综述对比专用语句

| 功能  | 英文句式 | 中文释义 |
| --- | --- | --- |
| 方法对比 | Compared with [MethodA], [MethodB] achieves better performance in [方面], but suffers from [不足]. | 与MethodA相比，MethodB在某方面表现更好，但受限于某不足。 |
| 方法归类 | These methods can be broadly categorized into [数量] groups: [类别1] and [类别2]. | 这些方法可大致分为两类。 |
| 优势承认 | It is worth noting that [Method] has demonstrated superior capability in [方面]. | 值得注意的是，该方法在某方面展现了卓越能力。 |
| 局限强调 | Nevertheless, a critical drawback of [Method] lies in [具体局限]. | 然而，该方法的一个关键缺陷在于... |
| 趋势总结 | Recent trends indicate an increasing interest in [技术方向]. | 近期趋势表明，对某技术方向的兴趣日益增长。 |
| 差异强调 | In contrast to existing approaches that [已有做法], our method [本文做法]. | 与现有方法的做法不同，本文方法... |

### 过渡连接词

| 类别  | 连接词 |
| --- | --- |
| 递进  | Furthermore, Moreover, In addition, Additionally, Besides |
| 转折  | However, Nevertheless, Nonetheless, Although, Despite, Conversely |
| 因果  | Consequently, Therefore, Thus, As a result, For this reason |
| 举例  | For example, For instance, Specifically, In particular, To illustrate |
| 总结  | In summary, Overall, To summarize, In conclusion |
| 对比  | In contrast, On the other hand, Compared with, Whereas, While |
| 引出  | To address this, Motivated by this, To bridge this gap, In light of this |

## 3.5 填表示例

以下以"多模态医学图像融合"方向为例，展示完整的Related Works写作示例。

* * *

### A. Multi-Modal Feature Representation Learning

Multi-modal feature representation learning has attracted considerable attention in medical image analysis due to its ability to extract complementary information from different imaging modalities. For example, Zhang et al. proposed a dual-branch network that learns modality-specific features through parallel convolutional streams. Li et al. introduced a cross-attention mechanism to model inter-modal correlations for CT-MRI fusion. Subsequently, Wang et al. developed a transformer-based representation learning framework that captures global contextual dependencies across modalities.

The above studies extract multi-modal features from a single aspect (i.e., spatial or channel dimension); however, they fail to jointly model the multi-scale spatial-temporal correlations inherent in multi-modal medical images, which limits their performances in complex clinical scenarios where both local anatomical details and global contextual information are critical.

To address this limitation, we introduce a novel Hierarchical Multi-Scale Fusion (HMSF) module that adaptively aggregates multi-modal features across multiple scales. Specifically, our method employs a dual-path pyramid architecture to capture both fine-grained local details and coarse-grained global semantics, thereby achieving comprehensive multi-modal representation.

### B. Cross-Modal Information Fusion Strategies

A number of studies have explored cross-modal information fusion strategies for medical image synthesis and segmentation. Liu et al. designed a gated fusion unit that dynamically weights modality-specific contributions based on spatial attention maps. Chen et al. presented a graph-based fusion approach that models inter-modal relationships as edge connections in a modality graph. More recently, Huang et al. proposed an adversarial learning-based fusion framework that aligns feature distributions across modalities in a latent space.

Although the aforementioned methods have achieved promising results, they share a common limitation: most of them treat cross-modal fusion as a static process and ignore the dynamic nature of clinical imaging data. Specifically, these approaches lack the ability to adaptively adjust fusion strategies based on input-specific characteristics, leading to suboptimal performance when dealing with heterogeneous imaging protocols and pathological variations.

Motivated by these observations, we design an Adaptive Cross-Modal Fusion (ACMF) module that dynamically adjusts fusion weights conditioned on input content. By employing a content-aware gating mechanism, our approach can effectively select the most informative modality-specific features for each spatial location, thereby enhancing the robustness of the fusion process.

### C. [可选子节标题]

[按照相同三段式结构继续撰写...]

* * *

# 模块四：Methods

## 4.1 写作框架指引

    【必备写作要点】
    - 本章节须对所提出方法的每个核心模块进行完整、清晰、可复现的技术描述。
    - 每个子节须遵循"动机 → 概述 → 具体设计（含公式/结构） → 小结"的四步结构，确保逻辑自洽。
    - 所有数学符号须在首次出现时严格定义，后续使用保持一致。
    - 网络结构描述须与示意图（Figure X）严格对应，图文互参。
    - 损失函数须给出完整的数学定义及各符号的物理含义。
    - 训练策略与实现细节须足够详尽，以支持方法的可复现性。
    - 须明确说明本文方法与已有方法在技术设计上的本质区别。
    
    【核心覆盖内容】
    - 整体框架概述与各模块的功能定位
    - 数据表示与预处理方法
    - 核心网络模块的架构设计与数学建模
    - 损失函数的完整定义与理论依据
    - 训练策略（包括优化器、学习率调度、训练阶段划分等）
    - 推理/测试流程说明（如适用）
    
    【写作逻辑顺序】
    - 开篇总览段（概述整体框架、引用示意图、列出各子节内容）
    - 子节A：问题定义与数据表示 / 整体网络架构
    - 子节B：核心模块一（如特征提取模块）
    - 子节C：核心模块二（如融合/注意力模块）
    - 子节D：损失函数与训练策略
    - （可选）子节E：推理流程 / 临床应用

## 4.2 章节总览段模板

    This section provides a detailed introduction to our proposed method.
    The overall framework of [方法名称] is illustrated in Fig. [X],
    which mainly consists of [数量] components: [组件A], [组件B], [组件C], and [组件D].
    The framework can be summarized as follows:
    1) [组件A] is designed to [功能描述];
    2) [组件B] aims to [功能描述];
    3) [组件C] is responsible for [功能描述];
    4) [组件D] is utilized to [功能描述].
    In the following subsections, we describe each component in detail.

**变体表达**：

    The proposed framework is presented in Fig. [X] and can be summarized as follows:
    First, [步骤1描述]. Second, [步骤2描述].
    Third, [步骤3描述]. Finally, [步骤4描述].
    Section [A] describes [内容], Section [B] introduces [内容],
    Section [C] presents [内容], and Section [D] details [内容].

    In this section, we elaborate on the proposed [方法名称].
    Fig. [X] provides an overview of the overall architecture.
    The pipeline consists of three key stages:
    [阶段1], [阶段2], and [阶段3].
    We now describe each stage in detail.

## 4.3 子模块划分方式说明

根据方法复杂度与技术路线，推荐以下两种子模块划分方式：

### 方式一：按功能模块划分（推荐，适用于模块化网络设计）

| 子节  | 内容  | 写作重点 |
| --- | --- | --- |
| A. Overall Architecture | 整体框架概述 | 引用示意图，说明数据流向与各模块关系 |
| B. [核心模块1名称] | 第一个核心模块 | 动机、结构设计、数学建模 |
| C. [核心模块2名称] | 第二个核心模块 | 动机、结构设计、数学建模 |
| D. Loss Function and Training Strategy | 损失函数与训练策略 | 完整损失定义、优化细节 |

### 方式二：按技术层次递进划分（适用于理论性较强的工作）

| 子节  | 内容  | 写作重点 |
| --- | --- | --- |
| A. Problem Formulation and Notation | 问题定义与符号约定 | 数学符号严格定义 |
| B. [核心方法/模型名称] | 核心方法设计 | 数学建模、公式推导 |
| C. Network Architecture and Implementation | 网络架构与实现 | 结构描述、实现细节 |
| D. Optimization and Training | 优化与训练 | 损失函数、训练策略 |

## 4.4 子模块标准写作模板

### 步骤一：动机（Motivation）

**功能**：说明为何需要设计该模块，指出其所解决的具体技术问题。

    [技术问题/挑战] remains a critical challenge in [任务/领域].
    Existing approaches typically [已有做法], which suffers from [具体不足].
    To address this limitation, the [模块名称] is designed to [目标].

**变体表达**：

    A key observation in [任务/领域] is that [关键洞察].
    However, conventional methods [已有做法], leading to [不良后果].
    Motivated by this observation, we propose [模块名称] to [目标].

* * *

### 步骤二：概述（Overview）

**功能**：用一两句话概括该模块的核心设计思想。

    The [模块名称] takes [输入] as input and outputs [输出].
    It consists of [数量] main components: [组件1] and [组件2].
    The core idea is to [核心设计思想].

**变体表达**：

    In this section, we use [技术手段] to obtain [目标].
    The detailed process is as follows:
    Given [输入], we first [步骤1], then [步骤2], and finally [步骤3].

* * *

### 步骤三：具体设计（Detailed Design，含公式）

**功能**：给出模块的详细技术描述，包括数学公式、网络结构、算法流程等。

（公式描述与网络结构描述的专用模板见4.5和4.6节）

* * *

### 步骤四：小结（Summary）

**功能**：总结该模块的设计要点与预期效果，承上启下。

    In summary, the [模块名称] effectively [功能总结] by [技术手段总结].
    This design enables [预期效果], which is crucial for [下游任务/整体性能].

**变体表达**：

    Through the [模块名称], our method can [能力描述].
    This provides a solid foundation for [后续模块/整体目标].

## 4.5 公式描述的标准句式模板

### 公式引入句

    The [目标/函数/操作] of [模块名称] is defined as follows:

    Formally, the [目标/函数/操作] can be expressed as:

    The [目标/函数/操作] is computed by:

    Given [前提条件], we formulate [目标] as:

### 符号定义句

    where [符号1] represents [含义1],
    [symbol2] denotes [含义2],
    [symbol3] indicates [含义3],
    and [symbol4] is the [含义4].

    where [符号1] \in [集合] denotes [含义1],
    [symbol2] \in [集合] represents [含义2],
    and [symbol3] \in [集合] stands for [含义3].

### 公式解释句

    Eq. ([X]) indicates that [公式含义的解释].

    From Eq. ([X]), it can be observed that [公式蕴含的物理/几何/统计含义].

    The term [某一项] in Eq. ([X]) measures [该部分的含义/作用].

    Intuitively, Eq. ([X]) encourages [期望行为] while penalizing [不期望行为].

### 公式推导/简化句

    By substituting Eq. ([X]) into Eq. ([Y]), we obtain:

    Eq. ([X]) can be rewritten as:

    After simplification, the final form of [目标] is:

## 4.6 网络结构描述的标准句式模板

### 整体架构描述

    The overall architecture of [模块名称] is depicted in Fig. [X].
    It comprises [数量] layers/blocks: [层1描述], [层2描述], and [层3描述].
    The input [输入描述] is first fed into [层1], which outputs [中间特征描述].
    Subsequently, [中间特征] is processed by [层2] to obtain [更高级特征].
    Finally, [层3] maps [高级特征] to the [输出描述].

### 卷积/注意力模块描述

    The [模块名称] consists of [数量] convolutional layers with kernel sizes of
    [尺寸1] and [尺寸2], followed by [激活函数/归一化层].
    Each convolutional layer is configured with [通道数] input channels and
    [通道数] output channels.
    A [残差连接/跳跃连接] is applied between the input and output to
    alleviate the gradient vanishing problem.

    The attention mechanism in [模块名称] is formulated as:
    [公式]
    where [符号] represents the query matrix,
    [symbol] denotes the key matrix,
    and [symbol] indicates the value matrix.
    The attention weights are normalized by [softmax/sigmoid] along the
    [空间维度/通道维度].

### 多尺度/多阶段结构描述

    To capture multi-scale features, we adopt a [U-Net/FPN/pyramid] structure
    with [数量] resolution levels.
    At each level, a [模块名称] is applied to extract features at the
    corresponding scale.
    Features from adjacent levels are connected via [跳跃连接/上采样/下采样].

    The [模块名称] operates at [数量] scales:
    {s_1, s_2, ..., s_N}, where s_i = [尺度定义].
    At each scale, a dedicated [子模块名称] is employed to process
    features of size [尺寸].
    The multi-scale features are then aggregated via [融合策略].

### 特征维度变换描述

    The feature map [符号] has dimensions of
    [C \times H \times W], where C, H, and W denote
    the number of channels, height, and width, respectively.
    After the [操作名称], the feature dimensions become [新维度].

## 4.7 损失函数与训练过程描述模板

### 损失函数定义

    The overall loss function of the proposed [方法名称] is defined as a
    weighted combination of [数量] loss terms:

    \mathcal{L}_{total} = \lambda_1 \mathcal{L}_1 + \lambda_2 \mathcal{L}_2 + \lambda_3 \mathcal{L}_3

    where \lambda_1, \lambda_2, and \lambda_3 are the balancing weights
    that control the relative importance of each loss term.

#### 各项损失详细定义

    1) [损失1名称]: The [损失1名称] measures [物理含义/优化目标]
    and is formulated as:
    \mathcal{L}_1 = [公式]
    where [符号] denotes [含义].
    
    2) [损失2名称]: To [优化目标], we introduce the [损失2名称]:
    \mathcal{L}_2 = [公式]
    where [符号] represents [含义].
    
    3) [损失3名称]: The [损失3名称] is designed to [优化目标]:
    \mathcal{L}_3 = [公式]
    where [符号] indicates [含义].

### 损失函数设计动机

    The [损失名称] is adopted because [选择理由，如：it provides
    pixel-wise supervision for dense prediction tasks /
    it encourages structural consistency between the input and output /
    it regularizes the model to prevent overfitting].

    Compared with the traditional [传统损失], our [自定义损失]
    additionally considers [额外因素], which is particularly important
    for [具体场景/任务].

### 训练策略描述

    The adversarial training of [方法名称] is divided into [数量] main steps:

    Step 1 (Generator Training):
    The generator [G] is trained to minimize the loss:
    \mathcal{L}_G = [公式]
    The parameters of [G] are updated while the parameters of [D] are fixed.
    
    Step 2 (Discriminator Training):
    The discriminator [D] is trained to maximize the loss:
    \mathcal{L}_D = [公式]
    The parameters of [D] are updated while the parameters of [G] are fixed.

### 优化器与超参数

    The entire network is optimized using the [Adam/SGD/AdamW] optimizer
    with an initial learning rate of [数值].
    The learning rate is decayed by a factor of [数值] every [数值] epochs
    according to the [cosine annealing/step decay/polynomial decay] schedule.
    The batch size is set to [数值], and the model is trained for [数值] epochs
    in total.
    We adopt [数据增强策略] for data augmentation during training.
    All experiments are implemented using the [PyTorch/TensorFlow] framework
    on [硬件配置].

### 多阶段训练（如适用）

    The training process consists of [数量] stages:
    In the first stage, we train [模块A] for [数值] epochs with
    \mathcal{L}_A to learn [目标].
    In the second stage, we fix the parameters of [模块A] and train
    [模块B] for [数值] epochs with \mathcal{L}_B to learn [目标].
    Finally, the entire network is jointly fine-tuned for [数值] epochs
    with \mathcal{L}_{total}.

## 4.8 填表示例

以下以一个假设的医学图像分割方法为例，展示完整的Methods写作示例。

* * *

### A. Overall Architecture

The overall architecture of the proposed method, termed Multi-Scale Adaptive Fusion Network (MSAF-Net), is illustrated in Fig. 1. The framework mainly consists of four components: a Multi-Scale Feature Encoder (MSE), a Cross-Modal Attention Fusion (CMAF) module, a Spatial-Temporal Refinement (STR) module, and a Task-Specific Decoder (TSD). The framework can be summarized as follows: 1) The MSE is designed to extract hierarchical multi-scale features from multi-modal inputs; 2) The CMAF module aims to model cross-modal correlations and adaptively fuse modality-specific features; 3) The STR module is responsible for refining spatial details and temporal consistency; 4) The TSD is utilized to generate the final segmentation map. In the following subsections, we describe each component in detail.

### B. Multi-Scale Feature Encoder

Accurately extracting multi-scale anatomical features from medical images remains a critical challenge in multi-modal segmentation. Existing approaches typically employ single-scale convolutional backbones, which suffer from limited receptive fields and insufficient representation capacity for both fine-grained structures and large-scale anatomical regions. To address this limitation, the Multi-Scale Feature Encoder (MSE) is designed to capture hierarchical features across multiple scales.

The MSE takes multi-modal input images $\{I_1, I_2, \ldots, I_M\}$ as input and outputs a set of multi-scale feature maps $\{F_1, F_2, F_3, F_4\}$ at four resolution levels. It consists of four cascaded encoding blocks, each comprising a residual convolutional unit and a dilated spatial pyramid pooling module. The core idea is to progressively increase the receptive field while preserving spatial resolution through skip connections.

Formally, the feature extraction at the $l$-th level can be expressed as:

$$F_l = \text{RCU}_l(\text{DSPP}_l(F_{l-1})), \quad l = 1, 2, 3, 4$$

where $F_{l-1}$ represents the input feature map from the previous level (with $F_0 = I$ denoting the raw input), $\text{DSPP}_l(\cdot)$ denotes the dilated spatial pyramid pooling operation at scale $l$, and $\text{RCU}_l(\cdot)$ indicates the residual convolutional unit. The dilated spatial pyramid pooling employs parallel dilated convolutions with dilation rates of $\{1, 2, 4, 8\}$ to capture multi-scale contextual information.

In summary, the MSE effectively extracts hierarchical multi-scale features by combining residual learning and dilated convolution strategies. This design enables the network to capture both local fine-grained details and global contextual semantics, which is crucial for accurate medical image segmentation.

### C. Cross-Modal Attention Fusion Module

A key observation in multi-modal medical image analysis is that different imaging modalities provide complementary information about the same anatomical structure. However, conventional fusion methods simply concatenate or add multi-modal features, leading to information redundancy and insufficient exploitation of cross-modal correlations. Motivated by this observation, we propose the Cross-Modal Attention Fusion (CMAF) module to adaptively select and fuse informative features across modalities.

In this section, we use a cross-modal attention mechanism to obtain modality-aware feature representations. The detailed process is as follows: Given multi-modal features $\{F^1_l, F^2_l, \ldots, F^M_l\}$ at the $l$-th level, we first compute cross-modal attention maps to model the inter-modal correlations. Then, the attention-weighted features are aggregated to produce a fused representation.

The cross-modal attention weight between modality $i$ and modality $j$ at spatial position $(h, w)$ is computed by:

$$A_{l}^{i \to j}(h, w) = \frac{\exp(\text{sim}(F_l^i(h,w), F_l^j(h,w)))}{\sum_{k=1}^{M} \exp(\text{sim}(F_l^i(h,w), F_l^k(h,w)))}$$

where $A_{l}^{i \to j}(h, w)$ represents the attention weight from modality $i$ to modality $j$ at position $(h, w)$, and $\text{sim}(\cdot, \cdot)$ denotes the cosine similarity function. The fused feature at the $l$-th level is obtained by:

$$\hat{F}_l = \sum_{j=1}^{M} A_{l}^{i \to j} \odot F_l^j$$

where $\hat{F}_l$ denotes the fused feature map, and $\odot$ indicates the element-wise multiplication.

Through the CMAF module, our method can adaptively emphasize the most informative modality-specific features while suppressing redundant or noisy information. This provides a solid foundation for the subsequent refinement and decoding stages.

### D. Loss Function and Training Strategy

The overall loss function of the proposed MSAF-Net is defined as a weighted combination of three loss terms:

$$\mathcal{L}_{total} = \lambda_1 \mathcal{L}_{seg} + \lambda_2 \mathcal{L}_{cons} + \lambda_3 \mathcal{L}_{reg}$$

where $\lambda_1$, $\lambda_2$, and $\lambda_3$ are the balancing weights that control the relative importance of each loss term.

1. **Segmentation Loss ($\mathcal{L}_{seg}$)**: The segmentation loss measures the pixel-wise discrepancy between the predicted segmentation map and the ground truth, and is formulated as a combination of Dice loss and cross-entropy loss:

$$\mathcal{L}_{seg} = \mathcal{L}_{CE} + \mathcal{L}_{Dice}$$

where $\mathcal{L}_{CE}$ denotes the standard cross-entropy loss, and $\mathcal{L}_{Dice}$ represents the Dice loss that directly optimizes the Dice similarity coefficient.

2. **Consistency Loss ($\mathcal{L}_{cons}$)**: To enforce structural consistency between the multi-scale feature maps and the final prediction, we introduce the consistency loss:

$$\mathcal{L}_{cons} = \sum_{l=1}^{4} \|\phi_l(\hat{F}_l) - S\|_2^2$$

where $\phi_l(\cdot)$ represents a lightweight projection layer at the $l$-th level, and $S$ denotes the ground truth segmentation map.

3. **Regularization Loss ($\mathcal{L}_{reg}$)**: The regularization loss is designed to prevent overfitting by encouraging smoothness of the attention maps:

$$\mathcal{L}_{reg} = \sum_{l=1}^{4} \sum_{i=1}^{M} \|A_l^i - \bar{A}_l^i\|_F^2$$

where $A_l^i$ denotes the attention map of modality $i$ at level $l$, and $\bar{A}_l^i$ is the spatially smoothed version obtained by average pooling.

The entire network is optimized using the AdamW optimizer with an initial learning rate of $1 \times 10^{-4}$. The learning rate is decayed by a factor of 0.1 every 50 epochs according to the cosine annealing schedule. The batch size is set to 8, and the model is trained for 200 epochs in total. The balancing weights are empirically set as $\lambda_1 = 1.0$, $\lambda_2 = 0.5$, and $\lambda_3 = 0.1$. We adopt random flipping, rotation, and intensity augmentation for data augmentation during training. All experiments are implemented using the PyTorch framework on four NVIDIA A100 GPUs.

* * *

# 模块五：Discussion

## 5.1 写作框架指引

    【必备写作要点】
    - 必须对实验结果进行深度解读，而非简单复述数据
    - 每个论断必须有文献支撑或统计证据
    - 需体现"方法优势 → 生物学/临床意义 → 与已有研究的一致性/差异性 → 局限性"的完整论证链
    
    【核心覆盖内容】
    (1) 整体性能优势的归因分析；(2) 各关键模块/组件的贡献与消融验证；(3) 与SOTA方法的逐维度对比；
    (4) 可解释性分析（如适用）；(5) 临床/生物学意义阐释；(6) 局限性坦诚讨论；(7) 未来工作展望
    
    【写作逻辑顺序】
    开篇总结核心发现 → 逐维度深入分析（性能→模块→对比→可解释性→临床意义）→ 局限性 → 未来工作

## 5.2 子节划分方式说明

推荐采用 **5~6个子节** 的结构化组织方式，每个子节对应一个独立分析维度。具体划分如下：

| 子节编号 | 推荐标题 | 核心分析维度 | 建议篇幅 |
| --- | --- | --- | --- |
| A   | **Overall Performance Analysis** | 整体性能优势的量化总结与归因 | 1段  |
| B   | **Component-wise Contribution Analysis** | 各关键模块/组件的消融实验解读 | 1~2段 |
| C   | **Comparison with State-of-the-art Methods** | 与已有方法的逐维度对比分析 | 1~2段 |
| D   | **Interpretability and Clinical Relevance** | 可解释性分析与临床/生物学意义 | 1~2段 |
| E   | **Limitations and Future Directions** | 局限性坦诚讨论与未来工作展望 | 1段  |

> **注**：若论文不含可解释性分析模块，可省略子节D，将临床意义融入子节C。若论文涉及多数据集/多中心验证，可在子节C后增设"Cross-dataset/Cross-center Generalization"子节。

## 5.3 各子节标准写作模板

### 子节A：Overall Performance Analysis（整体性能分析）

    The experimental results presented in Section [X] demonstrate that the proposed [方法名]
    achieves superior performance in [任务名称] compared with existing approaches. Specifically,
    our method yields an accuracy/AUC/sensitivity of [数值], outperforming the best competing
    method by [数值/百分比]. This performance improvement can be attributed to several key
    design choices in our framework. First, the [核心机制/创新点1] enables the model to
    capture [具体特征/模式] that are critical for [临床任务]. Second, the [核心机制/创新点2]
    facilitates a more comprehensive exploration of [数据特征/病理特征], which is essential
    for distinguishing between [类别/阶段]. These results collectively indicate that the
    integration of [技术A] and [技术B] within a unified framework provides a more effective
    solution for [任务名称] than treating them as isolated components.

**写作要点**：

* 首句直接点明核心发现，避免冗余铺垫
* 用 "can be attributed to" 进行因果归因，而非简单罗列结果
* 量化对比须精确（具体数值/百分比），不可使用模糊表述

* * *

### 子节B：Component-wise Contribution Analysis（模块贡献分析）

    To investigate the contribution of each key component in the proposed framework, we
    conducted ablation studies as detailed in Table [X]. The results reveal several notable
    findings. First, removing the [模块名A] leads to a performance degradation of [数值] in
    [指标], confirming that [模块功能描述] is essential for [具体任务目标]. This finding is
    consistent with the understanding that [相关领域知识/先验], as previously reported by
    [Author] et al. [引用]. Second, the incorporation of [模块名B] contributes an improvement
    of [数值] in [指标], which can be ascribed to its specific capacity to [模块的特定功能].
    This superior ability stems from the fact that [技术原理/机制解释]. Furthermore, the
    joint utilization of [模块A] and [模块B] yields a cumulative improvement beyond the sum
    of their individual contributions, suggesting a synergistic effect between [机制A] and
    [机制B] in capturing [目标特征].

**写作要点**：

* 每个模块的贡献须对应具体的消融实验结果
* 使用 "can be ascribed to" / "stems from the fact that" 进行因果解释
* 若存在协同效应，须明确指出并解释机制

* * *

### 子节C：Comparison with State-of-the-art Methods（与SOTA方法对比）

    We further compare the proposed method with several representative state-of-the-art
    approaches, including [方法1], [方法2], and [方法3]. As shown in Table [X], our method
    consistently outperforms these competitors across multiple evaluation metrics. In
    particular, compared with [方法1], which relies on [技术路线], our approach achieves
    [具体数值提升] improvement in [指标]. This advantage can be explained by the fact that
    [方法1的局限] limits its ability to capture [关键特征], whereas our [核心创新] explicitly
    models [目标特征/关系]. Similarly, [方法2] employs [技术], which may not adequately
    address [具体问题]. In contrast, our [模块名] is designed to handle this challenge by
    [具体机制].
    
    Furthermore, we analyzed the [分析对象，如结构连接脑网络/分割结果/特征分布] obtained
    by the proposed method in comparison with those obtained by [Author] et al. [引用]. The
    comparison reveals that our method produces [更合理/更一致/更具判别性] [分析对象], which
    aligns with the clinical expectation that [临床先验知识]. This connection resonates with
    previous findings reporting a strong correlation between [变量A] and [变量B] in
    [疾病/任务] [引用].

**写作要点**：

* 对比须逐方法进行，每个对比点需解释"为何优于"
* 须引用文献支撑临床先验或已有发现
* 使用 "resonates with previous findings" / "aligns with the clinical expectation" 建立一致性

* * *

### 子节D：Interpretability and Clinical Relevance（可解释性与临床意义）

    Beyond quantitative performance, we conducted interpretability analysis to elucidate the
    decision-making process of the proposed model. As illustrated in Fig. [X], the [可视化方法，
    如attention map/Grad-CAM/Shapley value/saliency map] highlights [关键区域/特征] as the
    most discriminative regions for [任务]. The previous research validates the significance
    of these regions in [疾病进展/诊断/预后] [引用]. Notably, [具体发现，如某脑区被显著激活],
    which is consistent with the neuropathological understanding that [病理机制].
    
    However, it should be noted that [可视化方法] in Fig. [X] could not clearly identify
    [某些区域/特征] due to the complexity of [数据特性/疾病异质性]. This limitation
    inherent to [可视化方法/分析工具] suggests that more sophisticated interpretability
    approaches may be needed to fully uncover the underlying pathological mechanisms.
    
    From a clinical perspective, the identified [关键特征/区域] provide potential biomarkers
    for [临床应用，如早期诊断/疾病进展监测]. The ability of our method to localize and
    quantify these features suggests its potential utility as a clinical decision support tool
    for [具体临床场景].

**写作要点**：

* 可解释性分析须与临床/生物学知识关联
* 对可视化方法的局限性须坦诚说明
* 须点明临床转化价值，但避免过度宣称

* * *

### 子节E：Limitations and Future Directions（局限性与未来工作）

    Despite the promising results, several limitations of the current study should be
    acknowledged. First, the experiments were conducted on [数据集描述], which may limit
    the generalizability of our findings to [其他人群/其他模态/其他疾病]. Future work should
    validate the proposed method on larger, multi-center datasets to assess its robustness
    across diverse clinical settings. Second, the current framework does not explicitly
    model [未考虑的因素，如纵向变化/多模态时序关系/个体差异], which may provide additional
    diagnostic information. Incorporating [相关技术/建模策略] could potentially further
    enhance the performance. Third, the computational cost of [具体模块/整体框架] remains
    relatively high, which may hinder its deployment in resource-constrained clinical
    environments. Optimizing the model architecture for efficient inference represents an
    important direction for future research.
    
    In summary, this study provides a [形容词] framework for [任务/应用场景] that demonstrates
    state-of-the-art performance. The extensive experiments and detailed analysis validate
    the effectiveness of each component and reveal clinically meaningful insights. We believe
    that the proposed approach holds promise for facilitating [临床目标] and warrants further
    investigation in prospective clinical studies.

**写作要点**：

* 局限性须具体、可操作，避免泛泛而谈
* 每个局限性须对应一个具体的未来工作方向
* 结尾段须总结全文贡献，但措辞须审慎（使用 "holds promise" / "warrants further investigation" 而非绝对化表述）

## 5.4 专用句式库

### 5.4.1 结果分析专用语句

| 功能  | 句式模板 | 示例  |
| --- | --- | --- |
| 结果总结 | Based on the [实验/结果], [数量] conclusions can be drawn. | Based on the experimental results, three conclusions can be drawn. |
| 结果解读 | This indicates that [解释], suggesting that [深层含义]. | This indicates that incorporating multimodal information facilitates a more comprehensive exploration of pathological patterns. |
| 结果归因 | This superior [能力/性能] of [方法] can be ascribed to its specific capacity to [功能]. | This superior diagnostic ability of MDL-Net can be ascribed to its specific capacity to capture cross-modal complementary features. |
| 发现强调 | Notably, [发现], which is consistent with [文献/先验]. | Notably, the hippocampus was consistently identified as the most discriminative region, which is consistent with the neuropathological literature. |
| 趋势描述 | The results demonstrate a clear trend that [趋势描述]. | The results demonstrate a clear trend that performance improves monotonically with the incorporation of additional modalities. |
| 统计支撑 | This difference was statistically significant (p < [阈值]), confirming that [结论]. | This difference was statistically significant (p < 0.05), confirming that the proposed fusion strategy yields meaningful improvements. |

### 5.4.2 对比验证句式

| 功能  | 句式模板 |
| --- | --- |
| 与已有研究一致 | This connection resonates with previous findings reporting a strong correlation between [A] and [B] in [疾病/任务] [引用]. |
| 与已有研究对比 | In contrast to the findings of [Author] et al., our results suggest that [结论]. |
| 验证已有假设 | The previous research validates the significance of [区域/特征] in [疾病进展/诊断] [引用]. |
| 方法优势对比 | Compared with [方法], which relies on [技术], our approach achieves [提升] improvement by explicitly modeling [特征]. |
| 逐维度对比 | Specifically, our method outperforms [方法] by [数值] in [指标1] and [数值] in [指标2], demonstrating its advantage in both [维度1] and [维度2]. |
| 一致性声明 | These findings are in good agreement with [文献], which reported that [已有结论]. |

### 5.4.3 因果解释句式

| 功能  | 句式模板 |
| --- | --- |
| 归因分析 | This performance improvement can be attributed to [原因]. |
| 特定能力归因 | This superior [能力] of [方法] can be ascribed to its specific capacity to [功能]. |
| 机制溯源 | This advantage stems from the fact that [技术原理]. |
| 效应解释 | The improvement observed in [指标] is primarily driven by [机制/模块]. |
| 协同效应 | The joint utilization of [A] and [B] yields a cumulative improvement beyond the sum of their individual contributions, suggesting a synergistic effect between [机制A] and [机制B]. |
| 负面效应解释 | The performance degradation when removing [模块] can be explained by the absence of [功能], which is crucial for [任务目标]. |

## 5.5 局限性表述标准句式

### 5.5.1 数据层面局限性

    First, the current study was conducted on [数据集描述，含样本量、来源、人口学特征],
    which may limit the generalizability of our findings to [更广泛的人群/其他临床场景].
    The relatively [small/sample size/homogeneous] nature of the dataset necessitates caution
    when interpreting the results. Future studies should validate the proposed method on
    larger, multi-center, and ethnically diverse cohorts to establish its robustness and
    applicability across different clinical settings.

### 5.5.2 方法层面局限性

    Second, the proposed framework does not explicitly account for [未建模的因素，如纵向变化/
    个体差异/模态缺失/类别不平衡]. This may restrict its applicability in scenarios where
    [具体限制场景]. Incorporating [相关技术/建模策略，如时序建模/元学习/生成式补全] could
    potentially address this limitation and further enhance the model's capability.

### 5.5.3 可解释性层面局限性

    Third, despite the interpretability analysis provided in this study, the [可视化方法]
    in Fig. [X] could not clearly identify [某些区域/特征] due to the complexity of
    [数据特性/疾病异质性/高维特征空间]. This inherent limitation of [方法/工具] suggests
    that more sophisticated interpretability approaches, such as [替代方法], may be needed
    to fully uncover the underlying decision-making mechanisms.

### 5.5.4 计算效率层面局限性

    Finally, the computational cost of [具体模块/整体框架] remains relatively high,
    requiring approximately [时间/资源] for [推理/训练] on a single [数据样本/受试者].
    This may hinder its deployment in resource-constrained clinical environments or
    real-time diagnostic applications. Model compression techniques, such as [知识蒸馏/
    轻量化设计/量化], represent a promising direction for addressing this challenge.

## 5.6 未来工作方向表述模板

### 模板一：多中心验证方向

    A primary direction for future research is the external validation of the proposed method
    on independent, multi-center datasets. This is particularly important for establishing
    the generalizability of [方法/模型] across different imaging protocols, scanner
    manufacturers, and patient populations. We envision conducting prospective studies in
    collaboration with [机构类型] to evaluate the clinical utility of our approach in
    real-world diagnostic workflows.

### 模板二：方法拓展方向

    Another promising avenue is to extend the current framework to incorporate [拓展内容，
    如纵向多时间点数据/更多模态/自监督预训练]. By leveraging [技术/策略], the model could
    potentially capture [更丰富的特征/时序动态/跨域知识], leading to improved performance in
    [任务]. Additionally, exploring [新技术，如Transformer架构/对比学习/基础模型] within
    our framework may yield further performance gains.

### 模板三：临床转化方向

    From a translational perspective, future work should focus on integrating the proposed
    method into clinical decision support systems. This requires addressing several practical
    considerations, including [实时推理/模型可解释性/监管合规]. We plan to develop a
    user-friendly interface that presents the model's predictions along with [可视化解释/
    置信度评估/临床建议], enabling clinicians to make more informed diagnostic decisions.

## 5.7 填表示例

> 以下示例基于一个虚构的医学影像分析方法（"TransMCI-Net"——用于阿尔茨海默病轻度认知障碍转化的多模态Transformer网络）进行填写演示。

### 子节A示例

> The experimental results presented in Section 4 demonstrate that the proposed TransMCI-Net achieves superior performance in predicting MCI-to-AD conversion compared with existing approaches. Specifically, our method yields an AUC of 0.923, outperforming the best competing method by 4.7%. This performance improvement can be attributed to several key design choices in our framework. First, the cross-modal Transformer encoder enables the model to capture long-range dependencies between structural and functional brain features that are critical for early AD detection. Second, the disease-progress-aware attention mechanism facilitates a more comprehensive exploration of longitudinal pathological patterns, which is essential for distinguishing between stable MCI and progressive MCI. These results collectively indicate that the integration of Transformer architecture with disease-specific inductive biases within a unified framework provides a more effective solution for MCI conversion prediction than treating them as isolated components.

### 子节B示例

> To investigate the contribution of each key component in the proposed framework, we conducted ablation studies as detailed in Table 3. The results reveal several notable findings. First, removing the cross-modal Transformer encoder leads to a performance degradation of 3.2% in AUC, confirming that cross-modal feature interaction is essential for accurate conversion prediction. This finding is consistent with the understanding that structural and functional brain changes provide complementary diagnostic information, as previously reported by Zhang et al. [28]. Second, the incorporation of the disease-progress-aware attention module contributes an improvement of 2.1% in AUC, which can be ascribed to its specific capacity to model the non-linear trajectory of neuropathological degeneration. This superior ability stems from the fact that the attention weights are explicitly guided by the known disease progression staging. Furthermore, the joint utilization of both modules yields a cumulative improvement beyond the sum of their individual contributions, suggesting a synergistic effect between cross-modal interaction and progression-aware modeling in capturing discriminative pathological features.

### 子节C示例

> We further compare the proposed method with several representative state-of-the-art approaches, including MMoE [15], GraphNet [22], and MDL-Net [31]. As shown in Table 2, our method consistently outperforms these competitors across multiple evaluation metrics. In particular, compared with MMoE, which relies on mixture-of-experts for modality fusion, our approach achieves a 4.7% improvement in AUC. This advantage can be explained by the fact that the late fusion strategy in MMoE limits its ability to capture fine-grained cross-modal interactions, whereas our cross-modal Transformer explicitly models the pairwise relationships between features from different modalities. Similarly, GraphNet employs graph convolutional networks for brain network analysis, which may not adequately address the heterogeneity of MCI subtypes. In contrast, our disease-progress-aware attention is designed to handle this challenge by adaptively weighting brain regions according to their stage-specific relevance.
> 
> Furthermore, we analyzed the structural connectivity brain networks obtained by the proposed method in comparison with those obtained by Wang et al. [22]. The comparison reveals that our method produces more clinically plausible connectivity patterns, particularly in the default mode network and the hippocampal complex, which aligns with the clinical expectation that these regions are among the earliest affected in AD pathogenesis. This connection resonates with previous findings reporting a strong correlation between default mode network disruption and cognitive decline in MCI patients [35].

### 子节D示例

> Beyond quantitative performance, we conducted interpretability analysis to elucidate the decision-making process of the proposed model. As illustrated in Fig. 5, the disease-progress-aware attention maps highlight the entorhinal cortex, posterior cingulate cortex, and hippocampus as the most discriminative regions for MCI conversion prediction. The previous research validates the significance of these regions in MCI progression [36, 37]. Notably, the entorhinal cortex exhibited the highest attention weights in the progressive MCI group, which is consistent with the neuropathological understanding that Braak stage I-II transentorhinal pathology precedes hippocampal involvement.
> 
> However, it should be noted that the attention maps in Fig. 5 could not clearly identify the contribution of subcortical structures due to the complexity of the heterogeneous atrophy patterns in MCI. This limitation inherent to attention-based visualization suggests that more sophisticated interpretability approaches, such as concept-based explanations, may be needed to fully uncover the underlying pathological mechanisms.
> 
> From a clinical perspective, the identified regional attention patterns provide potential imaging biomarkers for early identification of MCI individuals at high risk of conversion to AD. The ability of our method to localize and quantify region-specific pathological signatures suggests its potential utility as a clinical decision support tool for targeted therapeutic intervention trials.

### 子节E示例

> Despite the promising results, several limitations of the current study should be acknowledged. First, the experiments were conducted on the ADNI cohort comprising 432 MCI subjects from a single research consortium, which may limit the generalizability of our findings to broader clinical populations with diverse demographic and comorbidity profiles. Future work should validate the proposed method on larger, multi-center datasets such as the AIBL and NACC cohorts to assess its robustness across diverse clinical settings. Second, the current framework does not explicitly model the temporal progression of individual subjects, which may provide additional predictive information. Incorporating longitudinal trajectory modeling could potentially further enhance the prediction accuracy. Third, the computational cost of the cross-modal Transformer encoder remains relatively high, requiring approximately 0.8 seconds per sample for inference. This may hinder its deployment in resource-constrained clinical environments. Optimizing the model architecture through knowledge distillation represents an important direction for future research.
> 
> In summary, this study provides an effective and interpretable framework for MCI-to-AD conversion prediction that demonstrates state-of-the-art performance. The extensive experiments and detailed analysis validate the effectiveness of each component and reveal clinically meaningful insights into the regional brain changes associated with disease progression. We believe that the proposed approach holds promise for facilitating early identification of high-risk MCI patients and warrants further investigation in prospective clinical studies.

* * *

# 模块六：Conclusion

## 6.1 写作框架指引

    【必备写作要点】
    - 篇幅控制在 100~150 词（1段紧凑型），须言简意赅
    - 须覆盖：问题定义 → 方法概述（含核心创新） → 实验验证结论 → 意义/贡献
    - 不可引入新信息、新实验结果或新引用
    - 避免与Abstract过度重复，侧重于"贡献总结"而非"研究概述"
    
    【核心覆盖内容】
    (1) 研究问题与动机的精炼概括；(2) 所提方法的名称与核心机制的简要回顾；
    (3) 关键实验结论（含性能优势与对比结果）；(4) 研究意义与潜在临床价值的升华
    
    【写作逻辑顺序】
    问题动机（1句）→ 方法概述（1~2句）→ 实验验证结论（1句）→ 意义升华（1句）

## 6.2 完整可复用模板文本

    In this study, we introduce a novel framework called [方法名] for [任务名称],
    which integrates [核心技术1] and [核心技术2] to comprehensively analyze [分析对象]
    and enhance [任务目标]. Specifically, [方法名] designs a [核心机制描述，如multimodal
    fusion joint learning / pathogenesis-driven generative model] to [核心功能]. To further
    refine the identification of [细分任务/关键特征], we propose a [补充模块名] that
    [模块功能描述]. Experimental validations on the [数据集名称] dataset demonstrate
    the superiority and effectiveness of [方法名] in both [任务1] and [任务2] tasks,
    outperforming the state-of-the-art methods by [具体数值/百分比] in [核心指标].
    Moreover, our detailed analysis shows that [关键发现/临床意义]. In summary, this
    study provides a/an [形容词，如effective/interpretable/clinically meaningful]
    framework for [应用场景], holding promise for [临床目标/未来方向].

## 6.3 句式分类说明

### 6.3.1 方法总结句

| 类型  | 句式模板 | 说明  |
| --- | --- | --- |
| 开篇引入 | In this study, we introduce a novel framework called [方法名] for [任务], which integrates [技术A] and [技术B] to [目标]. | 直接点明方法名称与核心思路 |
| 问题导向 | To address current challenges in [问题], this article combines [A] with [B] to effectively mine [目标] and enhance [目标2]. | 从问题出发引出方法 |
| 机制描述 | Specifically, we first propose a [模型名] mathematical model based on the pathogenesis of [疾病], where [机制描述]. | 适用于病理驱动的方法 |
| 模块补充 | To further refine the identification of [目标], we propose a [模块名] that [功能]. | 补充说明辅助模块 |
| 设计理念 | [方法名] designs a [机制描述] to comprehensively analyze [对象] and capture [特征]. | 概括整体设计理念 |

### 6.3.2 实验验证句

| 类型  | 句式模板 | 说明  |
| --- | --- | --- |
| 综合验证 | Experimental validations on the [数据集] demonstrate the superiority and effectiveness of [方法] in both [任务1] and [任务2] tasks. | 涵盖多任务验证 |
| 性能对比 | The extensive experiments demonstrate that [方法] outperforms the state-of-the-art methods in [任务]. | 强调SOTA对比优势 |
| 量化优势 | [方法] achieves a [数值] improvement in [指标] compared with the best competing method. | 量化性能提升 |
| 分析发现 | Moreover, our detailed analysis shows that [关键发现/临床意义]. | 补充分析性结论 |

### 6.3.3 意义升华句

| 类型  | 句式模板 | 说明  |
| --- | --- | --- |
| 总结贡献 | In summary, this article provides a/an [形容词] algorithm/framework for [应用场景]. | 全文贡献的精炼总结 |
| 前景展望 | [方法] holds promise for facilitating [临床目标] and warrants further investigation in [研究方向]. | 审慎的前景展望 |
| 转化价值 | The proposed approach has the potential to serve as a clinical decision support tool for [具体场景]. | 临床转化价值 |
| 方法学意义 | This study establishes a new paradigm for [方法学方向] in the context of [疾病/任务]. | 方法学层面的贡献 |

## 6.4 填表示例

### 示例一：基于MDL-Net范式（多模态融合诊断框架）

> In this study, we introduce a novel framework called TransMCI-Net for predicting MCI-to-AD conversion, which integrates cross-modal Transformer encoding and disease-progress-aware attention to comprehensively analyze multimodal neuroimaging data and enhance early diagnostic accuracy. TransMCI-Net designs a multimodal fusion joint learning strategy to capture complementary information across structural MRI, functional MRI, and PET modalities. To further refine the identification of progressive MCI individuals, we propose a disease-progress-aware attention module that adaptively weights brain regions according to their stage-specific pathological relevance. Experimental validations on the ADNI dataset demonstrate the superiority and effectiveness of TransMCI-Net in both MCI conversion prediction and early disease staging tasks, outperforming the state-of-the-art methods by 4.7% in AUC. Moreover, our detailed analysis shows that the identified discriminative brain regions are consistent with established neuropathological knowledge, providing interpretable and clinically meaningful insights. In summary, this study provides an effective and interpretable framework for MCI conversion prediction, holding promise for facilitating early identification of high-risk individuals in clinical practice.

### 示例二：基于CPST-GAN范式（病理驱动生成模型）

> To address current challenges in cross-modality neuroimaging synthesis, this article combines conditional pathogenesis-driven modeling with spatio-temporal adversarial learning to effectively mine disease-specific evolutionary patterns and enhance the quality of synthesized medical images. Specifically, we first propose a CPST-GAN mathematical model based on the pathogenesis of Alzheimer's disease, where the generative process is explicitly conditioned on the known trajectory of neuropathological degeneration. Experimental validations on the ADNI dataset demonstrate the superiority and effectiveness of CPST-GAN in both image synthesis quality and downstream diagnostic accuracy tasks, outperforming the state-of-the-art methods by 6.3% in SSIM and 3.8% in diagnostic AUC. In summary, this article provides a clinically meaningful algorithm for cross-modality neuroimaging synthesis with embedded disease progression prior, offering a promising tool for data augmentation in neuroimaging research.

* * *

# 附录

## 附录一：高频学术词汇与短语速查表

| 类别  | 推荐表述 | 避免使用 |
| --- | --- | --- |
| 性能描述 | achieves superior performance / demonstrates competitive results / yields promising outcomes | works well / does a good job / is very effective |
| 对比描述 | consistently outperforms / shows a clear advantage over | is better than / beats / wins |
| 因果解释 | can be attributed to / can be ascribed to / stems from | because of / is caused by / due to |
| 一致性 | resonates with previous findings / is in good agreement with / aligns well with | matches / is the same as |
| 局限性 | should be acknowledged / necessitates caution / inherent limitation | is bad / has problems / is weak |
| 未来展望 | holds promise / warrants further investigation / represents a promising direction | will definitely / is sure to / for sure |
| 统计描述 | statistically significant (p < 0.05) / reaches a significant level | very significant / really significant |
| 贡献声明 | provides a novel framework / establishes a new paradigm / offers new insights | is very new / is the first (无充分论证时) |

## 附录二：各模块自查清单

### Abstract 自查清单

* [ ] 字数是否控制在 200-250 词范围内？
* [ ] 是否包含 Background -> However -> To address -> Specifically -> Results 五步结构？
* [ ] 是否避免了参考文献引用？
* [ ] 是否避免了主观评价词（very, extremely 等）？
* [ ] 是否包含至少一个具体的量化实验结果？
* [ ] 方法名称是否在首次出现时给出全称？

### Introduction 自查清单

* [ ] 是否在第一段建立了充分的临床动机？
* [ ] 文献引用是否覆盖经典方法与近三年进展（>=15 篇）？
* [ ] 挑战分析是否聚焦且逻辑递进（P3 -> P4）？
* [ ] 方法概述是否清晰描述了核心架构与关键模块？
* [ ] 贡献列表是否为 3-4 条、条目化、以动词不定式开头？
* [ ] 是否避免了在 Introduction 中出现数学公式？
* [ ] 段落间过渡是否自然流畅？
* [ ] 是否避免了口语化表达（如 "a lot of", "kind of"）？

### Related Works 自查清单

* [ ] 开篇是否有总览句，明确综述的维度划分？
* [ ] 每个子节是否形成"列举 -> 不足 -> 引出"的三段式闭环？
* [ ] 引用文献是否覆盖近五年高影响力工作？
* [ ] 是否明确区分已有贡献与尚未解决的问题？
* [ ] 过渡连接词使用是否自然、多样？
* [ ] 是否避免口语化表达（如 "a lot of", "very good"）？
* [ ] 末尾是否有总结段，综合引出本文动机？

### Methods 自查清单

* [ ] 开篇是否有总览段，引用示意图并概述各模块功能？
* [ ] 每个子模块是否遵循"动机 -> 概述 -> 具体设计 -> 小结"四步结构？
* [ ] 所有数学符号是否在首次出现时严格定义？
* [ ] 公式描述是否使用标准句式（"is defined as", "where ... denotes"）？
* [ ] 网络结构描述是否与示意图严格对应？
* [ ] 损失函数是否给出完整数学定义及各符号物理含义？
* [ ] 训练策略是否包含优化器、学习率、batch size、epoch数等关键信息？
* [ ] 是否明确说明本文方法与已有方法的本质区别？
* [ ] 是否避免口语化表达和主观性描述？

### Discussion 自查清单

* [ ] 是否对实验结果进行了深度解读而非简单复述？
* [ ] 每个论断是否有文献支撑或统计证据？
* [ ] 是否包含因果归因分析（can be attributed to）？
* [ ] 可解释性分析是否与临床/生物学知识关联？
* [ ] 局限性是否具体、可操作，对应明确的未来方向？
* [ ] 结尾段措辞是否审慎（holds promise / warrants further investigation）？

### Conclusion 自查清单

* [ ] 篇幅是否控制在 100-150 词？
* [ ] 是否覆盖问题动机、方法概述、实验验证、意义升华四要素？
* [ ] 是否引入了新信息或新引用（应避免）？
* [ ] 是否与Abstract过度重复（应侧重贡献总结）？

## 附录三：常见写作误区

| 误区  | 正确做法 |
| --- | --- |
| Abstract 中引用文献 | Abstract 中不出现任何引用标记 |
| Introduction 第一段直接介绍方法 | 第一段应先建立临床动机，再引出技术需求 |
| 贡献列表超过 5 条或不足 2 条 | 控制在 3-4 条，每条聚焦一个独立创新点 |
| 使用 "very good", "much better" 等模糊表述 | 使用量化指标："improves accuracy by 3.2%" |
| 挑战分析过于笼统（"existing methods have limitations"） | 具体指出哪类方法、哪个环节、为何不足 |
| 贡献列表与方法概述内容重复 | 方法概述讲 "是什么"，贡献列表讲 "为什么新" |
| 忽视过渡连接词，段落跳跃感强 | 使用标准学术过渡词实现逻辑衔接 |
| Discussion 简单复述实验数据 | 对结果进行深度解读与因果归因分析 |
| Conclusion 引入新信息或新结果 | 仅总结已有贡献，不引入新内容 |

* * *

> **模板版本**：v1.0**适用领域**：医学影像分析、深度学习辅助诊断、多模态融合、医学图像生成、脑影像分析、计算神经科学**适用期刊**：IEEE TMI, Medical Image Analysis, NeuroImage, NeuroImage: Clinical, Human Brain Mapping, IEEE JBHI, MICCAI**最后更新**：2026年6月
