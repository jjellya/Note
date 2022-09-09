# [DeepDive](http://deepdive.stanford.edu/#documentation)

> 
>
> 该系统利用知识库的已有知识构建正例和反例数据，进行相应的特征提取，根据这些特征从经过预处理的测试文本中抽取候选实体关系对，最后利用因子图的方式计算出该实体对属于某种关系的可能性，经过对可能性的排序得到最后的实体间的关系。现如今主要研究从异构的非结构化文本、视频、语音等数据中进行隐藏信息的挖掘，抽取其中的真实信息形成知识，对知识进行整理分析并进行统一的建模，并以结构化的形式输出的一种自然语言文本处理技术。
>
> 
>
> <p align="right">——赵骁雅</p>



DeepDive 是一种新型的数据管理系统，可以在单个系统中解决提取、集成和预测问题，它允许用户快速构建复杂的端到端数据管道，例如暗数据 BI（Business Intelligence) 系统。

通过允许用户端到端构建他们的系统，DeepDive 允许用户专注于最直接提高应用程序质量的系统部分。

相比之下，以前的基于管道的系统要求开发人员构建提取器、集成代码和其他组件，而对他们的更改如何提高数据产品的质量没有任何清晰的认识。

这种简单的洞察力是 DeepDive 系统如何在更短的时间内产生更高质量数据的关键。

没有机器学习专业知识的用户在从古生物学到基因组学到人口贩运等多个领域使用基于 DeepDive 的系统；

有关示例，请参见我们的 [showcase](http://deepdive.stanford.edu/showcase/apps)。



DeepDive 是一个**经过训练的系统**，它使用机器学习来应对各种形式的噪音和不精确。 

DeepDive 旨在让用户通过 [Mindtagger 界面](http://deepdive.stanford.edu/labeling) 的低级反馈和通过规则的丰富、结构化的领域知识来轻松地训练系统。 

DeepDive 希望为不具备机器学习专业知识的专家提供支持。 

DeepDive 的一项关键技术创新是能够大规模解决统计推断问题。

DeepDive 在几个方面与传统系统不同：

- DeepDive 要求开发人员**考虑功能，而不是算法**。（PS：正如它的官网标题如图1所示）
- 相比之下，其他机器学习系统则需要开发者考虑使用哪种聚类算法、哪种分类算法等。在 DeepDive 的基于联合推理的方法中，用户只指定必要的**信号或特征**。
- DeepDive 系统可以实现高质量：PaleoDeepDive 在提取[科学领域](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0113523)的复杂知识方面**高于人类志愿者**和在**[实体关系提取竞赛](http://i.stanford.edu/hazy/papers/2014kbp-systemdescription.pdf)**中的表现。
- DeepDive 意识到**数据通常是嘈杂且不精确的**：名称拼写错误，自然语言模棱两可，人类会犯错误。考虑到这种不精确性，DeepDive 计算它做出的每个断言的 [校准](http://deepdive.stanford.edu/calibration) 概率。例如，如果 DeepDive 产生一个概率为 0.9 的事实，则该事实有 90% 的可能性是真实的。
- DeepDive 能够使用来自**各种来源**的大量数据。使用 DeepDive 构建的应用程序已从数百万个文档、网页、PDF、表格和图形中提取数据。
- DeepDive 允许开发人员**使用他们对给定领域的知识**，通过 [编写简单的规则](http://deepdive.stanford.edu/writing-model-ddlog) 来提高结果的质量，从而通知推理（学习过程。 DeepDive 还可以考虑用户对预测正确性的反馈，以改进预测。
- DeepDive 能够使用数据[“远程”学习](http://deepdive.stanford.edu/distant_supervision)。相比之下，大多数机器学习系统都需要对每个预测进行繁琐的训练。事实上，许多 DeepDive 应用程序，尤其是在早期阶段，根本不需要传统的训练数据！
- DeepDive 的秘诀是**可扩展的高性能推理和学习引擎**。在过去的几年里，我们一直在努力让底层算法尽可能快地运行。该项目中首创的技术是商业和开源工具的一部分，包括 [MADlib](http://madlib.net/)、[Impala](http://www.cloudera.com/content/cloudera/en/products -and-services/cdh/impala.html)，来自 [Oracle](https://blogs.oracle.com/R/entry/low_rank_matrix_factorization_in) 的产品，以及低级技术，例如 [Hogwild!](http://i.stanford.edu/hazy/papers/hogwild-nips.pdf)。它们也被[Microsoft's Adam](http://www.wired.com/2014/07/microsoft-adam/) 和其他主要网络公司收录。

For more details, check out [our papers](http://deepdive.stanford.edu/papers).

![deepdive](DeepLive.assets/deepdive.png)