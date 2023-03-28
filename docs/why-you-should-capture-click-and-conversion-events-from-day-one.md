# 为什么每个企业都应该从第一天就捕捉点击+转化事件

> 原文：<https://www.algolia.com/blog/engineering/why-you-should-capture-click-and-conversion-events-from-day-one/>

你知道我们在生意上走得越远，我们用商业语言交谈得就越多吗？我们将开始参考整体概述和一些驱动的方法，我们将不时地接触关于大规模转移前沿范例的基础。

好吧…我确实用了“大规模”这个词。我向那些被我的商业术语困扰的人道歉。

在商业中你会经常听到的一个词是*分析*。因为它经常被用作行话，所以很容易认为它只是“杠杆”或“稳健”等毫无价值的陈词滥调。尽管这个词——分析——是一颗未经雕琢的钻石，一朵荆棘中的玫瑰(好吧，我不说了)。说真的，什么是分析？它们如何明显地影响我构建应用程序的方式？我什么时候应该关心他们？让我们一起来探究答案吧。

## [](#analytics-hone-every-area-of-the-business)分析磨练商业的每一个领域

当你想到这个词时，分析只是指将被分析的数据。你可能会问，我们在这个分析中寻找什么？嗯，完全看情况！精心制作的分析作为许多不同流程的输入数据，包括业务方面和技术方面。

让我们用一个电子商务的例子来探索一下这两个方面。想象一下，你一直在记录一个产品在你的网站上被点击的每一次，以及每一次交易发生的每一次。光是这些数据就足够通用，可以用于各种不同的事情，但它仍然足够适用，在所有这些情况下都有价值。

例如，在业务方面，您可以问自己这样的问题:

*   *是不是有些产品没有任何点击，更别说转化了？*这表明该产品对你的受众没有吸引力，并且/或者无法被发现。
*   *是否有些产品产生的点击量很大，但转化很少？*这可能暗示产品页面或产品当前的展示方式有问题；也可能只是产品本身的一个因素。
*   *是否有些产品几乎总是转化中的唯一产品？*也许这表明该产品更多的是一种冲动购买，甚至在顾客往购物车里添加任何东西之前就购买了。
*   特定产品的大量转化是否可以归因于一个营销渠道？这里的明显效果是，如果是这样，我们应该做更多的营销！
*   *我们网站上的哪些页面最擅长将点击转化为转化率？*好吧，那么让我们找出是什么让这些页面成为转换机器，并将这种逻辑应用到其他地方。
*   *某些产品是否比你预期的更受季节性关注？*那么，或许你与该商品相关的营销应该比现在更适应季节变化。
*   *用户在转换前点击了多少产品？如果这个数字很高，这可能表明你的产品页面转换得不够好，或者你的应用程序的结构使得很难找到潜在客户想要的产品。*
*   *回头客会一直搜索相同的商品吗？也许把这些物品放在最前面和最中心是个好主意，这样他们在重复购买时就不会有摩擦了！*
*   *潜在转化被放弃的频率有多高？*同样，如果这个数字很高，这表明您的应用程序流程降低了潜在客户的速度，打消了他们的兴趣。

