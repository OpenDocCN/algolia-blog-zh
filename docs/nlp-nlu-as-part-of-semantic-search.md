# 作为语义搜索一部分的自然语言处理和 NLU-Algolia 博客

> 原文：<https://www.algolia.com/blog/ux/nlp-nlu-as-part-of-semantic-search/>

NLP 和 NLU——这两项(经常被混淆的)技术让搜索变得更加智能，并确保人们可以搜索和找到他们想要的东西，而不必像在页面或产品中一样键入准确的单词。

NLP 和 NLU 就是为什么你可以输入“礼服”并找到那件长期受欢迎的“NYE 派对礼服”，也是为什么你可以输入“马修·麦康纳”并让麦康纳先生回来。

NLP 代表“自然语言处理”它是那些已经建立了如此大的意义的事情之一，以至于很容易忽略它告诉你它到底是什么的事实:NLP *处理* 自然语言，特别是转换成计算机可以理解的格式。这些类型的处理可以包括诸如规范化、拼写纠正或词干分析之类的任务，我们将更详细地研究每一项。

NLU 代表“自然语言理解”这项技术旨在“理解”一组自然语言在交流什么。例如，它执行的任务可以识别句子中的动词和名词或文本中的重要项目。然后，人们或程序可以使用这些信息来完成其他任务。

电脑看起来很先进，因为它们可以在短时间内做很多动作。然而，在很多方面，计算机是相当愚蠢的。他们需要以特定的方式构建信息，并以此为基础。对于自然语言数据，这就是 NLP 的用武之地，因为它获取杂乱的数据(自然语言可能非常杂乱)，并将其处理成计算机可以处理的东西。

### [](#text-normalization)文字规范化

当搜索者在搜索栏中输入文本时，他们试图找到一个好的匹配，而不是玩“猜测格式”例如，要求用户以与记录中匹配单词完全相同的格式键入查询，这是不公平的，也是徒劳的。我们使用文本规范化来消除这个需求，这样无论文本来自哪里，它都是标准格式的。

随着我们经历不同的标准化步骤，我们将会看到没有一种方法是人人都遵循的。每个标准化步骤通常会增加召回率并降低精确度。

一个小题外话:“召回”是指搜索引擎找到已知的好结果。精确意味着搜索引擎只能找到好的结果。通过返回索引中的每一个文档，搜索结果可以有 100%的召回率，但精确度会很差。相反，一个搜索引擎可以有 100%的精确度，只返回它确信完全匹配的文档，但是一些好的结果可能会被错过。

同样，标准化通常会提高召回率，降低精确度。向 *召回精度谱* 一端的移动是否有价值取决于用例以及搜索技术，因此这不是应用所有规范化技术的问题，而是决定哪些技术提供了精度和召回的最佳平衡。

#### 字母规范化

您能想到的最简单的规范化就是处理字母大小写。至少在英语中，单词一般在句首大写，偶尔在标题中大写，当是专有名词时大写。(也有其他规则，看你问谁了。)但在德语中，所有名词都是大写的。其他语言有自己的规则。

这些规则是有用的，否则，我们不会遵守它们。例如，将句子的第一个单词大写有助于我们快速看到句子从哪里开始。然而，这种有用性在信息检索环境中被削弱了。单词的意思不会因为它们出现在标题中并且首字母大写而改变。

更棘手的是，这里有规则，还有人们实际上是如何写作的。如果我发短信给我妻子，“有人撞了我们的车！”，我们都知道我说的是一辆车，而不是因为这个词大写而有所不同的东西。通过思考有多少人在非正式交流时根本不使用任何大写字母 — 我们可以清楚地看到这一点，顺便提一下，这是大多数大小写规范化的工作方式。

当然，我们知道有时候大写 *确实会让* 改变一个词或者词组的意思。我们可以看到，《猫》是一种动物，《猫》是一部音乐剧。不过，在大多数情况下，不规范 case 带来的精度提高会被召回率降低太多所抵消。这两者之间的区别也很容易通过上下文来辨别，我们将能够通过自然语言理解来利用这一点。

