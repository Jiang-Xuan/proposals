在 insight 的前端开发工作中总是需要和设计, 交互, 产品进行密切的配合, 想要成立设计规范和组件库, 痛点在于各方合作的流程, 因为 设计/交互/产品 不甚了解前端技术, 前端在没有实际的开发的时候有可能会忽视设计稿中的难点. 想要解决掉这些痛点, 就需要有一个来流程

hello, 大家好, 在座的各位应该都是非常熟悉的, 不过今天有新来的交互美女和帅哥, 在上周的 table 组件的规范中匆匆见了一面, 有可能没有记住我的名字, 所以我两句话介绍一下 **下一张 PPT**

我叫蒋璇, 现全职负责 Insight 前端部分的开发工作 **下一张 PPT**

先说一下前端角度的代码迭代历史, 其实 Insight 已经迭代很多很多年了, 从最初的大量的覆盖 antd 组件库的样式,之后的几年就一直在魔改 antd. 到 2018 年想要在 antd 的基础之上成立自己的一套规范, 由于设计师离职, 导致还没有推动就已经搁浅了.所以现在的 设计师, 前端开发都有自己的痛点, 比如:

* 设计师方面, 没有通用组件可以复用, 即便设计师复用了组件, 前端也不是复用组件, 其实这不是复用组件, 从现在的 insight 的网站就可以看出来, 大量的可复用组件几乎都是重新写, 交互和样式都不尽一致, 所以其实每一次的设计都是从头开始的.
  
  > 我感觉我和设计师说的最多的就是: 和现在的其他页面保持一致吧, 改动不好改动, 有可能会影响其他的页面, 这其实是前端开发和设计师共同的问题, 我们不知道其他地方的代码到底是怎么运作的

* 前端开发工程师方面, 无法构建组件库, 因为和设计师沟通不足, 抽出来的组件并没有被设计师在设计稿中使用, 无法复用组件, 其实每一次的设计稿都是在做重复的工作, 重复的和设计师确认.

* 产品方面, 整站样式混乱, 交互混乱

* 全员痛点: 没有文档, 没有 demo, antd 升级困难, 全靠口口相传😅, 后续的接手人会很难受

想要解决以上问题, 就需要成立一套设计规范和组件库, 但是需要解决以下问题**下一张 PPT**:

* 我们如何推动一条样式或者是组件进入组件库
* 如何开发以及文档如何维护
* 如何保证设计师, 前端开发工程师, 产品经理知道某一 组件/样式, 并对其的理解一致
* 如何让某一个人的想法能够让各方充分的理解并决定是否实施

**下一张 PPT**

我用一个拟物化的流程来暴露这些问题, 设想我们有一个盒子, 这个盒子有一个特点是一件东西被放进去之后, 它可以被无限的取出, 也就是如果里面有一个苹果, 你取出来一个苹果, 里面的这个苹果还是存在的. **下一张 PPT**

大多时候一个样式规范或者是一个组件都是由 设计师/前端开发工程师 提出的, 这里就以设计师为列, 就好像这个苹果, 设计师说我想要在很多地方都用到这个苹果, 我在 设计稿中将其抽成了一个组件, 其他地方和这个是一样的.由于职业不同, 设计师并不知道这个苹果是不是真的在前端可以实现, 如果没有充分的沟通实际上在前端的实现有可能是千差万别的, 所以设计师即便在设计稿中将其抽成一个组件也无用.  所以这就暴露除了第一个问题, 我们如何推动一条样式或者是组件进入组件库? **下一张 PPT**

> 其实前端方面也是一样的问题, 我们抽成的一个组件有时候设计师也不知道.

假设 设计师 和各个利益方都已经沟通了这个苹果, 大家都很满意, 都同意这个是可以进入这个盒子的, 那么接下来就需要进一步的沟通, 沟通这个苹果的细节, 这个苹果的叶子是什么颜色的, 这个苹果是不是允许带上一些装饰品,以及交给 谁来开发/谁来设计, 文档谁来书写, 谁来维护? 这就暴露出来了第二个问题, 我们如何开发以及文档如何维护? **下一张 PPT**

这个苹果完成了之后我们还需要让产品在原型稿阶段就可以使用, 让设计师在设计阶段可以使用, 让前端开发工程师在开发阶段可以使用😃 这就暴露出来了第三个问题, 如何保证设计师, 前端开发工程师, 产品经理知道某一 组件/样式, 并对其的理解一致?**下一张 PPT**

每一个人在自己的工作领域都会遇到自己的痛点, 有时候就想用规范来简化自己的工作, 所以每一个人都有可能有把东西放到这个盒子里面的需求, 这就暴露出来第四个问题, 如何让某一个人的想法能够让各方充分的理解并决定是否实施.

> 1. 我在 11.0 改动了 tree 组件的间距和一些样式, 把前端覆盖 antd 的样式去掉了, 我以为产品可以接受, 所以我就偷偷的改掉了. 结果产品还是发现了, 让我把样式还原😅.
> 
> 2. 在做全球新药详情页面的时候和设计讨论了把一个东西抽成组件, 结果我并没有做, 设计也不知道, 我们也没有文档, 而且林潇也不知道我们决定抽出来这个组件. 所以目前也还是没有实现这个组件😅.

OK, 问题我们暴露完毕, 这些问题的相关利益方有, 设计师, 交互师, 前端开发工程师, 产品经理, 所以需要我们一起才能解决这些问题, 我们要实现的东西有**下一张 PPT**

样式 -> 字号和其行高, 字体的粗细, 颜色, 间距 ...

组件 -> Modal, Table, Button, Grid, ... 不过注意, 将会采用 antd 组件库, 进行一部分的样式覆盖, 目前 antd 的版本被锁定在 3.5.4 版本, 所以会和现在的 antd 官网的表现不一致.

就上诉的所有问题, 我提出以下的流程来解决这些问题:

第一

第二

第三

第四

第五