看看这些问题是如何得到不仅仅是商业人士的答案的？当我们在像 [Algolia](https://www.algolia.com/) 这样的灵活系统中从第一天开始跟踪点击和转换事件时，我们就可以“整体地”改善我们的业务——换句话说，跟踪分析使业务全面改善。

## [](#analytics-can-be-input-data-for-new-features)数据分析可以为新功能输入数据

人工智能是我们现在用来解决电子商务中复杂问题的最大工具之一。比如 [Algolia 推荐](https://www.algolia.com/products/recommendations/)可以(顾名思义)根据之前的一些数据，向用户推荐产品、内容或者类别。如果他们喜欢现在正在看的产品，我们可能会向他们推荐他们喜欢的产品，或者推荐那些经常与他们正在看的产品一起购买的产品。无论哪种方式，我们都需要输入数据来训练我们产品目录上的人工智能，我们这样做的方式是向 Algolia 发送点击和转换事件！

请注意，不同的功能需要不同数量的训练数据。例如，Algolia 让您 A/B 测试不同的索引设置，但只有当您有办法测量结果时才有意义。输入分析。当您从一开始就发送点击和转换事件时，A/B 测试可以定量地测量对您的搜索索引配置的轻微调整的影响。这意味着我们拥有的数据越多，我们对应用程序的影响就越大。个性化也是如此——如果我们没有任何关于用户行为的数据，那也没关系！我们不会以任何方式将结果个人化。但是我们掌握的用户行为数据越多，我们就能更好地调整搜索结果，使其更有可能反映用户偏好。

另一方面，如果没有至少一些数据，如何创建一个经常一起购买的部分呢？你不能只显示随机结果，因为很明显它们是随机的——例如，如果你经营一家技术经销商，你最终会说 iphone 通常是按照 Galaxy 手机的顺序购买的，而更合适的建议是充电器或手机壳。Algolia 可以为我们处理“经常一起购买”部分——通过在过去 30 天内与多种产品共享至少 1，000 次转换事件(在我们的示例中为结账),我们就可以开始了。

相关产品是电子商务网站通常应该有的部分。由于 Recommend 的混合动力引擎，您可以从第一天开始根据您记录中的信息进行相关产品推荐。但是，为了真实地反映用户的行为，你需要事件数据——过去 30 天的 10，000 次点击或转换足以让 Algolia 对产品之间的一般关联做出准确的结论。但是，如果您从第一天开始跟踪点击事件，那么当您选择实现这个相关产品部分时，您可能已经拥有了在 Algolia 中训练模型所需的数据，这样您就可以立即前进。

## [](#analytics-can-save-you-from-future-headaches)分析可以让你免除未来的头痛

实话实说吧。如果你是开发人员，你的经理会要求你在某个时候实现一些分析系统。如果你是经理，你知道你会提出要求。然而在许多代码库中发生的问题是，不同的分析以不同的方式被跟踪，因为它们在不同的时间被实现并且用于不同的目的。通常，相同的事件会在多个分析系统中重复出现，这种情况会被所有相关人员所鄙视。我们如何避免这个难题？

下面简单回答:**从第一天**开始尽可能多的跟踪。

[这个简单的指南](https://www.algolia.com/doc/guides/sending-events/planning/)能帮上忙，要点如下:

*   分解用户交互中可能发生在页面上的每一件小事。
*   尽可能详细，最好在事件本身中包含足够的信息，甚至可以通过编程重现事件。
*   建立一个系统，这样你就可以从用户到达你的网站的那一刻起，到他们离开的那一刻，真实地跟踪他们的每一个选择。
*   不要忘记在你的主站点之外的交互点跟踪事件，比如电子邮件、广告、推送通知，或者跨不同的域/子域属性。
*   *不嫌*多有意义的事件！绝对不要为用户滚动的每一个像素发送一个事件，但是如果他们停留在网站的某一部分，那就有意义了！将它事件化！

在未来，您将最终实现更多需要分析的功能，但您已经拥有了这些数据。您可以随时过滤掉分析仪表板中您不关心的额外数据，但您可以放心地知道，无论何时您或其他人需要这些数据，它们仍然存在。你永远不必重新实现分析的概念，或者在不同的平台之间划分你的事件数据。在分析您的业务表现时，您将永远不必担心考虑重复事件，并且您将始终拥有足够的数据来准确地为您的客户流建模。

## [](#what-have-we-learned)我们学到了什么？

*   虽然有些人谈论分析就像另一个陈词滥调的商业术语，但它实际上是一个非常有用的概念，应该立即在您的应用程序中实现。
*   您将来想要实现的功能可能取决于您是否已经拥有可用的分析数据。
*   对于不同的特性和使用不同的平台，你可能最终会实现一些度量跟踪工具很多次——所以通过提前计划和现在存储一切，你会为自己节省很多工作。
*   Algolia 是存放所有物品的好地方！如果你更喜欢将你的分析数据存储在其他地方，但想要 Algolia 的仪表板和人工智能驱动的搜索的好处，也有针对 [GTM](https://www.algolia.com/doc/guides/sending-events/implementing/connectors/google-tag-manager/) 和[细分市场](https://www.algolia.com/doc/guides/sending-events/implementing/connectors/segment/)的插件。

如果您已经做到了这一步，我敢打赌您已经准备好开始跟踪您的应用程序中的点击和转换。这里是[注册 Algolia](https://www.algolia.com/users/sign_up) 的链接，这里是[帮助你实现这个](https://www.algolia.com/doc/guides/sending-events/getting-started/)的详细指导指南。如果您还没有在现有的应用程序中走过这条路，请不要担心——现在是您走上正确道路的机会了(我们不会告诉任何人😉).