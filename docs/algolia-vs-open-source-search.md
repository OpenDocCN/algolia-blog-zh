# 开源搜索工具与 Algolia 

> 原文：<https://www.algolia.com/blog/product/algolia-vs-open-source-search/>

如果你的网站需要一个搜索工具来匹配你的用例，你有两个选择:从头构建一个内部搜索引擎或者从搜索提供商那里购买。您可能会担心开箱即用的解决方案对于您的规格来说过于死板。然而，构建您自己的工具可能需要您没有多余的资源。

无论你决定走哪条路，你都需要确保你的业务需求和那些重要的利益相关者的需求，比如项目经理、开发人员和最终用户，以最有效的方式得到满足。

在本文中，我们将评估搜索即服务工具 Algolia，以及流行的开源工具 ElasticSearch 和 Solr，看看购买或构建是否适合你。

## [](#what-is-open-source-search)什么是开源搜索？

开源搜索是通过免费的开源软件实现的，该软件旨在处理许多不同的用例。通常，该软件受 Apache 或 [MIT 许可证](https://tldrlegal.com/license/mit-license) 管辖，这实际上允许任何商业或个人使用。虽然这提供了灵活性，但像 ElasticSearch 或 Apache Solr 这样的流行开源软件仍然需要大量的技术专业知识来构建特定于用例的行业标准搜索应用程序。

## [](#what-is-search-as-a-service)什么是搜索即服务？

搜索即服务是通过软件即服务(SaaS)模式实现的。有了 [搜索即服务](https://blog.algolia.com/what-is-search-as-a-service/) ，搜索功能、托管、运营、维护等都由软件提供商提供。特别是 Algolia，它具有像 [即时搜索](https://www.algolia.com/products/search-and-discovery/ui-component-libraries/) 这样的功能，多语言功能，以及内置在可定制搜索界面中的错别字容差，该界面旨在随着业务的增长而扩展。

## [](#build-vs-buy-for-search)构建与购买搜索

是建立还是购买你的内部搜索工具取决于几个关键的考虑因素

*   您需要的搜索定制的级别和类型
*   开发资源的可用性
*   构建搜索的预计时间表

一旦你概述了你最终需要的搜索结果，评估了你现有的资源，你就能更好地决定走哪条路。

## [](#why-build-your-search%c2%a0)为什么要建立你的搜索？

建筑搜索是一个耗费时间和资源的过程，并不适合所有人。虽然可定制性的级别看起来很有吸引力，但是构建只对少数类型的公司有意义。

将搜索作为其产品或功能的关键部分的资源丰富的公司(想想谷歌或亚马逊)可能会走这条路，因为他们可以投入整个团队来开发、实施和维护他们的搜索。此外，规范非常严格的公司或需要开发不太常见的搜索类型(例如，视觉搜索)的公司可能会选择构建。然而，绝大多数公司不属于这些类别。

### [](#the-benefits-of-open-source-search)【开源搜索的好处】

开源软件在开发者社区中很受欢迎。对于构建搜索应用程序来说，它有很多好处:

*   **初期成本低。** 开源搜索需要最低的前期成本，因为它可以免费下载，并在构建和测试时在本地运行。
*   **社区支持** 。世界各地的软件工程师都在使用和开发开源搜索工具。在线社区可以成为工程师进行功能开发的重要资源。
*   **灵活部署** 。开源搜索工具也可以在许多不同的环境下运行。无论您是在构建一个小型的内部搜索工具，还是一个大型的分布式企业云搜索系统，这些工具都可以进行扩展，以满足大多数条件。此外，AWS 和 Google Cloud 等云提供商提供了一些基础设施来帮助部署和配置软件。

### [](#the-challenges-of-open-source-search)开源搜索的挑战

虽然开源工具提供了巨大的开发灵活性，但它们也带来了一些挑战:

*   **总拥有成本高。楼宇搜索包含许多隐性成本，包括持续维护成本和托管成本。请记住，将整个工程师团队投入到设计和维护你的搜索中，将会使公司每年花费数十万美元！**
*   **技术复杂** 。开源工具通常需要大量的定制开发工作才能应用于特定的用例。这意味着开发人员必须很好地理解工具如何在幕后工作，以确保正确使用，并且任何特定于业务的逻辑或 API 都必须从头开始构建。
*   **延长实施时间表。** 与业务团队在优先级、构建、测试和启动搜索方面保持一致需要几个月的时间，即使你的开发团队技术高超。
*   **搜索的更新和改变需要密集的计划。一旦你的搜索上线，即使对你的搜索工具做很小的修改也需要许多利益相关者的配合。搜索算法的改变，增加新的排名因素，或者开发新的功能可能会比你想象的要长得多。**
*   监控和维护会消耗资源。随着业务的增长扩大搜索范围会占用开发者大量的带宽。花在监控和维护搜索上的时间会抑制其他领域的创新和发展。
*   对于企业用户来说，搜索是一个黑匣子。 由于开发人员将完成搜索的大部分设计工作，业务团队可能很少或根本不了解为什么项目、内容和/或产品会以这样的方式排名。
*   **不包括分析。分析对于推动搜索工具的改进和调整至关重要，但它们不会自动包含在开源软件中。请确保将您的分析工具或数据可视化工具的成本包括在您的搜索总成本中。**

## [](#why-buy-a-search-as-a-service-solution)为什么要购买搜索即服务解决方案？

大多数公司几乎没有开发资源来从零开始开发搜索引擎。然而，增加搜索功能可以极大地改善普通网站用户的体验。事实上， [43%的用户会立即去网站上的搜索栏](https://www.forrester.com/report/MustHave+eCommerce+Features/-/E-RES89561) 。从媒体到电子商务，再到中间的每一个网站，在线公司必须提供符合谷歌、亚马逊、网飞和其他主要参与者设定的标准的搜索体验。购买托管搜索即服务解决方案可能是改善用户体验同时保持可承受成本的有效方式。

### [](#the-benefits-of-search-as-a-service)搜索即服务的好处

搜索即服务工具旨在最大限度地降低搜索启动和运行的复杂性。以下是购买搜索即服务解决方案的一些好处，以及 Algolia 如何帮助您实现这些好处:

*   **开箱即用的可定制搜索 UI。** Algolia 提供了一系列现成的可定制搜索 UI 组件。 [联合搜索](https://blog.algolia.com/what-is-federated-search/) 、随键入搜索自动完成、过滤器和方面、 [个性化](https://blog.algolia.com/personalization/) 和销售工具立即可用，帮助您以最快的速度构建强大的搜索。
*   **内置分析。每次搜索，Algolia 都会捕获有价值的用户数据，并将其显示在 [一个可消化的分析仪表板](https://www.algolia.com/products/search-and-discovery/analytics/?tab=no-results) 中。无需额外费用，您可以轻松查看重要指标，如点击位置、点击率、热门搜索、无结果热门搜索、搜索来源国家，并使用这些信息来推动[](https://blog.algolia.com/internal-site-search-analysis/)。**
*   **可靠性和可扩展性。** 如果你从头开始构建，你的开发者最终将不得不管理系统备份并解决网络延迟和搜索中断的问题。Algolia 的 [分布式搜索网络消除延迟](https://blog.algolia.com/distributed-search-network-latency-ruins-search-experience/) 。凭借 99.999%的 SLA(适用于具有 1000 倍折扣政策的精选计划)，Algolia 网站上始终提供当前 API 状态。
*   利用即时创新。得益于“搜索即服务”模式，Algolia 的新产品功能、升级和改进可立即提供给所有用户，无需额外付费。
*   白盒方法。阿果的 [排名公式](https://www.algolia.com/doc/guides/managing-results/relevance-overview/in-depth/ranking-criteria/) 对所有人都是透明的。此外，像 [可视规则编辑器](https://www.algolia.com/products/search-and-discovery/visual-merchandising-curation/) 这样的工具，允许商业用户基于商业优先级对搜索排名进行改变和改进，所有这些都不需要开发者的帮助。
*   更低的拥有成本。使用 Algolia 的持续成本是合理且可预测的，并且没有任何隐藏的维护、托管或升级成本需要担心。

### [](#the-challenges-of-search-as-a-service%c2%a0)搜索即服务的挑战

虽然“搜索即服务”模式提供了许多好处，但也有一些挑战需要考虑:

*   **不太适合技术性极强的工作流程。Algolia 是面向用户搜索的理想产品。如果你的重点是分析/日志处理，你可能需要一个不同的工具。**

*   一些灵活性的损失是不可避免的。如果你不是从零开始，你将无法控制搜索的每一个细节。然而，Algolia 是高度可定制的，适用于大量的用例，并旨在成为您用例的合作伙伴。

*   可能很难转换供应商。当你作为服务提供商使用搜索工具时，你可以根据自己的需求调整工具，生成有价值的搜索数据。如果您需要切换到一个新的合作伙伴，将您的所有数据和规范移植到另一个供应商可能需要一些工作。

## [](#choose-the-best-partner-for-the-search-experience-you-want-to-create)为您想要创造的搜索体验选择最佳合作伙伴

虽然从头开始构建新的应用程序很有诱惑力，但从长远来看，这看起来在短期内节省了成本，实际上却花费了更多的时间和金钱。大多数公司会在托管解决方案中找到他们需要的工具。如果你决定选择搜索即服务，你需要一个强大的合作伙伴，在你成长的过程中与你并肩作战。 [观看我们的深度演示](https://go.algolia.com/deep-dive-demo) ，了解 Algolia 如何应对开源替代方案。