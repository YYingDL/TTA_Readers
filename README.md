# TTA_Readers
This is a repository for organizing papers related to domain adaptation.

# Test-time Adaptation

0. ICML  [AdaNPC: Exploring Non-Parametric Classifier for Test-Time Adaptation](https://arxiv.org/abs/2304.12566)(用KNN进行测试时间自适应，从理论上分析了TTA work的原因)[[Code]](https://github.com/yfzhang114/AdaNPC)  [[Reading Notes]](https://zhuanlan.zhihu.com/p/624770864)
1. NeurIPS 2021 [Spotlight] [Test-Time Classifier Adjustment Module for Model-Agnostic Domain Generalization](https://zhuanlan.zhihu.com/p/559916666)(在test的阶段，我们在依然会选择更新模型头部的linear层)
2. CVPR 2021 [Adaptive Methods for Real-World Domain Generalization](https://zhuanlan.zhihu.com/p/559916666)(测试时输入source domain embedding，即test时利用domain信息)
3. ICLR 2021 [Spotlight] [Tent: Fully Test-Time Adaptation by Entropy Minimization](https://zhuanlan.zhihu.com/p/559916666)(测试时最小化模型预测的entropy)
4. ICCV 2021 [Test-Agnostic Long-Tailed Recognition y Test-Time Aggregating Diverse Experts with Self-Supervision](https://zhuanlan.zhihu.com/p/559916666)(测试时优化样本的自监督损失)
5. NeurIPS 2022 [Revisiting Realistic Test-Time Training: Sequential Inference and Adaptation by Anchored Clustering](https://arxiv.org/abs/2206.02721)(发现源和目标域中的集群，并将目标集群与源集群进行匹配，以改进泛化。)
6. NeurIPS 2022 [Test-Time Prompt Tuning for Zero-Shot Generalization in Vision-Language Models](https://arxiv.org/abs/2209.07511)(测试阶段根据最小化预测熵从而更新prompt)
7. NeurIPS 2022 [MEMO: Test Time Robustness via Adaptation and Augmentation](https://arxiv.org/abs/2110.09506)(测试阶段数据增强+最小化熵)
8. NeurIPS 2022 [Test-Time Adaptation via Conjugate Pseudo-labels](https://arxiv.org/abs/2207.09640)(对于现存的有/无监督的TTA loss，可以通过对偶的推导简单的得到最优TTA loss（从广泛的函数类别中进行元学习以获得的最佳的TTA损失），这个loss可以转化为一类特殊的伪标签，被称为 Conjugate Pseudo-labels)
9. CVPR 2022 [Continual Test-Time Domain Adaptation](https://arxiv.org/abs/2203.13591)(从一个源域adapt到一系列连续改变的目标域)
10. Arxiv [A Simple Test-Time Method for Out-of-Distribution Detection](https://arxiv.org/pdf/2207.08210.pdf)(test time adaptation for OOD detection)
11. SIGKDD 2023 [Domain-Specific Risk Minimization for Out-of-Distribution Generalization](https://arxiv.org/abs/2208.08661)(每个域学习单独的分类器，测试阶段根据entropy动态组合)[[Code]](https://github.com/yfzhang114/AdaNPC)[[Reading Notes]](https://zhuanlan.zhihu.com/p/631524930)
12. CVPR 2023 [Improved Test-Time Adaptation for Domain Generalization](https://arxiv.org/abs/2304.04494)(使用一个具有可学习参数的损失函数，而不是预定义的函数)
13. CVPR 2023 [Feature Alignment and Uniformity for Test Time Adaptation](https://arxiv.org/abs/2303.10902)(将TTA作为一个由于源域和目标域之间的域差距而导致的特征修订问题:确保当前批和所有先前批之间的表示之间的均匀性,一致性)
14. CVPR 2023 [TIPI: Test Time Adaptation with Transformation Invariance](https://atuannguyen.com/assets/pdf/nguyen2023tipi.pdf)(为了克服小batch的问题提出了一个新的loss)
15. ICLR 2023 Oral [Towards Stable Test-Time Adaptation in Dynamic Wild World](https://openreview.net/forum?id=g2YraF75Tj)(测试数据流可能具有混合域偏移、小批量和不平衡标签分布shift)
16. ICLR 2023 [Towards Understanding GD with Hard and Conjugate Pseudo-labels for Test-Time Adaptation](https://openreview.net/forum?id=FJXf1FXN8C)(带共轭标签的GD收敛于在高斯模型下任意小误差的最优预测器，而带有传统伪标签的GD在此任务中失败。)
17. ICLR 2023  [Energy-Based Test Sample Adaptation for Domain Generalization](https://openreview.net/forum?id=3dnrKbeVatv)(将目标域数据adapt到源域，利用随机梯度朗之万动力学的能量最小化方法迭代更新样本)
18. ICLR 2023 [Deja Vu: Continual Model Generalization for Unseen Domains ](https://openreview.net/forum?id=L8iZdgeKmI6)(Continual Domain Shift Learning (CDSL))
19. ICLR 2023 [MECTA: Memory-Economic Continual Test-Time Model Adaptation](https://openreview.net/forum?id=N92hjSf5NNh)(目前大多数TTA方法内存消耗比较高因为要反向传播，本文建议减少批处理大小，采用自适应规范化层来保持稳定和准确的预测，并启发式地停止反向传播缓存。另一方面，我们对网络进行修剪以减少优化过程中的计算和内存开销，并在优化后恢复参数以避免遗忘)
20. ICML 2023 Oral [The Price of Differential Privacy under Continual Observation](https://zhuanlan.zhihu.com/p/639174050)(连续适应模型场景下的差分隐私)
21. ICML 2023 Oral [ODS: Test-Time Adaptation in the Presence of Open-World Data Shift](https://zhuanlan.zhihu.com/p/639174050)(同时适应协变量和标签分布的偏移)
22. ICML 2023 [Uncovering Adversarial Risks of Test-Time Adaptation](https://zhuanlan.zhihu.com/p/649295930)(测试批处理中引入恶意样本可能会对最终预测模型的生成产生影响)
23. ICML 2023 [On Pitfalls of Test-Time Adaptation](https://zhuanlan.zhihu.com/p/649295930)(名为TTAB的测试时自适应基准，包含了十种最先进的算法、多样化的分布偏移情况和两种评估协议。)
24. ICML 2023 [Leveraging Proxy of Training Data for Test-Time Adaptation](https://zhuanlan.zhihu.com/p/649295930)(使用训练数据的轻量级且信息丰富的代理方法，并提出了一种完全利用这些代理的测试阶段自适应方法)
25. ICML 2023 [Test-time Adaptation with Slot-Centric Models](https://zhuanlan.zhihu.com/p/649295930)(在场景分解任务中，简单的TTA损失对于任务是不足够的)
26. ICML 2023 [Test-Time Style Shifting: Handling Arbitrary Styles in Domain Generalization](https://zhuanlan.zhihu.com/p/649295930)(将测试样本的样式（与源域存在较大样式差距）转换为模型已熟悉的最近的源域样式，然后进行预测)


