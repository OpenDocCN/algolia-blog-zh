# 什么是个性化推荐？

> 原文：<https://www.algolia.com/blog/ux/what-are-personalized-recommendations-and-how-can-they-boost-engagement-and-conversion/>

如果你不得不在没有首先查看你的个性化推荐的情况下做出网上商店(甚至实体商店)的购买决定，那会怎样？你知道，那些数据科学驱动的相关产品的营销想法，专为你而想。这些电子商务网站对相关产品的推荐基于机器学习智能，这些智能是由关于用户行为和购买历史的输入数据产生的。

如果连一个 *基于人工智能的推荐都没有，比如“你可能会喜欢…”或“看看这些受欢迎的产品”或“喜欢这个的人也喜欢…”会怎么样？连一句“经常一起买”都没有*

嗯。你会觉得有点失落。你会对购买该商品感到矛盾，即使它的伟大功能在专业的图片中有详细的描述，营销文案很有吸引力，网站宣传免费退货。

然而，如果网站的产品推荐引擎 主动地、全心全意地主动推荐特定的产品，因为它本质上知道你想要什么，你就不会犹豫了。

基于深度学习的推荐系统肯定会让网上购物变得更容易，不是吗？

## [](#personalized-product-recommendations-work)个性化产品推荐工作

针对购物者和媒体网站订阅者的深度学习生成的推荐已经成为电子商务发现和购买体验不可或缺的一部分。为了使你的网站指标获得最大的成功，你需要确定正确的产品推荐模型。事实上，在 [的一项调查](https://www.invespcro.com/blog/e-commerce-product-recommendations/) 中，54%的零售商声称产品推荐功能作为 *的关键驱动因素* 的平均订单价值更高。

每个人都知道，像亚马逊和网飞这样的大公司在个性化推荐方面设立了很高的标准——这种量身定制的指导是人们现在所期望的，即使他们只是浏览较小公司的网站，这些公司没有同样的能力来实施或预算最先进的数字资源和功能。

有了网购，一个相关的推荐就能改变一切。就像一个个人购物者在你喜欢和不喜欢的每一个方面接受教育一样，推荐功能会为你进行搜索，搜索网站以找到你可能想要的信息检索，然后在适当的时候礼貌地建议你可能想要查看一下。

所以，是的，你要提供正确的推荐，让你的顾客感受到在你的网站上购物的乐趣。你想展示他们愿意考虑的产品。你希望他们习惯于考虑你的建议，然后回来。

客户保留是利用个性化推荐的一个有据可查的好处。2018 年 Monetate [的一项研究](https://www.insiderintelligence.com/content/the-impact-of-product-recommendations) 发现，55%的零售网站回头客在购物期间更有可能购买推荐的产品(如通过阅读产品描述)。对于新客户呢？ *高达 70%。*

## [](#what-is-a-personalized-recommendation)什么是个性化推荐？

简而言之，在线个性化推荐是由推荐引擎(又称为 [推荐系统](https://www.algolia.com/blog/product/what-is-a-recommender-system-recommendation-engine/) )基于对客户现场参观的了解，使用算法和过滤选项生成的相关建议。前瞻性线索:

*   他们输入了什么搜索查询？
*   他们的浏览历史是怎样的？
*   他们最近买了什么？
*   还有哪些项目可以补充他们一直在看的东西？
*   其他购物者购买了哪些他们似乎想要的商品？
*   他们的购物车里有什么，他们有没有抛弃？
*   他们是否在社交媒体上分享了某件物品的一些信息？
*   在在线电影订阅网站模式中，他们在看什么？
*   他们的人口统计是怎样的？

### [](#types-of-product-recommendations)产品类型推荐

推荐引擎必须对所有可用的数据进行分类，并给出他们对推荐内容的最佳猜测。有三个不同的焦点:

### [](#collaborative-filtering-systems)协同过滤系统

这种类型的推荐引擎收集并分析用户活动和偏好的数据，根据用户与其他用户的相似性推测用户的喜好。有趣的是，内容本身(物品、书籍或电影)不在考虑之列。这种方法以矩阵形式的公式为基础，在具有相似偏好的人群中应用有关用户偏好的逻辑，并根据早期活动进行预测。

协作过滤有两种方式:基于记忆和基于模型。

基于记忆的 协同过滤识别用户群，并查看用户交互来预测相似用户的交互。它还识别由用户 A 评级的项目群，然后使用它们来预测用户 A 与相似项目 b 的交互

依靠机器学习和数据挖掘， **基于模型** 协同过滤专注于训练模型进行预测。例如，它可能使用与某个项目的交互来预测喜欢的项目。它可以向更多的人推荐更多的商品

比基于记忆的协同过滤。

### [](#content-based-filtering-systems)内容过滤系统

当你看到“如果你喜欢那个，你可能也会喜欢这个”时，或者如果你几周前看了某个东西，而你现在得到一个提示来查看类似的项目时，你知道过滤是基于内容的。对于基于内容的推荐，相似的项目根据特征进行分组。推荐算法着眼于顾客偏好加上商品描述(例如，流派、类型、颜色)。

### [](#hybrid-recommendation-systems)混合推荐系统

当您可以享受 *两者的好处时，为什么只利用内存或只利用内容协同过滤？* 网飞就是这样做的。它考虑了用户的兴趣(协同过滤)以及电影描述和特征(基于内容的过滤)。

## [](#how-can-you-use-personalized-recommendations-to-lift%c2%a0-engagement-conversion-and-performance)如何利用个性化推荐来提升参与度、转化度和绩效？

合适的定制推荐可以让你的网站与众不同。当您可以使用大数据来打动客户并让客户满意时，您就实现了参与的崇高目标。足够的持续参与会带来网站绩效的提升。

当然，最终的回报是更高的转换率，这是因为你从客户开始搜索到他们在购物车页面上前进的过程中，不断努力适应他们的需求，无论他们是否意外地放弃了购物之旅，或者购买了多种额外的推荐产品，然后第二天又回来寻找更多产品。最终，使用个性化推荐对零售商和购物者都是双赢的。

### [](#what-do-we-recommend-for-you)我们为 *的你推荐什么？*

因为你已经和我们在一起这么久了，所以你很可能对添加直观的推荐感兴趣。是时候为你的网站寻找最佳的推荐方案了。你可能想知道，除了我们著名的 [搜索技术](https://www.algolia.com/products/search-and-discovery/hosted-search-api/) 之外，这也是我们在 Algolia 专攻的功能。

我们久经考验的电子商务推荐系统可以做到这一切:实现快速、可扩展的产品发现，促进一流的用户参与，确保重复的客户访问，并最大限度地提高转化率。我们的相关内容模型使用混合引擎以及协作过滤和用户信号来提供高质量的推荐。

你可以将用户推荐显示在最合适的地方，无论是在产品页面、主页还是产品类别页面。你甚至可以整合 [推荐](https://www.algolia.com/products/recommendations/) 在结账时展示互补产品，以增加你的平均订单价值。您的开发人员可以利用我们可靠的 API 来构建和完善您的最佳推荐体验。

使用“推荐”功能推荐不同颜色和功能的类似产品，有助于人们继续寻找相关信息，最终做出最佳选择，而不必在主页上重复搜索。我们怎么知道推荐对于构建增强个性化体验的推荐系统来说是一个非常好的选择呢？在客户数据的帮助下，我们收集了一些令人信服的统计数据。

战略性地推荐使用，提高每个接触点的客户参与度。我们已经计算出这会导致一个:

*   订单率增长 150%
*   篮子增加 20%
*   整体站点转化率增加 13%
*   跳出率降低 24%

当然电子商务商店 *喜欢* 推荐商品，但是像电影推荐这样的事情呢？无论您处于哪个行业，也无论您最关注的是更高的购物车价值、更好的客户保持率还是更高的转化率，您都可以提供令人愉快的用户体验优化，并取得成效。Algolia Recommend 将根据有监督的机器学习算法，从您的索引和用户事件中专业地构建模型。

让我们来聊聊 Algolia 的推荐如何帮助你提升客户体验以及 [发展业务](https://www.algolia.com/blog/product/why-we-recommend-recommend-to-make-recommendations/) 。我们会给你一个 [个性化演示](https://www.algolia.com/demorequest/) ，你可以 [免费试用我们](https://www.algolia.com/users/sign_up) ，每月有 10，000 次推荐请求。了解如何通过正确的推荐策略增加流量和销售额。谁知道呢？像我们的许多客户一样，你可能很快就会显著改善你的顾客之旅，然后亲自推荐 Algolia。