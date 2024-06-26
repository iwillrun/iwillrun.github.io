---
layout: post
title: LLM-based Agent,为大模型的应用落地开辟一个新的战场
categories: [AI应用]
description: LLM-based Agent,为大模型的应用落地开辟一个新的战场
keywords: AI agent，LLM-based Agent，AI应用落地，智能体系统，智能体应用，AI agent设计方法
mermaid: false
sequence: false
flow: false
mathjax: false
mindmap: false
mindmap2: false
---

最近哈佛团队在AI agent的应用场景上又有了新的进展，在自动化社会科学和人类行为建模方向实现新的突破。
其中“科学家Agent”承担起提出因果假设、设计实验的重任。
接着定制化创建“普通人Agent”，这些虚拟代理在精心构造的实验环境中代替真人参与各类社会科学研究。
实验数据随后自动采集，系统性地验证假设，形成闭环。
这一框架展示了社会科学问题自动化探索的潜力，成功应用于讨价还价、税务诈骗保释听证、律师面试及艺术品拍卖等多种场景中。

**论文地址** ：[https://arxiv.org/abs/2404.11794](https://arxiv.org/abs/2404.11794)

**解决问题**:在传统社会科学领域，进行面试、拍卖、产品测试、保释听证会等场景的模拟测试需要招募真人参与，过程费时费力且成本高昂，有的场景根本不能进行实验。团队利用 LLM-based Agent 作为人的近似模型，提出了一种通用的自动化实验方法，实现低成本高效的社会实验测试，最终能对公共政策等宏观测试有进一步促进作用

**模型框架**：团队对科研人员和普通人进行建模，演示了社会科学问题的自动化探索。这个流水线由“科学家 Agent”提出因果假设，设计实验，建造符合实验设定的“普通人 Agent”替代真人进行实验，到完成各种场景的社会科学模拟实验，最终数据自动收集，并且检验假设

**使用效果**：论文的结果表明，完全自动化实验的方案可以快速地进行大量社会学实验，并且获得对于新的因果关系的洞见，这些新的知识反过来也可以改进大语言模型本身对于人类行为的理解

**应用空间**：各种社会科学和经济学测试场景，论文展示了讨价还价、税务诈骗保释听证会、律师面试、私人藏品拍卖等场景

#### 模型框架的创新逻辑

该研究构建了一条从理论到实践的自动化流水线，其中“科学家Agent”承担起提出因果假设、设计实验的重任，接着定制化创建“普通人Agent”，这些虚拟代理在精心构造的实验环境中代替真人参与各类社会科学研究。实验数据随后自动采集，系统性地验证假设，形成闭环。这一框架展示了社会科学问题自动化探索的潜力，成功应用于讨价还价、税务诈骗保释听证、律师面试及艺术品拍卖等多种场景中。

#### 实验效果与洞见

论文结果显示，全自动化实验平台不仅加速了社会学实验的进程，还揭示了新因果关系，这些新知反过来促进了对大语言模型理解人类行为能力的提升。这意味着，我们正逐步迈向利用AI技术深化人类自我认知的新时代。

#### 应用前景与挑战

该技术在社会科学和经济学测试领域的广泛应用，预示着研究方式的革命。然而，实现这一愿景还需克服多模态交互的限制和确保模型能准确反映非理性行为等人类特质。此外，数据代表性问题也不容忽视，当前模型多偏重WEIRD群体，限制了其普适性。如何确保模型在多样性和真实性之间取得平衡，是未来研究的关键。

PS:WEIRD:(Western,  Educated, Industrialized, Rich, Damocratic）) 西方世界中产阶级群体

#### 结构因果模型（SCM）与Agent应用

论文采用Judea Pearl提出的结构因果模型，将复杂的社会现象简化为节点与连线的图示，清晰展现变量间因果关系，增强了实验设计的严谨性。通过精心设计的Agent，实验可模拟特定情境下的互动，如在马克杯讨价还价案例中，精准捕捉了价格、预算及情感依恋等因素对交易结果的影响，展现了LLM在模拟人类决策行为方面的潜力。

#### 进一步思考

关于AI Agent的讨论和应用已经越来越多了，目前大多数方向都是通过AI agent来替代一部分重复、有固定模式的人工工作，这种使用AI agent直接对整个人类角色进行建模的想法虽然有，但讨论不多。

这种使用agent直接对人类行为建模的应用前景也确实广泛。比如：

- 对目标客户进行建模，可以低成本的创建虚拟目标客户，不管是获取实施的用户画像还是测试用户反映都有帮助。
- 对目标客户进行建模，通过训练一部分收集到的目标客户数据，可以实时预测用户未来的可能反应，在产品推荐领域是一条新的途径
- 对工作人员进行建模，同时对客户进行建模，两者进行对抗训练，不断增强自身能力范围。
- 对一个小型社会生态进行建模，研究这种变量对人类社会的影响

