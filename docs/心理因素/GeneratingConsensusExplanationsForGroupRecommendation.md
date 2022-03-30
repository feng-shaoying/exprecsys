# Najafian and Tintarev - 2018 - Generating Consensus Explanations for Group  Recommendations

## 1、研究介绍

在某些场景中，比如音乐，人们经常集体消费物品。然而，达成一致意见是困难的，而且往往需要作出妥协。这样的妥协可能会帮助用户扩大他们的品味。同时它们还可能导致完全拒绝接受推荐的项目。避免这种情况的一种方法是给出让个别用户令人惊讶的解释，甚至是不喜欢的建议。本文提出了一种组解释的方法。提出了选择一组歌曲序列的算法。这些算法考虑共识，但有不同的权衡。接下来，使用这些算法，我们使用合成数据进行分层评估生成解释。在对用户的结构化访谈(n=16)中研究了这些解释对用户满意度的影响。

**本文最大的创新点：基于Masthoff之前的工作,融合之前的*Least Misery Strategy*、*Most Pleasure Strategy*、*Average Without Misery Strategy*、*Fairness Strategy*等不同的算法产生推荐序列,然后通过结构化面谈,来了解用户的满意度。**

## 2、研究贡献

我们建议开发在一个组中聚合用户偏好的算法可以帮助提高用户满意度。然而，要想有效地做到这一点，这可能需要使用经过验证的解释。为了解决这些问题，本文做出了以下贡献：

* Two *improved algorithms* for constructing sequences of recommendations to groups. These strategies build on existing work on generating sequences, and address scenarios where users have different preferences from each other.
* *Evaluating* the *satisfaction* of users receiving explanations resulting from two different algorithms. In structured interviews we evaluated how four (4) different explanations influenced user satisfaction for five (5) different scenarios..

## 3、相关工作

Masthoff等人提出了几种生成推荐序列的算法。以下是一些可能会影响masthoff工作中提出的基于权衡的场景的算法：

* *Least Misery Strategy*
* *Most Pleasure Strategy*
* *Average Without Misery Strategy*
* *Fairness Strategy*

我们可以观察到，这些算法代表了不同的策略。.例如，Average Without Misery会确保没有人不开心，但它可能会错过（或排名非常低的排名）只有一些用户喜欢的东西。另一方面，公平可以确保每个人都能得到他们喜欢的东西，但只有在轮到他们的时候。**在Masthoff的工作中,从不同的角度考量设计推荐算法产生推荐序列。本文基于Masthoff的工作,融合不同的算法产生推荐序列,通过结构化面谈,了解用户的满意度。**

Nguyen和Ricci通过组成员的交互和用户长期偏好融合了生成最佳推荐，虽然他们研究了组决策和共识达成，但没有研究解释。基于融合的策略构建推荐序列并设计组解释，这种新颖的策略和解释适应用户不同的偏好并达到一个可接受的共识。

## 4、研究方法(提出的算法)

在这里，我们定义了新的序列构造算法，并解释了它们的动机。实例说明了由所提算法所产生的序列的有序组列表。这两种算法代表了两种在偏好不一致时解决共识的方法，这可能会影响用户的满意度，例如，避免痛苦，最大化快乐，公平性；以及系统性能，如完整性，清晰的排序。

*  *Algorithm 1: Least Misery + Most Pleasure + Without Misery.* The strategy of this algorithm is to mitigate the original strategies’ disadvantages as much as possible. When using original Least Misery and Without Misery strategies on their own, items may be selected that nobody hates but also nobody really likes.

* *Algorithm 2: Fairness -> Average.* We apply the base strategy Fairness, and for tie-resolving use the Average rating across all users in the group. By tie-resolving we mean that when the rating is the same for multiple items the one with higher average rating will be selected. 

  **STRUCTURED INTERVIEWS**

  Four types of explanations:

  1. Repair-related explanation with vital information
  2. Repair-related explanation with complete information
  3.  Reassuring explanation with vital information
  4. Reassuring explanation with complete information

## 5、研究结论

设计出提高用户满意度的解释是本研究的目标。我们基于不同的序列构建算法提出了不同类型的解释，并调查了不同场景下用户对这些解释的印象。我们基于不同的序列构建算法提出了不同类型的解释，并调查了不同场景下用户对这些解释的印象。图1通过解释和场景总结了结果。纵轴表示每个场景对每种解释的平均满意度。此外，误差条表示了这些结果的标准偏差(SD)。由于样本量小，且本研究为探索性研究，我们没有进行统计学分析。
![](https://fengshaoying.oss-cn-shanghai.aliyuncs.com/images/20220313205427.png)

比较上述四种解释类型的类型，解释3（reassuring with vital information）在满意度方面表现更好，无论它在哪个场景。情景1、2、3、4、5中的(m=3.4、SD=1.15)、m=1.06)、SD=3.9，SD=1.06)、(m=4.6、SD=0.51)、(m=3.8、SD=1.2)。特别是，场景4中的解释3的平均满意度最高(m=4.6，SD=0.51)。除了对解释进行评分外，我们还问参与者他们为什么他们喜欢这个特定的解释，为什么不喜欢。他们喜欢解释3的一些原因如下： "*The explanation is easy to understand*", "*The encouraging tone.*", "*Nice, friendly,*clear and short*", "*The explanation is short and concise".参与者提到的特点包括简洁、简单、友好，以及清晰易懂的内容。

## 6、不足与展望

在本文中，我们提出了两种改进的构造推荐序列的算法。然后，我们提出了不同的解释方式，可以让人reassuring or repairing。参与者更喜欢简短、简单、非正式、友好和鼓励的解释，而不是长时间、复杂和消极的解释。然而，当预期到最大的痛苦（根本没有得到他们喜欢的东西）时，一个更复杂的解释是可以接受的。虽然直观，但我们的结果为序列的要求提供了实证基础。
我们的下一步将是研究小组在一个联合环境下的行为，所有小组成员都在场。我们将评估更简单的解释是否只对“active user”有效，以及这对他们的组成员有什么影响。我们也在努力从评级中自动生成这些解释，这样我们就可以以更系统的方式来评估它们的效果。