虽然在英语中不太常见，但处理音调符号也是字母规范化的一种形式。变音符号是附加在字母上的标记或“字形”，如á、或。单词在其他方面可以拼写相同，但添加的音调符号可以改变意思。在法语中，“élève”的意思是“学生”，而“élevé”的意思是“提升的”。尽管如此，许多人在搜索时不会包括音调符号，因此另一种形式的规范化是去掉所有音调符号，留下简单的(现在是模糊的)“eleve”

#### 标记化

下一个标准化挑战是如何分解搜索者在搜索栏中输入的文本和文档中的文本。这一步是必要的，因为查询和文档文本之间的词序不需要完全相同，除非搜索者用引号将查询括起来。

将查询、短语和句子分解成单词似乎是一项简单的任务:只需在每个空格处分解文本。使用这种方法，问题很快就会出现。还是那句话，先从英语说起。单独用空格分隔意味着短语“让我们把这个短语分开！”让我们 *让我们**破**起**本* ，还有 *短语！* 作词。

对于搜索，我们几乎肯定不希望在单词“短语”的末尾出现惊叹号我们是否要保持“让我们”这个缩写词在一起，就不那么清楚了。 [有些软件](https://text-processing.com/demo/tokenize/) 会把单词分解得更细(“let”和“‘s”)而有些不会。有的不会把“让”分解，而把“不要”分解成两块。

这个过程被称为“标记化”我们称之为 *记号化* ，原因现在应该很清楚了:我们最终得到的不是单词，而是离散的字符组。对于英语以外的语言来说更是如此。

以德语为例，说德语的人可以将单词(更准确地说是“ [语素](https://simple.wikipedia.org/wiki/Morpheme) ，“但足够接近”)合并在一起，形成一个更大的单词。“狗屋”的德语单词是“Hundehü tte”，它包含了“狗”(“Hund”)和“房子”(“hütte”)两个单词。

几乎所有的搜索引擎都将文本标记化，但是引擎可以采取进一步的步骤来规范化标记。两种相关的方法是词干化和词汇化。

#### 词干化和词汇化

词干化和词汇化采用不同形式的记号，并对它们进行分解，以便进行比较。例如，以“计算器”和“计算”或“减速”和“缓慢”为例。我们可以看到有一些明显的相似之处。

词干分析将一个单词分解成它的“词干”，或者这个单词的其他变体。词干提取相当简单；你可以自己做。“词干”是什么词干？你大概能猜到是“stem”词干通常意味着去掉前缀或后缀，就像在这种情况下。

有多种词干提取算法，最流行的是波特词干提取算法，它从 20 世纪 80 年代就已经出现了。它是将一个 [系列步骤](https://iq.opengenus.org/porter-stemmer/) 应用到一个令牌上得到的词干。

词干有时会导致你意想不到的结果。看看单词“carry”和“carries”，你可能会认为它们的词干都是“carry”至少根据波特词干算法，实际的词干是“carri”这是因为词干分析试图能够比较相关的单词，并将单词分解为尽可能小的部分，即使该部分不是单词本身。

另一方面，如果您想要一个始终是可识别单词的输出，那么您需要词汇化。还是那句话，有不同的 lemmatizers，比如 [NLTK 使用 Wordnet](https://www.nltk.org/_modules/nltk/stem/wordnet.html) 。

词汇化将一个记号分解成它的“词汇”，或者被认为是其派生词的基础的单词。Wordnet 中关于“进位”和“进位”的引理就是我们之前所期望的:“进位”。

词汇化一般不会像词干化那样分解单词，也不会像词干化那样在操作后认为许多不同的单词形式是相同的。“说”、“说”和“说”的词干都是“说”，而 Wordnet 的词条是“说”、“说”和“说”。为了得到这些词条，词条分类器通常是基于语料库的。

如果你想要尽可能广泛的回忆，你会想要使用词干。如果你想要最好的精度，既不使用词干也不使用词汇化。您最终选择哪一个取决于您的目标，但是大多数搜索通常可以很好地执行，既没有词干化也没有词条化，检索到正确的结果，并且不会引入噪声。

#### 复数

如果你决定不在你的搜索引擎中包含词汇化或词干化，还有一种标准化技术你应该考虑。这是复数对其单数形式的规范化。

一般来说，忽略复数是通过使用字典来完成的。即使“去多元化”看起来像去掉一个“-s”一样简单，但情况并不总是如此。第一个问题是不规则复数，如“鹿”、“牛”和“老鼠”。第二个问题是带有“-es”后缀的复数形式，比如“potato”最后，还有一些以“s”结尾但不是复数的单词，比如“always”基于字典的方法将确保你引入回忆，但不是错误的。

就像词汇化和词干化一样，你是否规范化复数取决于你的目标。通过规范化复数来撒一张更宽的网，通过避免规范化来撒一张更精确的网。通常，规范化复数是正确的选择，当您发现它们会导致问题时，可以从您的字典中删除规范化对。

然而，在处理错别字的时候，你几乎总是会想要增加召回率。

### [](#typo-tolerance-and-spell-check)错别字公差和拼写检查

我们都在搜索中遇到过错别字容忍和拼写检查，但思考一下为什么它会出现是很有用的。有时候，会因为手指打滑打错键而出现错别字。其他时候，搜索者认为一个单词的拼写与实际不同。越来越多的“错别字”也可能是语音到文本理解不良的结果。最后，单词可能看起来有错别字，但实际上没有，例如在比较“尖叫”和“奶油”时。

处理这些错别字、拼写错误和变体的最简单的方法就是根本不去纠正它们。有算法可以比较不同的令牌。其中之一就是[Damerau-Levenshtein 距离算法](https://www.lemoda.net/text-fuzzy/damerau-levenshtein/) 。

这一衡量标准着眼于从一个令牌到另一个令牌需要多少编辑。然后，您可以过滤掉距离过大的所有标记。(2 通常是一个很好的阈值，但是您可能希望根据令牌的长度来调整这个阈值。)过滤后，您可以使用距离对结果进行排序，或者将其输入到排名算法中。

很多时候，在确定一个单词是否拼写错误时，上下文是很重要的。“尖叫”这个词在“我”后面可能是正确的，但在“冰”后面就不是了。通过将 [上下文带入这个 NLP 任务](https://spacy.io/universe/project/contextualSpellCheck) ，机器学习可以是对此的解决方案。这个拼写检查软件可以使用单词周围的上下文来识别它是否有可能被拼错，以及它最有可能的更正是什么。

我们之前忽略的一件重要的事情是，当用户在搜索栏中输入单词时，单词不仅可能被拼错。文档中的单词也可能拼写错误。当文档由用户生成的内容组成时尤其如此。

这个细节是相关的，因为它意味着如果搜索引擎只查看查询中的错别字，它就会丢失一半的信息。最好的打字错误容忍度应该适用于查询和文档，这就是为什么编辑距离通常最适合检索和排列结果。拼写检查可以用来设计一个更好的查询或者向搜索者提供反馈，但是它通常是不必要的，不应该单独使用。

## [](#natural-language-understanding)自然语言理解

自然语言处理是处理文本和自然语言，而 NLU 是理解文本。

### [](#named-entity-recognition)命名实体识别

有助于搜索的任务是命名实体识别，或 NER。NER 识别文本中的关键项目或“实体”。虽然有些人会把 NER 称为自然语言处理，而其他人会把它称为自然语言理解，但很清楚的是，它可以在文本中找到重要的东西。

对于查询“NYE 派对服装”，你可能会得到一个映射到“类别”的“服装”实体 NER 总是将一个实体映射到一个类型，从通用的“地点”或“人”，到具体的你自己的方面。

NER 也可以使用上下文来识别实体。“白宫”的查询可以指一个地方，而“白宫涂料”可以指“白色”的颜色和“涂料”的产品类别

#### 查询分类

命名实体识别在搜索中很有价值，因为它可以与方面值结合使用，以提供更好的搜索结果。

回想一下“白宫油漆”的例子，您可以使用“白色”和“油漆”产品类别来过滤结果，只显示与这两个值相匹配的结果。这会给你很高的精度。如果您不想走那么远，您可以简单地提升所有符合这两个值之一的产品。

查询分类也有助于回忆。对于结果数量较少的搜索，您可以使用实体来包含相关产品。想象一下，没有与关键词“白宫涂料”相匹配的产品。在这种情况下，利用产品类别“paint”可以返回其他可能是不错的选择的油漆，比如漂亮的蛋壳色。

#### 文档标记

命名实体识别有助于提高搜索质量的另一种方式是将任务从查询时间移到摄取时间(当文档被添加到搜索索引时)。摄取文档时，NER 可以使用文本自动标记这些文档。

查询者将更容易找到这些文件。要么搜索者使用显式过滤，要么搜索引擎应用自动查询分类过滤，以使搜索者能够使用方面值直接找到正确的产品。

### [](#intent-detection)意图探测

与实体识别相关的是意图检测，或者确定用户想要采取的动作。

这与我们所说的识别搜索者意图并不相同。识别搜索者的意图就是让人们在正确的时间找到他们想要的正确内容。

意图检测将请求映射到特定的预定义意图，然后根据该意图采取行动。用户搜索“如何退货”可能触发“帮助”意图，而“红鞋子”可能触发“产品”意图。在第一种情况下，您可以将搜索路由到您的帮助台搜索，在第二种情况下，路由到产品搜索。这与你在谷歌上搜索天气时看到的没有太大区别，你会在页面的最上方看到一个天气预报框。(新推出的 [网络搜索引擎 Andi](https://andisearch.com/) 将这一概念发挥到极致，在聊天机器人中捆绑搜索。)

对于大多数搜索引擎来说，这里概述的意图检测是不必要的。大多数搜索引擎一次只能搜索一种内容类型。当有多种内容类型时，通过在单个 UI 中同时显示多个搜索结果，联邦搜索可以执行得非常好。

### [](#other-nlp-and-nlu-tasks)其他 NLP 和 NLU 任务

还有很多其他的自然语言处理和 NLU 任务，但是这些通常与搜索不太相关。像情感分析这样的任务在某些情况下可能是有用的，但搜索不是其中之一。您可以想象使用翻译来搜索多语言语料库，但这在实践中很少发生，也很少需要。

问答是一项 NLU 任务，越来越多地被应用到搜索中，尤其是期望自然语言搜索的搜索引擎。再一次，你可以在主要的网络搜索引擎上看到这一点。Google、Bing 和 Kagi 都会立即回答“英国女王多大了？”而不需要点击任何结果。

一些搜索引擎技术已经探索了为更有限的搜索索引实现问题回答，但是在帮助台或长的、面向行动的内容之外，使用是有限的。很少有搜索者会去网上服装店并向搜索栏提问。

摘要是一项 NLU 任务，对搜索更有用。就像使用 NER 进行文档标记一样，自动摘要可以丰富文档。摘要可用于将文档与查询相匹配，或者更好地显示搜索结果。这种更好的显示可以帮助搜索者确信他们已经得到了好的结果，并让他们更快地找到正确的答案。

即使包括使用图像和音频的新搜索技术，绝大多数的搜索都是文本搜索。为了获得正确的结果，确保搜索处理并理解查询和文档是很重要的。NLP 和 NLU 任务，如标记化、规范化、标记、错别字容忍等，可以帮助确保搜索者不需要成为搜索专家，而是可以“自然地”快速地从需求到解决方案。