# 白皮书

## 作者注
## Author's note

在2017-2018区块链发生了非常引人注目的投机活动把我们的注意集中到了加密通证上。当我们买卖它们时，我们甚至忘记了它们真正的用途; 这类似于房地产泡沫，人们忘记了房屋不仅仅是投机资产，而是居住的地方。
The remarkable blockchain speculations that took place in 2017 - 2018 brought our attention to crypto tokens. As we bought and sold them, we forgot their intended purpose was to be used; this is analogous to the housing bubble in which people forgot that houses were not merely speculative assets but rather a place to live.

为了给区块链提供实际的用途，我们必须了解他对世界经济和互联网的作用。这篇文章的作者是对金融机构和初创公司进行了长期的学习和探索的技术专家。凭借这些经验，我们逐步意识到区块链有两个主要的功能，我们将在本文中进一步阐述。
To provide a practical use of the blockchain, we must understand its utility to the world economy and the internet. The authors of this paper are technical experts who went through years of study and exploration into its applications both via financial institutions and startups. With this experience, we came to realise that the blockchain has **two primary functions** which we will elaborate further in this paper.

尽管过去的2017-2018年非常愚蠢，但是开始对于通证的关注并不是坏事。通证，作者即将详细阐述的，将是两个主要功能的推动者。我们将定义实现“通证化”的技术。
Despite the great folly in 2017-2018, it is not a bad thing to initially focus on tokens. Tokens, as the authors will elaborate, are the enabler of the two primary functions. We define the technique to make it happen in "Tokenisation".

区块链行业一起的努力主要集中在丰富技术能力上。这篇文章将集中在通证化，并且介绍一个称作TBML的标准化工作（通证行为标记语言，它将使区块链技术具备完整的技术堆栈，为经济和互联网提供实用性。
Previous efforts in this industry primarily focused on enriching the capacity of the technology. This paper will focus on tokenisation and introduce a standardisation effort known as TBML (Token Behaviour Markup Language) which will make the blockchain technical stack complete, providing utility for the economy and the internet.

就像房子是用来住的一样。
Just like a house providing a place to live.

## Advertisement

 Please join our work at xxx. A yellow paper will be produced to guide implementors to use TBML for their tokens and dapps, but a work in progress is always available online.


 \pagebreak


# Introduction: What does blockchain *do*?
\pagebreak


区块链主要有两种功能，这两个功能能够改变人与人之间的交互和商业行为.很不幸的是这两个功能都在早期的投机游戏中被忽视了。
There are two primary functions of blockchains that can change the way human interacts and business conducts. Both were neglected amidst the unfortunate speculative games in the early days of Blockchain.

正如我们即将阐述的，第一个是创造完全市场(译者注:”完全资本市场又称无摩擦资本市场(Frictionless Capital Markets)是金融经济学家所假想出来的一种资本市场环境，旨在简化或深化理论分析，促进理论的发展。完全资本市场，是指在这个资本市场中，任何投资人都无法拥有通过自身交易行为而影响或操纵市场上的证券价格的力量；投资者可以平等地免费获得影响股票价格的全部信息；证券发行不存在发行成本、交易费用等)的能力。第二个是集成网络的能力。
As we will soon elaborate, the first is the capacity to create frictionless markets. The second is the capacity to integrate the web.

本文将从愿景开始，然后解释架构师需要在区块链上架构的原因,接下来关注一个使这个架构成为可能的关键技术，我们把它叫做TBML。
This paper is going to start with the vision, then, reason the architect needed on top of blockchains, then focus on a critical layer of technology that enables this architect to be possible, which we name TBML.

在2017-2018区块链发生了非常引人注目的投机活动把我们的注意集中到了通证上。当我们买卖通证的时候，我们忘记了它的用途。就好像罐头沙丁鱼变成了一种投机资产，人们对罐头沙丁鱼是用来吃的想法不屑一顾。
The remarkable blockchain speculations took place in 2017 - 2018 brought our attention to tokens. As we buy and sell tokens, we forgot that it was intended to be used. It was like when canned sardines became a speculative asset, people brush off the idea that it was made to eat.

尽管存在令人遗憾的投机泡沫，但专注于通证并不是错误的，因为它是我们将阐述的两个主要功能的推动者：
Despite the unfortunate speculative bubble, it's not wrong to focus on tokens, as it is the enabler of the two primary functions we will elaborate:

介绍
## Introduction

区块链技术提供 **两种主要功能** 为未来经济和未来互联网提供基本用途：
Blockchain technology has **two primary functions** that serve essential purposes for the future economy and the future Internet:

 - 提供完全市场; 
 - 集成网络。
- providing a frictionless market; and
- integrating the web.

本文将阐述我们的目标，并且了解区块链顶层架构背后的设计和推理。 然后，我们将解释TBML，这是一个关键的缺失层，接下来回顾其设计原则和了解我们将如何构建它。
This paper will address the vision of where we can be and follow up with the design and reasoning behind the architecture needed on top of the blockchain. We will then explain TBML which is a critical missing layer and go over its design principles and how we are building it.

## 区块链提供了一个完全市场
## Blockchain provides a frictionless market

上个世纪80年代的“回到未来”描绘了一个强大的机械世界，悬浮滑板，飞行汽车。但是他们并没发生。正如彼得·泰尔曾经注明的哀叹，“我们曾经承诺能飞的汽车，结果只得到140字符。但是我们时代的技术进步依旧超出了80年代科幻电影的想象，尽管不是通过更强大的机器，而是有效利用互联网。
The 80s' "Back to the Future" featured a world of powerful machines filled with hovering boards and flying cars. It didn't happen. As Peter Thiel once famously lamented, "we were promised flying cars; instead, we got 140 characters". The technological advancement of our time is beyond the imagination of the 80s science fiction movies, albeit not through more powerful machinery, but efficient use of  the  Internet.

共享行程彻底改变了我们的日常生活，airbnb改变了我们旅行的方式。这个是一个全新的，摩擦更小的市场市场，它们的运营成本更低，更易于使用，并且拥有更精细的运行单位。
Ride-sharing revolutionised the way we organise our daily lives, and AirBNB changed the way we travel. These are the new, less frictional markets. They incur less cost to operate, are more accessible and have finer operational units.

然而，尽管进行了Web 2.0革命，大多数市场仍然以高成本运营。例如，股票市场由于依靠对于规章制度的信任来运作，开销非常大，它只适合价值数百万美元的商业。
However despite this web 2.0 revolution, the majority of markets still operate with high costs. The stock market, for example, has so much overhead that it is only justifiable for multi-million dollar businesses which rely on the trust of rules and regulations to operate.

使用区块链，任何通证化的资产都可以随时进行交易，只要遵循规则，没有中间商或中间人，给我们提供最大的市场效率-一个完全市场。除了不依赖中间商之外，在通证化的市场模型中，买方和卖方不在需要”进入“市场。相反，通证总是在市场上【*市场模型】，这样的模型当然比中间商更好
With blockchain, any tokenised asset can be transacted any time, as long as it follows the rules, without middlemen or intermediary, gives us maximum market efficiency - the frictionless market. On top of the benifits of not relying on an intermediary, in a tokenised market model, the buyers and sellers do not need to "enter" the market; instead, tokens are *always on the market*[^market-model], making such a model better than intermediaries.

【*市场模型】: 传统的中介操作市场模式，交易分为两个阶段：进入市场，达成交易。 区块链可以将其简化为协议; 因此，区块链通证资产可以被视为始终在市场上。

我们能够通过通证化创造完全市场吗？
### Can we create a frictionless market through tokenisation?

我们是否可以通证化，举个例子，1%的资产，这样的房地产市场是否可以比长达一个月的房地产购买-销售周期更快？ 
Can we tokenise, for example, 1% of a property, so that the property market can react faster than the typical month-long property purchase-sales cycle?

我们是否可以通证化电力，让电力用户能够从更精细的安排中受益，家庭能够从更多的太阳能收集受益。
Can we tokenise electricity, allowing power users to benefit from finer scheduling of the use of resources, and households to benefit from collecting surplus sun energy?

我们是否可以通证化Airbnb的预订，以便房屋主人可以从市场上获得有保证的现金流，而投机者可以通过预测旅行需求获利
Can we tokenise AirBNB bookings, so that hosts can purchase a guaranteed cash flow from the market, while speculators profit from predicting the travel needs?

我们是否能够通证化国际贸易的风险和回报，让没有足够信用的，小型进口商和出口商，能够在国际市场上参与竞争，也许能够超过像Airbnb这样的传统供应商。
Can we tokenise the risk and reward of international trades, so that small importers and exports, not significant enough to obtain letters of credit, can compete in global markets and perhaps eventually outcompete the traditional model like AirBNB outcompetes hotels?

我们是否能够通证化依赖于加密证明的保单，以便保险公司减少处理欺诈性文件的成本，我们可以完全去中心化保险公司吗？
Can we create an insurance token that depends on cryptographic proofs, so that the insurer can remove from their pricing, the costs incurred by fraudulent documents? Can we decentralise the insurers altogether?

区块链可以提供基础层来实现这些。为了定义通证应该如何被使用和交易，仍然在可扩展性，隐私方面仍需要完成很多工作。但是我们认为最大的挑战在于通证化。
Blockchain can provide the foundational layer to achieve these. A lot of work needs to be done to ensure scalability, privacy and quality methods to define how tokens should be used and traded, but we see the biggest hurdle lies in tokenisation.

通证具有不同的属性。通证是否会过期？ AirBNB预订通证当然会，但1％的房产通证可能不会。通证所有者是否应收到有关特定事件的通知，电力通证肯定需要，因为电力是不断变化的。通证是否流通？
Tokens have different properties. Do tokens expire? AirBNB booking tokens certainly do, but 1% ownership of property tokens probably don't. Should the token owner receive a notification on a specific event? Power tokens certainly need that, for the change in the power supply is dynamic. Is a token stream-able?

它如何在用户的手机上显示，用户如何使用。
How does it look on the user's mobile, and how is it called in a users language?

如果买家需要从卖家沟通通证化的乡村庄园，他们如何进行有效的沟通。
If a buyer wants to purchase a tokenised country estate from a seller, how do they establish a trusted method of communication?

如果通证允许用户在线执行特定操作，用户如何使用通证登录特定web服务。
If a token entitles the user to do specific actions online, how can the user login to the web services with that token?

很容易看出需要一个定义通证的框架，让他们适应不同的交易，上市以及评级。我们确实在我们确实在2017-2018期间拥有数百种通证，但是他们在同一支付方面-类似货币，ERC20 通证。 几乎没有让通证在代表 *商品和服务*上做任何努力，这个是一个有效市场的基本需求。
It's easy to see the need for a framework defining tokens and making them interoperable with different methods of trading, listing and rating. We did end up having hundreds of tokens in 2017-2018, but they are uniformly on the payment side - currency-like, ERC20 tokens. There is nearly zero effort devoted to making tokens represent *goods and services* - a basic need for an efficient market.

举个例子，在2017年的投机泡沫期间，电力通证的ICO不需要提供关于如何使用通证的任何解释。 所有投机需要知道的是，它们代表了“未来的电力通证”。 只要通证可以满足投资者的想象力，这对ICO来说就足够了。 因此，除了ERC20接口之外，他们没有任何其他功能。 对于这样的投机电力通证来说，它不依赖任何证据，如实际发电量的证明，没有在哪儿提供电力的属性，以及可用的时间长短。
During the speculative bubble of 2017, a power token ICO does not need to provide any explanation of how the tokens can be used. All speculators need to know is that they represent a "stake in the future world of tokenised electricity". As long as the token can inspire investors with imagination, it's good enough for an ICO. There is, no more functionality needed other than an ERC20 interface. Such a speculative token doesn't depend on attestations - the proof of actual power production - nor does it need properties like where the energy is provided or for how long it is available.

现在疯狂已经结束，现在是时候提出技术框架来使市场发挥作用。
Now that the madness is over, it's time to present the technical framework to make the market work.

区块链集成网络
## Blockchain integrates the web

蒂姆·伯纳斯·李 和 万维网的创造者主要公共图书馆的模型和人机交互模型为模型来构筑互联网。
Tim Berners-Lee and the innovators of the world wide web modelled the web primarily on a public library model and computer-human interaction model.

在图书馆模型中，信息可以免费获得，并通过URI进行索引和交叉引用。 它的化身，URL就是数据所在的位置，它对你能够访问的地方没有限制。
In the library model, information is freely available, indexed and cross-referenced by a URI. Its incarnation, the URL, is where the data is, and there is no restriction on where you can go.

在人机交互模型中，两个玩家进行对话，人问，机器回答，机器拥有优先的知识，但是这个能够帮助用户正确的访问计算机。
In the computer-human interaction model, two players are having a conversation - the human asks and the machine answers. A computer has limited knowledge, but it can help the user to reach the right computer.

因此，网络被构建为一个巨大的图书馆，每本书都是一台可以与之交谈的计算机。 这可能是Facebook获得同名灵感的地方 - 网站就是一本书。
Therefore the web was built as a giant library where each book is a computer with whom one can have a conversation. The analogy probably is where Facebook got its namesake inspiration - a website is a book after all.

正是这种设计造成了许多现代的不便。用户有一天会在她的月结单上收到一封电子邮件，但她无法识别出一些条目，它问:"亚马逊"，这个是一个鞋子的订单吗？她必须复制订单号并在亚马逊中查找。在另一种情况下，同一个用户可能会在预订两张歌剧门票时暂停，切换到她的常旅客应用程序，复制该号码并将其粘贴到订单中以收集积分。 她需要会在一开始就安装那个常旅客应用程序。
This design has caused a lot of modern inconveniences. A user would one day receive an email on her monthly statement, yet she couldn't recognise a few entries on them. It says "Amazon". Was it about ordering a pair of shoes? She has to copy the order number and look it up in Amazon. In another occasion, the same user might pause as she books two tickets for an opera, switch to her frequent flyer app, copy that number over and paste it into the order to collect the points. She might struggle a bit installing that frequent flyer app at the outset.

我们为什么要做这么多的复制和粘贴，这些机器特别擅长的动作。因为网络就像一个图书馆设计，我们就像读者一样在袖子上面记录索引号。他们并不像个人助理一样设计。
Why are we doing so much copy and pasting when machines are exceptionally good at doing this? It's because the web is like a giant library by design, and we are like readers keeping notes of the index numbers under our sleeves. It's not, as we would hope to have, designed like a personal assistant.[^smart-phone]

[^智能手机]：令人惊讶的是，即使是为了充当个人助理（智能手机）的角色而发明的技术仍然失败了，原因同样如此：单靠客户端的努力无法集成网络。必须在基础设施上支持集成， 智能手机的模型类似于拨号互联网连接，每个应用程序代表一个网站。 在进入对话之前，用户仍然需要找出要与之通话的计算机（app），并且在他交换应用程序时仍然可以复制信息。 例如，要求您的智能手机通过在线银行的app汇总你所有的资金是不可能的。
[^smart-phone]: Surprisingly, even the technology that was created to fill the role of a personal assistant, the Smart Phone, still failed, for the same reason: the efforts from client side alone can't integrate a Web that is not designed to integrate. The infrastructure has to support integration. A smartphone is modelled like a dial-up Internet connection, with each app representing a website. The users still need to figure out which computer (app) to talk to before entering the conversation, and still copies information around as he swaps apps around. It's not possible, for example, to ask your smartphone to sum up all the money one may access by his online banking apps.

很容易就能看出造成不便的原因：不同的网络之间没有更好的集成。继续举几个不好的例子；

It's easy to see the cause of the inconvenience; the web is poorly integrated. The bad examples go on and on:

- 当用户在网站上结账时，她不确定她的卡上是否有足够的余额，因为银行未与购物系统集成。
- When a user checks out on the web, she isn't sure if she has enough balance on her card, since the bank is not integrated with the shopping system.
- 当患者订购服务时，在账单结算之前，她无法看到保险可以支付多少费用，也不知道她是否达到年度上限，因为诊所没有与保险公司集成。
- When a patient orders a service, she can't see how much the insurance can cover until the bill settles, nor can she know whether she has reached the annual cap since the clinic is not integrated with the health insurance company.

集成网络的答案需要一些不在蓝图中的模块：身份验证，所有权，价值转移和交易。
The answer to integrating the web requires a few building blocks that weren't in the Web's blueprint: authentication, ownership, transfer of value and trading.

Web没有内置的身份验证机制。 像“使用Facebook登录”这样的附加组件仅仅试图通过受信任的第三方提供身份验证【^tls】，尽管存在隐私和可用性问题，但它仅适用于帐户身份验证，而不适用于业务逻辑。
The web doesn't have a built-in authentication mechanism[^tls]. The add-on "Sign in with Facebook" merely tried to provide authentication through a trusted 3rd party, which, despite privacy and availability concerns, is only good for account authentication and not for integration.

尽管在TLS中对客户端/服务器证书进行了很好的努力，但这些身份验证方法不适用于进程，仅适用于站点。这其实是一个委托模型。想象一下，买方不检查所有权契约是否真实，但只检查卖方的名称是否与契约上的名称相匹配。 这就是TLS中使用的委托模型。 事实上，TLS无法保证网站上的任何内容是真实的，只有网站是真实的.
Facebook使用TLS，但人们在其上放了很多假新闻。 毫无疑问，这里的信任单位不足以提供集成网络的体现。
[^tls]: Despite the excellent efforts on client/server certificates in TLS, these authentication methods are not for processes, but only for sites. It's a delegation model. Imagine a buyer not checking if a title deed is real, but only checks if the seller's name matches the one on the deed. That would be the delegation model used in TLS. In this model, TLS can't guarantee anything on the website is real; only that the website itself is. Facebook uses TLS, but people put much fake news on it. The unit of trust here is undoubtedly not granular enough for the web to deliver an integrated experience.

“帐户身份验证”不能取代Web集成
### "Account authentication" is not a substitute for web integration.

例如，简单的业务逻辑：“汽车的所有者可以检查其服务历史记录”，并不需要帐户。 如果您强行使用“帐户身份验证”模型，就会出现很糟糕的情况：
For example, the simple business logic: "the owner of a car can check its service history", doesn't require an account. If you force the "Account authentication" model, bad things happen:

 - 当汽车售出时，新车主现在需要在服务网站上创建一个新帐户，并且加密它，用来证明自己的所有权。 这是繁重且不可靠的。
- When the car is sold, the new car owner would now need to create a new account at the service website and secure it with the proof of ownership to the car. This is onerous and unreliable.

 - 当车辆改装车间或保险公司等第三方需要访问维修历史记录时，没有简单的方法可以在不泄露帐户的情况下对其进行授权。 这是不灵活的。
- When a 3rd party like a Vehicle Modification workshop or an insurer needs to access the repair history, there is no easy way to authorise them without giving away the account. This is inflexible.

更多此类示例很容易在医疗保健，零售和网络上的几乎所有业务中找到。 今天，我们不断添加越来越多的帐户来满足这种集成需求。这就像是你手里有一把锤子，看什么都是钉子。以下章节将演示通过通证集成而非帐户是一个可靠的解决方案。

Such integration needs, poorly addressed by adding accounts, are easily found in healthcare, retail and almost every web-based business. Today, we are still adding more and more accounts to address the growing integration needs. It's a case of hammering every problem down as if it is a nail. The following chapters will demonstrate that integration through token, not account, is the solution.

同样，网络没有内置的所有权，价值转移和交易机制。
Similarly, the web doesn't have a built-in mechanism for ownership, transfer of value and trading.

来看看汽车故事的未来发展，汽车销售商需要在网站上发布汽车信息，在过程中创建另一个帐户。 买方不能点击“购买”并一次性获得所有权证明，强制保险，未使用的服务配额等，并进行付款处理。 所有这些操作都必须使用易于篡改的纸张样张和表格单独完成。 该过程从Web开始，在其他的地结束。
Taking the car story further, a car seller would need to post the car information on a website, creating yet another account on the way. The buyer cannot click "buy" and acquire the ownership proof, compulsory insurance, unused service quota and so like in one go, and have payment processed. All these actions have to be done separately, using easily-tampered paper proofs and forms. The process starts at the web and ends somewhere else.
相反，同样的过程反正在区块链上是自动的，防伪的[^证明]和原子的。
In contrast, the same process on blockchain would be automatic, fraud-proof[^attestations] and atomic[^atomic].

[^证明]：提供加密签名的证明作为交易条件的方法将在后面的“证明”章节中讨论。
[^attestations]: the method to provide cryptographically signed attestations as a condition for a transaction is discussed later in the "Attestation" chapter.

[^ 原子性]：在区块链术语中，原子事务以为着都发生或者都不发生。 如果定义明确，买方不可能成功支付汽车而没有获得所有权令牌，或者只是转让了汽车的所有权而没有强制性保险。
[^atomic]: In blockchain terms, an atomic transaction either happens or not. If well defined, it's not impossible for a buyer to have successfully paid for a car yet not getting the ownership token, or only have transferred the car's ownership but not the compulsory insurance on it.

网络的这些缺失特征是区块链的众所周知的功能。 这对完美契合夫妇的虚拟婚礼需要虚拟交换通证，或者本文称之为“通证化”。
These missing features of the web are the well-known functions of the blockchain. The virtual wedding of this perfect fit couple requires a virtual exchange of tokens, or what this paper called "tokenisation".

通证无缝地跨越系统，承载其交易规则和用户界面以及业务环境。
Tokens seamlessly go across systems, carries their trading rules and user interfaces and business context.

## 例子：汽车所有权通知
## Example: Car Ownership Token

下面是一个例子：汽车所有权通知，已经成功通证化
The following example, a car ownership token, is a successfully tokenised .... [Edit: explain the elements]

    +----------------------------------------------------------+
    |                                                          |
    |          Holden Barina 2012 Ownership Token              |
    |                                                          |
    |          Make: Holden Year: 2013  Colour: Black          |
    |          VIN: KL3TA48E9EB541191                          |
    |                                                          |
    | +--------+  +--------------------+  +------------------+ |
    | | Open   |  | Authorise use      |  | List for sale    | |
    | +--------+  +--------------------+  +------------------+ |
    |                                                          |
    | +--------+  +--------------------+  +------------------+ |
    | | Start  |  | Lend               |  | Auction          | |
    | +--------+  +--------------------+  +------------------+ |
    |                                                          |
    | +--------+  +--------------------+  +------------------+ |
    | | Lock   |  | Transfer Ownership |  | Collateralise    | |
    | +--------+  +--------------------+  +------------------+ |
    |                                                          |
    | +--------+                          +------------------+ |
    | | Locate |                          | List for sharing | |
    | +--------+                          +------------------+ |
    |                                                          |
    |               Registration:                              |
    |                                                          |
    |               +------------------------------------+     |
    |               |                                    |     |      +-----------------------------+
    |               | Issuer: Roads & Maritime Services  |     |      |                             |
    |               | Rego: CJ41HL   Expiry: 2017+12+03  |     |  +-> | Access rego attestation     |
    |               |                                    |     |      |                             |
    |               +------------------------------------+     |      +-----------------------------+
    |                                                          |
    |               Holden Capped Service                      |
    |                                                          |
    |               +------------------------------------+     |
    |               |                                    |     |
    |               | Issuer: Holden Australia           |     |      +-----------------------------+
    |               | Expiry: 2020-12-09                 |     |      |                             |
    |               | Last served: 180 days ago          |     |  +-> | Access Invoice Token        |
    |               |             (due for a service)    |     |      |                             |
    |               |                                    |     |      +-----------------------------+
    |               +------------------------------------+     |
    |                                                          |
    |               Insurance                                  |      +------------------------------+
    |                                                          |      |                              |
    |               +------------------------------------+     |      | Access insurance token       |
    |               |                                    |     |      | functions:                   |
    |               | Issuer: Qantas Car Insurance       |     |  +-> |                              |
    |               | Start Date: 2017 12 30             |     |      | · Claim                      |
    |               |                                    |     |      | · Lump sum discount payment  |
    |               +------------------------------------+     |      | · Upgrade / downgrade        |
    |                                                          |      | · Suspend policy             |
    |               Purchase:                                  |      | · Access Roadside Assistance |
    |                                                          |      |                              |
    |               +------------------------------------+     |      +------------------------------+
    |               |                                    |     |
    |               | Issuer: Manheim Auctions           |     |
    |               | Date: 2015+12+09   Price: $4724.83 |     |
    |               |                                    |     |
    |               +------------------------------------+     |
    |                                                          |
    +----------------------------------------------------------+

咋一看，它只是一个便利的能够做关于汽车所有事情的门户网站，包括市场功能和实用程序。然而传统的网络模型是不可行的。
At first glance, it is just a handy portal to do everything about the car, including market functions and utility. However, it's not possible with the traditional web model.

在web2.0模型中，你只能自己处理每个元素。要注册汽车，有一个单独的过程，需要创建一个道路与海洋服务处的账户，并且在没有密码学的帮助下证明所有权。当您想为汽车提供保险时，您必须创建另一个帐户并手动提供其注册到该新服务的证明。（如果发现你不需要这样做，这部分无法支付的保险费用仅仅是隐藏起来了，由市场来承担）同样，如果您想让汽车能通过优步或基于小时的汽车租赁来参与分享经济，那么证明，结算付款和保险成本的工作会给市场带来摩擦。
In the web 2.0 model, you are restricted to handling every element on its own. To register the car, there is a separate process which involves creating an account with the Road and Maritime Services and proving ownership manually without the aid of cryptography. When you want to provide insurance to the car, you have to create another account and manually offer proof of its registration to that new service. (If you find not needing to do so, the cost of unpayable insurance merely is hidden and borne by the market.) Likewise, if you want to make the car available to share economy through Uber or hour-based car rental, the work of proving and settling payments and insurance cost adds friction to the market.

现在让我们在web3的世界中构想这一点，这些元素能够被通证化。供应商（在这个例子里面是holden）向新的拥有者提供所有权通证，在购买时转移给所有权者的通证又用于获取注册通证。内置的物联网允许骑车通过通证来证明所有权。
Now let's reimagine this in the web3 world whereby such elements can be tokenised. Vendor (in this case Holden) provides an ownership token to the new owner which can be used to operate the car. The token, transferred to the owner at the time of purchase, is in turn used to acquire the registration token. An inbuilt IoT device allows the car to be operated with proof of ownership via a token.

希望购买保险的所有者只需提供所有权证明和注册通证即可满足保险公司的要求。通过将通证与其要求相匹配来自动满足保险公司标准，并且一旦经过验证，保险公司可以向所有者发送保险通证以换取用户付款。 保险通证具有自己的功能和服务。
The owner, wishing to purchase insurance, only needs to provide the proof of ownership and registration token to be qualified to fulfil the requirements with the insurance company. The insurance companies standards are met automatically by matching the tokens to their requirements and once validated, the insurance company can send the owner an insurance token in exchange for payment. The insurance token carries its own functions and services.

如果车主希望成为优步司机，她可以通过提供所有权证明，保险轻松证明她的车辆足够好，并且通过通证注册。 优步然后自动向她提供一个Uber通证，根据所有者的需要，可以用来让自己成为Uber司机或允许第三方司机这样做。 这些流程都不需要手动验证或帐户创建。
If the owner would like to become an Uber driver, she can easily prove her vehicle is good enough by providing proof of ownership, insurance and registration with her tokens. Uber then automatically provides her with an Uber token which, depends on the owner's need, can be used to get himself started as an Uber driver or allow a 3rd party driver to do so. None of these processes requires manual verification or account creation.

更进一步，车主可以跳过优步，直接将车租给陌生人。 她不想让她的汽车被一些随意的陌生人破坏。她可以将她的租房者限制在那些拥有“更好的司机局”颁发的证明通证的人身上。 承租人证明他们有这个通证，向所有者支付一笔款项，并且原子性的发放一个临时通证，允许他们解锁并使用汽车一段时间。 这是在没有创建帐户的情况下完成的，或者需要提交大量文档来由车主手动验证。
Taking this even further, the owner can skip Uber all together and rent her car directly to strangers. Not wanting her car to be trashed by some random stranger, she can restrict her renters to those who have an attestation token issued by the 'better drivers bureau'. The renter proves they have this token, pays a sum to the owner and is atomically issued with a temporary token that allows them to unlock and use the car for a certain period of time. This is done without the creation of an account or need to submit tons of documents to be validated manually by the owner.

如果车主希望出售汽车，她只需要在任何网站上列出价格。 所有权通证和付款可以原子方式交换（确保买方或卖方都不会受到欺骗），新的所有者可以驾车离开，甚至无需面对面地与原始所有者会面。 新买家事先知道汽车是否已经注册，并且仅通过验证其钱包中的原始所有者的所有权通证而合法拥有。 一旦发生交换，原始所有者的通证就会失效，并且她无法再操作汽车。 一旦交换发生，也可以自动使保险单无效，并为原始所有者提供过早取消的折扣。
If the owner wishes to sell the car, she only has to list it on any website with a price. The ownership token and payment can be swapped atomically (ensuring neither the buyer or seller is cheated) and the new owner can drive away with the car without even meeting the original owner face to face. The new buyer knows in advance whether the car has been registered and is legally owned by merely validating the original owner's ownership token in their wallet. The original owner's token is invalidated once the swap occurs and she can no longer operate the car. It is also possible to automatically void the insurance policy once the exchange has occurred and provide the original owner with a rebate for premature cancellation.

本章用于展示愿景。 我们将在后面的章节中再次检查这种良好集成的通证化的汽车通证的技术层面。
This chapter serve to present the vision. We will have the opportunity to inspect the technical aspect of this well-integrated well-tokenised car token in later chapters again.

--
#### 通证化的挑战
#### The challenge of tokenisation

通证化需要构建一个通证并且与其事务规则和行为模式捆绑在一起，将他们从最初生成的系统中取出，是的他们可以在不同的场景下进行交易和使用。
Tokenisation requires bundling a token with its transaction rules and behaviour patterns, taking them off the system where they initially grew in, free them to be traded or used in different context.

允许用户通过通证与不同系统进行交互：在汽车这个例子中：汽车通证由制造商Holden发布，因为它包含和智能锁的 *打开*，*启动*，*锁定*  操作和Holden自己的web服务（*定位*），但它需要在其他环境中工作。例如 *拍卖* 动作由第三方拍卖网络服务提供。用户通过通证访问拍卖服务，无需注册和证明所有权。*共享清单* 由第三方服务提供，该服务将汽车的使用通证化为数小时或者数天，并逐个销售。所有者可以通过此通证访问这个市场，买家将通过此通证获得有关汽车的gps位置，开门和使用它的能力。
Allow users to interact with different systems through the tokens
:   In the car example, the car token is issued by Holden, the maker, and necessarily so because it contains code to interact with a smart lock (the *Open*, *Start*, *Lock* actions) and Holden's own web service (the *Locate* action), yet it needs to work in other environments. The *Auction* action, for example, is provided by a third party auction web service. The user access auction service through the token without the need of signing up and proving ownership. The *List for sharing* is provided by a third party service which tokenises the usage of the car by hours or days and sells them piecemeal. The owner can access such a market through this Token. The buyers will have information about the car's GPS location, the capacity to unlock the door and use it, through this token as well.

渲染通证并将其与可在用户钱包中执行的操作相关联：在汽车的示例中，如果注册过期，工作中的web组件会将注册通证绘制为红色或显示警告。过期的汽车将无法使用 *共享清单* 等操作，并且汽车的通证页面应该明确的将消息传递给用户。
Rendering a token and associate it with the actions they can perform in the user's wallet
:   In the car example, if the registration expired, the web component at work would paint the Registration Token red or display a warning. Actions like *List for sharing* will not be available with an expired car rego, and the integrated token interface should clearly pass that message to the user.

允许在通证上开发新协议：在汽车示例中，抵押可能是附加协议，也就是以太坊上下文中的ERC。 该协议可能有自己的实现，并且汽车通证可能会预先约定它。 同样，有流媒体，通信，赌注或其他协议（参见“魔术”章节）。 框架必须允许它们存在并通过通证使用。
Allow new protocols to be developed on tokens
:   In the car example, collateralization might be an additional protocol, an ERC in Ethereum context. The protocol might have its own implementation and the car token might pre-date it. Similarly, there are streaming, communication, staking or other protocols (See "Magic" chapter). The framework must allow them to exist and work with tokens.

将信任关系和业务背景传递给第三方：在汽车示例中，保险通证通过NRMA提供道路救援服务，NRMA是另一家未与驾驶员直接签约的公司。 然而，驾驶员可以通过保险通证访问此功能，并立即被确定为有资格获得帮助。 在此示例中，*信任关系*表示用户间接信任NRMA以提供路边援助，以在紧急情况下获取用户的GPS位置和身份信息。 *业务背景* 是指客户对路边援助的资格，例如保险支付，服务范围内的位置和未达到的年度上限等。在这个故事中，*信任关系*和*业务背景* 都必须在通证中，而不是 通过保险公司的网络服务集中，因为两者有不同的 a）可用性，b）隐私和c）集成要求[^ abc]。
Carry trust relationship and business context to 3rd parties
:   In the car example, the insurance token provides Roadside Assistance service through NRMA, another company not directly contracted by the driver. Yet the driver might access this function through the insurance token and immediately be identified as qualified for help. In this example, *Trust relationship* means that the user indirectly trusts NRMA to provide roadside assistance, to obtain the user's GPS location and identity information at the time of emergency. *Business context* means the customer's qualification for roadside assistance, like insurance paid, location in the range of service and annual cap not reached etc. In this story both *trust relationship* and *business context* has to be in the token, not centralised through the insurance company's web service since the two have different a) availability, b) privacy and c) integration requirements[^abc].

[^abc]: 可用性：NRMA 7*24小时在线，但是澳航保险 可以再公众假期或者晚上展厅服务。隐私：NRMA可以获取用户的GPR，但是澳航保险在法律上不可以。集成：大多数NRMA的客户不是通过Qantas Insurance 获得的，因此它将成为NRMA集成和额外安全问题的附加系统，以集成到Virgain Insurance的网络服务。在所有的三个钟，可用性可能是最明显的。想象一哈客户会有多生气，当他的汽车在澳大利亚贫瘠的内陆地区抛锚，这个时候发现无法或者道路援助，因为保险公司的网络服务器正在为了 ”更好的服务用户“ 升级。
[^abc]: Availability: NRMA is online 24/7 but Qantas Insurance can suspend their services in public holidays or at night. Privacy: NRMA can learn user's GPS location but Qantas Insurance isn't legally allowed to learn it. Integration: Most of NRMA's customers are not obtained through Qantas Insurance, so it would be an additional system to integrate and extra security concern for NRMA to integrate to Virgain Insurance's web service. Of all three, availability might be the most visible. Just imagine how angry a customer will be, having his car breaking down in the middle of the barren Australian outback, and learn that the road-side assistance can't be authorised because the insurer's web service is upgrading "For a better user experience".

＃设计要求
# Design requirements

我们断言需要一种描述性语言（TBML）来允许区块链技术实现“完成市场”和“集成网络”。 TBML代表令牌行为标记语言。
We assert that a descriptive language (TBML) is needed to allow blockchain technology to enable "frictionless markets" and an "integrated web". TBML stands for Token Behaviour Markup Language.

由于TBML是一个解决方案层，而不是像以太坊和等离子(译者注：一种以太坊的二层扩容框架)这样的基础层技术，我们选择通过实例介绍该技术，并为观众的观众提供丰富的商业环境讨论。
By virtue of TBML being a solution layer rather than base-layer technologies like Ethereum and Plasma, we choose to introduce the technology by example, and provide rich business-context based discussion for a boarder specturm of audience.

## 地址 完全市场的需求
## Address "Frictionless Market" needs

仔细研究“市场”，市场并不是一个超载信息的嘈杂渠道; 更重要的是，这是一个交付与付款的地方。 由于区块链不依赖于中间商，即交易主机，我们的重点转变为交易的通证，即 *可交付成果* 和 *支付* ，以及他们在市场中的角色。
Taking a closer look at "market", a market is not a noisy channel overloaded with information; more importantly, it is a place where delivery versus payment happens. With blockchain relying less on the middlemen, the host of the trades, our focus is turned into the tokens being traded, that is, *deliverables* and *payments*, and their role in market.

交付
：金钱可以买到各种各样的东西：资产，商品和服务。
deliverables
:    All sorts of things money can buy: assets, goods and services.

付款
：Ether，DAI，Sovereign。 任何类似货币的东西。 只有可编程货币才与本文相关
payment
:    Ether, DAI, Sovereign. Anything currency-like. Only programmable currencies are relevant to this paper.

市场
：市场是交割与付款发生的地方。 *市场*是一个概念，而不是一个实体市场。 在网站上结账的用户正在访问市场。 她不必在市场（例如亚马逊）这样做。
market
:    Market is where delivery versus payment happens. *Market* is an concept, not a marketplace. A user who checks out on a website is accessing a market. She doesn't have to be in a marketplace (e.g. Amazon) to do so.

向* market *提供*可交付*和*付款*方标记“插件”。
TBML provides both *the deliverable* and *the payment* side tokens to "plug-in" to the *market*. 
这样的框架对于通证的呈现，索引，交易，交易，拍卖，组合......以实现完全市场至关重要。
Such a framework is essential for tokens to be presented, indexed, transacted, traded, auctioned, combined... to work towards a frictionless market.

我们将通过每个 *可交付* 方面和 *付款* 方面的示例介绍TBML。
We will introduce TBML through an example on each of the *deliverable* side and on *payment* side.

## 可交付方面的示例 1% 房产通证
### Deliverable side example: 1% property token

让我们想象一下“1％房产”的市场。房产所有者可以发放许多通证，每个通证代表1％的房产所有权。他可以出售这些通证以换取现金。
Let's imagine a market for "1% property". A property owner can issue many pieces of a token, each represents 1% ownership of the property. He can sell these tokens for cash.

买家需要了解相当多的信息。很容易理解，如果基础通证被出售，这样的通证将获得1％的销售收入，但需要更多细节
A buyer needs to know quite a bit of information. It's easy to understand that such a token would fetch 1% of the sales revenue if the underlying property is sold, but a lot more details are needed:

1.房产在哪里以及它的状态如何？
1. Where is the property and what status is it in?

2. 1％的房产代币所有者可以投票吗？例如，有关丛林火灾保险的购买决定？
2. Can a 1% property token owner vote?  For example, on the purchase decision to insurance against a bush fire?

3. 1％是否在房产销售时自动转换为货币，或者代币持有人是否可以选择继续持有？
3. Is the 1% automatically converted into currency at the time of property sales, or can the token holder elect to continue holding it?

4. 是否正确承保了令牌以防止双重抵押？
4. Is the token properly underwritten to prevent double-collateralization?

5. 如果房产是抵押贷款的抵押品，清算事件的条件是什么？
5. If the property was collateralized for a mortgage, what is the condition for a liquidation event?

6. 提供买方身份证明是购买的条件吗？
6. Is providing a buyer's identity attestation a condition of a purchase?

7. 卖方是房产的实际所有人吗？
7. Is the seller the actual owner of the property?

8. 过去几年该地区类似物业的表现如何？
8. What was the performance of similar properties in the region in the past years?


9. 这家酒店的历史销售价格是多少？
9. What was the historical sales price of this property?
具体到区块链，我们还有：
Specific to blockchain, we also have:

10.如何正确安全地为资产建立交易（购买，投票等）

10. How to correctly and securely construct a transaction for the asset (purchase, voting etc)

我们将这些贸易敏感信息分为四类：

  产品说明 [^ pd]。 项目2,3,5,6在PD中
- 证明信息。 项目1,4,6,7在Attestations中。
- 参考信息。 项目8,9。
- 行为信息（如何执行资产行动）。 项目10。

We categorise these trade-sensitive information into four categories:

- product description[^pd]. Item 2, 3, 5, 6 are in PD
- attested information. Item 1, 4, 6, 7 are in Attestations.
- reference information. Item 8, 9.
- action information (how to perform an asset action). Item 10.

可以理解的是，买家需要访问所有这些信息以做出明智的决定。
Understandablly, the buyers need to access all these for an informed decision.

[^ pd]这个词来自金融部门，通常用于描述包装的投资产品。 它基本上是指计算利润的公式和公式中的变量的当前值。
[^pd] The word is loaned from the financial sector, usually used to describe packaged investment products. It basically means the formular which profit is calculated and the current values of the varibales in the formular.

#### 产品描述
#### Product description

产品描述信息通常在智能合约中。 在以太坊的情况下，这些可以通过进行一些智能合约函数调用来获得，因此，唯一需要的工作是将它们转换为演示文稿 - 通常意味着转换为用户语言并将“实际”值转换为精心打勾的复选框。 这有助于介绍TBML的第一个功能：充当智能合约的表示层。
Product description information is typically in the smart contract. In Ethereum cases, these can be obtained by making a few Smart Contract function calls, therefore, the only needed work is to convert them into presentation - usually it means translating to the language user speaks and converting "True" value into a nicely ticked checkbox. This serve to introduce the first functionality of TBML: acting as a presentation layer for smart-contracts.

    <attribute-type id="voting-right">
       <name xml:lang="en">Voting right</name>
       <name xml:lang="zh">投標權</name>
       <origin contract="holding-contract" as="mapping">
          <function name="getVotingRight">
	     <inputs>
	        <uint256 ref="TokenID"/>
	     </inputs>
	  </function>
          <mapping>
	     <option key="0">
	         <value xml:lang="en">No Voting Right</value>
		 <value xml:lang="zh">無投標權</value>
             </option>
	     <option key="1">
	         <value xml:lang="en">Voting rights on sale</value>
		 <value xml:lang="zh">可投標決定售出</value>
	     </option>
	     <option key="2">
	         <value xml:lang="en">Voting rights on expense (e.g. insurance)</value>
		 <value xml:lang="zh">可投標決定維護項目如添置保險</value>
	     </option>
	  </mapping>
	</origin>
    </attribute-type>

这个简化的`attribute-type`代码片段允许从“holding-contract”获取投票权的值，这是一个在TBML中其他地方定义的智能合约，并以几种语言之一呈现。

This simplified `attribute-type` code snippet allows the value for Voting Right to be fetched from `holding-contract`, which is a smart contract defined somewhere else in the TBML, and present it in one of a few languages.

#### 证明信息
#### Attested information

证明只是一条用来说明事实的经过签名的信息。通常使用证明来表示满足交易的条件，更多关于证明的信息如下
Attestation is just a signed message stating a fact. Attestations are often used to satisfy the conditions of the transactions. More on that in the chapter Attestations.

在1％财产通证的示例中，涉及的证明是：
In the 1% property token example, the involved attestations are:

 - 通过身份管理机构和所有权契约办公室，以证明发行人对财产的所有权。
- by identity authority and title deeds office, to attest the issuer's ownership of the property.
 - 通过抵押权限[^ set-operation]来防止双重抵押
- by collateralization authority[^set-operation] to prevent double collateralization
 - 由买方提供投资此类资产的身份或能力
- by buyers, for providing identity or capacity to invest in this type of asset

[^ set-operation]：最终，这可能是一个加密集合操作，但即使发生这种情况，也需要在TBML中描述指示上下文（用户代理）进行计算的元数据。
[^set-operation]: Eventually, this could be a cryptographic set operation, but even if that happens, the metadata directing the context (user-agent) to proform the computation still needs to be described in TBML.
前两个证明并未存储在智能合约中，由于成本（交易的大小和数量）和隐私的原因。可以采用零知识证明来证明该证明适用于所述财产和所述所有者的通用证据，并且它尚未过期。 TBML中还描述了预期和可验证的证据。
The first two attestations are not stored in smart contract for cost (size and number of transactions) and privacy reasons. It's possible to utilise zero knowledge proof to provide a generic proof that the attestation is for the said property and said owner, and it has not expired. What proofs are expected and can be validated is also described in TBML.

此外，交易需要来自买方的身份证明或投资能力证明。 这些也在TBML中描述，因此上下文（例如，用户代理）可以防止用户在没有限定证据的情况下提交交易或帮助用户为购买交易选择合适的证明。
Furthermore, the fact that the transaction requires an identity attestation or investment capacity attestation from the buyers. These are described in TBML as well so the context (e.g. user-agent) can prevent the user to submit a transaction without qualifying proof or help the user to select suitable attestations for a purchase transaction.

#### 参考信息
#### Reference information

参考信息与通证相关，由Web服务提供，通常通过RESTful API调用。[^ trusted-information]
Reference information is what relevant to the token and provided by web services, typically through a RESTful API call.[^trusted-information]

[^ trusted-information] 最初我们将其称为“可信信息”，这意味着以前的房产销售价格或区域性能数据等数据只是“提供”，没有区块链证明或证明，因此，必须由用户自己信任。 事实证明，这个术语是错误的，因为一些开发人员认为它意味着“经过验证的信息”，并且已经提供了可靠信息。 因此，我们使用了一个不太精确的术语“参考信息”，遗憾的是，它就像一个包罗万象的短语。
[^trusted-information]: Originally we call it "Trusted information", meaning data such as previous property sales price or regional property performance data is just "provided", without blockchain proofs or attestations, hence, it has to be explicitly trusted by the user. As it turned out, this term misfired as some developers think it means "proven information" and provided as trusted already. So we used a less precise term "Reference information", which, unfortunately, feels like a catch-all phrase.

由于TBML由通证发行者签署（不是通证所有者 - 通证发行者通常是部署智能合约的实体），因此假定来自TBML中指定的web apis的参考信息是可信的。 安全章节将详细说明不同的信任级别。
Since TBML is signed by the token issuer (not token owner - the token issuer is often entity that deployed the smart contrat), the reference information sourced from the web apis specified in TBML is assumed trusted. The security chapter will detail different levels of trust.

今天，与通证相关的所有此类信息通常一起保存在由部署通证的同一实体制作的DAPP网站上。 我们认为，要使通证有效地市场化，需要将其抽象出来并置于通证行为语言TBML中。
Today, all such information related to a token is usually held together on a DAPP website made by the same entity that deployed the token. We argue that for tokens to be effectively marketized, It needs to be abstracted out and placed in the token behaviour language TBML.

#### 行为信息
#### Action information

规定构建区块链交易的正确方法，如：
Dictates the correct method to construct a blockchain transaction, like:

 - 需要哪些证明来证明买方的购买能力。
 - 购买需要哪些参数（例如1％的股份数量）。
 - 如何呈现购买表单并转换为用户的本地语言。
 - 是否满足条件（例如，在相关财产被清算后无法进行购买）。
- What attestations are needed to prove the buyer's capacity to purchase.
- What parameters are needed for a purchase (e.g. number of 1% shares).
- How to render the purchase form and translate to user's local language.
- Is the condition all met (e.g. a purchase isn't possible after the underlying property is liquidated).

这些信息是一套超级智能合约可编程接口（In Ethereum，称为ABI），附加部分是业务逻辑（例如财产必须仍然有效且卖方仍然拥有它）和表示逻辑（例如消息“The property” 被清算。不再购买“）。
These information is a super-set of smart contract programmable interface (In Ethereum, called ABI), with the additional part being business logic (e.g. property must be still valid and seller still have it) and presentation logic (e.g. the message "The property is liquidated. Purchase no longer possible").

总之，TBML允许上下文（用户代理或交易引擎）：

 - 从持有智能合约，证明和参考资料中获取通证相关信息。
 - 生成通证的视觉或音频呈现
 - 生成可执行的操作列表以及如何构建交易。
In conclusion, TBML allows the context (user-agent or trading engine) to:

- Fetch token related information from its holding smart contract, attestations and references.
- Produce a visual or audio rendering of the token
- Produce a list of actions that can be performed and how to constrct the transactions.

任何一方都能够使用TBML渲染和应用函数到通证，包括通用市场，用户代理和第三方应用等实体。 我们将这部分称为“上下文”。
Any party is able to render and apply functions to the token using TBML, including entities like generic marketplaces, user-agents and 3rd party apps. We call these parties "context" in general.

### 为什么需要TBML
### Why TBML

通过演示的第一个示例，我们利用这个机会阐明了为什么需要TBML，而不是目前通过DApp提供资产访问的主流方式。 我们认为目前流行的方法不适合创建无摩擦市场，而TBML可以提供 *互操作性*，*可扩展性*和*安全*等保障。
With the first example demonstrated, we use the opportunity to articulate why TBML is needed, over the current prevailing way of providing asset access with a host DApp. We argue that the current prevailing method is not suitable for creating a frictionless market, while TBML could, by providing reasons in the areas of *interoperability*, *scalability* and *security*.

#### 互操作性：
#### Interoperability:

假设名为Peter的房产大师希望创建一个名为“Peter's Pride Asset”的网站，在那里有市场上最好的房产。他可以创建这些房产的列表，其中包含当前价格，位置，建筑物年龄甚至照片的丰富信息，用户可以通过点击购买。但是他没有理由必须要这样做，因为通证的数据在区块链上并且交易不需要中间人就能执行。然而，他需要如何在他网站上呈现令牌的只是，比如如何持有智能合约中获取通证的到期时间。如果基础智能合约经历了变化，例如添加属性（费率），他的网站将需要升级。
Suppose a property guru named Peter wishes to create a website called "Peter's Pride Asset", where he selects the best properties available on the market. He can create a listing of those properties with rich information of the current price, location, age of the building and even photos, which the users can purchase with a click. There is no reason that he needs permission to do so because the data of those tokens are on the blockchain and the transaction of those tokens requires no middlemen. However, he would need to obtain the knowledge local to how to render the token on his website, like how to get the expiration of a token from its holding smart contract. If the underlying smart contract has gone through changes, like adding an attribute (e.g. council rate), his website would need to upgrade.

同样，交易规则也可能会更新，要求买房提供身份证明作为购买的一部分。如果没有快速升级，他的用户将提交不符合要求的交易，并且在接下来的区块中被拒绝。最终，他会将通证的呈现和交易，交给与该通证绑定的Dapp，这会恢复到中心化状态并限制该领域的创新和竞争。
Similarly, the transaction rule might be updated to require the buyer to submit an identity attestation as part of a purchase. Without a speedy upgrade, his users would submit transactions not conforming and get rejected later in the blockchain. In the end, he would resort to passing the rendering and trading of the token to the Dapp tied to this token, returning to a centralised status and limit the innovation and competition in this space.
类似的方式，假设一个投资者论坛允许成员使用它们的1%房产通证登录，每个帖子下的通证呈现都需要来自与通证绑定的Dapp。这将会是一个非常大的工作量，为论坛提供通证并且保持代码更新，并且这个将会和Dapp的可用性强耦合。
In a similar fashion, suppose an investors' forum where the members are allowed to login using their 1% property token, the rendering of the token, under each post, would need to be sourced from the Dapp tied to the token, since it's too much work for a forum to render the token and keep the code updated. Such sourcing would require permission and might be tied to the availability of that Dapp.

#### 可扩展性
#### Scalability

水平地，相同类型的资产可能在多个网络（如等离子链）上具有其通证实例。买方可能只对澳大利亚的资产感兴趣，因此仅与澳大利亚1％房地产网络相关联。可能难以拥有一个全知的节点来为所有现有通证提供呈现的令牌信息，尤其是在设计网络时考虑到隐私的情况。因此，为了扩展，必须从对通证的访问中分离关于通证（TBML）的知识。
Horizontally, the same type of asset might have its token instances across multiple networks like Plasma Chains. A buyer is likely to be interested only in assets in Australia, and therefore only connected to the Australian 1% Property network. It can be difficult to have an all-knowing node to provided rendered token information for all existing tokens, especially if a network is designed with privacy in mind. Therefore, to scale, the knowledge about the token (TBML) must be detached from the access to the token.

垂直 - 通过说* vertical *，我们的意思是向上构建，使用通证交易构建结构化的交易或在通证之上创建结构化通证。此类事务和通证访问组件通证。例如，如果我们想要一个通证，其组成是来自100个全球城市的样本的1％资产通证，对于中型投资者来分摊风险，必须使用关于成员的知识构建可以操纵此类通证的系统通证。它再次不能依赖于与该资产相关的原始Dapp的可用性，安全性和开放性。 TBML可以在中间用于制作这样的通证。
Vertically - by speaking *vertical*, we mean to build upward, to building structured transactions using a token transaction or creating structured tokens on top of a token. Such transaction and token access the component tokens. For example, if we desire a token whose make up is a 1% property token from a sample of 100 global cities, for mid-size investors to distribute the risk, a system that can manipulate such a token must be built with the knowledge about member tokens. It again cannot depend on the availability, security and openness of the original Dapp tied to that asset. TBML would work in the middle for the making of such tokens.

如果我们以Peter's Pride Property网站的例子作为Hello World示例，可能需要用户提交交易，不仅要购买通证，还要提示Pride。 如果只有停止的发行人的DAPP知道如何组装通证购买交易，这对彼得来说是不切实际的。
If we follow the example of Peter's Pride Property website as a Hello World example, it might need the user to submit a transaction not only purchase a token, but also tips Peter in the meanwhile. If only the token's issuer's DAPP knows how to assemble a token purchase transaction, this will be impractical for Peter.

即使在简单的场景中，垂直情况自然也会比这复杂得多。 您将在本章“基础网络”部分的电子商务故事中看到一个例子。
The vertical stack naturally can be a lot more complicated than this, even in simple scenarios. You will see one revealed in an e-commerce story in the "Integrate the web" section of this chapter.

#### 安全性
#### Security

即兴创建一种模型是不切实际的，其中用户可能签署的每个事务都以用户可读的格式呈现。使用事务可视化工具开始这样的工作很简单，向用户解释一个神秘的事务负载，类似于Linux的`identify（1）`命令，但最终系统集成和UX需求将超过字典样式事务可视化器能够完成的范围。
It is impractical to improvise a schema where every transaction the user might sign is rendered in a user-readable format. It's easy to start with such an effort with a transaction visualiser tool, interpreting an enigmatic transaction payload to the user, similar to Linux's `identify(1)` command, but ultimately the system integration and UX needs would surpass what a dictionary style transaction visualiser can do.

以1％房产通证为例; 确认可能如下所示：您打算用45个Ethers购买1％的房产＃802820，您确定吗？
Take the 1% property token as an example; a confirmation might look like this: You are going to purchase 1% of property #802820 with 45 Ethers, are you sure?

用户不确定他正在观看的玻璃天花板设计的两居室的房子是＃802820。
The user will be unsure if the glass ceiling designer 2-bedroom house he is watching is #802820.

基于字典的翻译可视化器不能做的更好，因为正确呈现属性标记需要的不仅仅是文字处理。 这个限制很容易发现，即使没有在本章的“集成Web”部分中介绍集成方案。
A dictionary based translation visualiser cannot go further because correctly rendering the property token requires more than word processing. This limit is easily hit even without introducing integration scenarios in the "Integrate the web" section of this chapter.

最终，使用代码生成交易，用户必须将信任委托给代码。 用用户的话说，我正在访问与此通证绑定的网站，所以我相信我签署的这个交易是为了我在使用网站时的意图而生成的。 这是一个破碎的信任模型，就像的TLS模型一样是对网站的信任而不是内容。
Eventually, a transaction is generated with code, and the user would have to delegate the trust to the code. In a user's words, I am accessing the website tied to this token, so I will trust that this transaction I am signing is generated for the intention I have while using the site. This is a broken trust model, a regression to the TLS model of trusting the site instead of the content.

TBML旨在分离通证呈现代码和交易生成代码，并将它们打包到其容器中，由用户可能信任的一方签名（通常由用于部署智能合约的相同密钥签名）。 有不同的信任级别，我们将在后面的章节中详细介绍。
TBML is designed to separate token rendering code, and transaction generating code and package them into its container, signed by a party that the user is likely to trust (often, signed by the same key used for deploying a smart contract). There are a few trust levels, which we will detail in later chapters.

从Peter's Pride Property推荐网站购买1％房产通证的用户可以获得一个渲染和交易包，由创建此类代币的持有合同的同一组人签名。 因此，用户可以从具有类似信任级别的任何网站购买资产，或者从微信或Facebook私人消息购买资产，并且知道它是正在呈现和交易的真实交易。
A user who is purchasing a 1% property token from Peter's Pride Property recommendation website can be supplied with a rendering and transaction package, signed by the same group of people who created the holding contract of such tokens. Therefore the user can purchase assets from any website with a similar level of trust, or purchase it from a WeChat or Facebook private message and know it is the real token being rendered and transacted.

## 付款方示例：DAI通证
## Payment side example: DAI token

DAI是一种用于支付的代币 - 购买加密货币，购买商品和服务等等。 它锚定美元的价值。 没有固定供应上限，它本身不是一个投资品种。
DAI is a token designed for payment - purchasing security token, purchasing goods and services and so like. It's intended to match USD in value. Not fixing the supply cap, it is not itself an investiment candidate.

在许多方面，DAI的功能类似以太网，它是以太坊的基础货币。 但是，它不能成为Ether的替代品。
In many ways DAI functions like Ether, the base currency in Ethereum. However, it can't be a drop-in replacement for Ether.

首先，为以太坊编写的Dapps可能不知道用户有DAI令牌，除非它明确支持DAI。 例如，接受以太币作为付款的比萨订购服务不能轻易地开始接受DAI令牌。 即使DAI提供DAI-to-Ether网关服务也是如此，该服务以原子方式在同一事务中将DAI转换为以太网，使用生成的Ether来购买Pizza。
First, the Dapps written for Ethereum may not be aware that the user has DAI token, unless it explicitly support DAI. A Pizza ordering service that accepts Ether as payment, for example, cannot trivially start to accept DAI token. This is true even if DAI provides a DAI-to-Ether gateway service which, in an atomic fashion, converts DAI to Ether in the same transaction which uses the resulting Ether to purchasing Pizza.

如果Pizza网站没有升级，用户必须首先将DAI转换为Ether，然后通过第二次交易购买Pizza。 这样的过程不仅不方便，而且缺乏原子性，这意味着用户需要通过努力将DAI转换为Ether，但是由于Pizza已经售罄而无法结账，用户必须处理他已经购买的eth
If Pizza website doesn't upgrade, the user has to convert DAI to Ether first, then, purchase Pizza with a second transaction. Such a process is not only inconvenient, but lack atomicity, meaning that the user could have converted DAI to Ether trough the effort, only to fail the checkout since the Pizza is sold out, and ended up with additional Ethers that she has to deal with.

值得注意的是，披萨网站无法升级到支持DAI，而不知道如何获取用户的DAI余额[^ balance-is-privacy]（为了不浪费交易费结果只发现DAI余额不足），如何构建DAI撤销事务或DAI-Ether网关事务，并对DAI持有合同进行直接智能合约函数调用。
It's worth noticing that the Pizza website cannot upgrade to support DAI without knowing how to discover the user's DAI balance[^balance-is-privacy] (to not to to waste a transaction fee just to find the DAI balance is insufficient), how to construct a DAI withdraw transaction or DAI-Ether gateway transaction and make direct smart contract function calls to the DAI holding contract.

[^balance-is-privacy]:最终，披萨网站不仅不需要检查余额，因为TBML处理它，也不需要知道余额。 这将需要底层区块链的支持，但如果我们继续当前的趋势，继续关注业务逻辑的网站也关心支付逻辑，这最终无法完成。
[^balance-is-privacy]: Eventually, the Pizza website would not only be oblivious about how to check balance, since TBML handles it, but also not possible to know the balance. This would require underlying blockchain's support, but ultimately cannot be done if we continue the current trend where website, who should care about business logic, also care about payment logic.

当然，Pizza网站不是管理这些付款方详细信息的最佳位置。 TBML通过以下方式解决了这个问题
Naturally, the Pizza website isn't in the best position to manage these payment-side details. TBML addreses this problem by

1.封装支持DAI所需的智能合约函数调用，以及用于在TBML中构建所需事务的javascript，由DAI发行者签名。
1. Encapsulating the smart contract function calls needed for supporting DAI, along with the javascript to construct needed transactions in TBML, signed by DAI issuer.
2.TBML，兼容性提供浏览器端实现和基于javascript的实现，以便Pizza商店可以调用泛型操作来返回ETH（或任何可接受的货币）并使用TBML中的支付逻辑来交易。
2. Providing a browser side implementation and a javascript based implementation for TBML compatibility, so that the Pizza shop could just call a generic action to return Ether (or any acceptable currency) and let the payment logic in TBML work at transaction.

TBML嵌入支付逻辑和表示的能力意味着它不仅可以用用户的语言显示消息（如余额或“余额不足”消息），而且可以执行预检余额等功能，暂停结账流程以便用户 可以执行充值流程并返回结帐流程以完成结账。
TBML's capacity to embed payment logic and presentation means that not only it can display messages in user's language (like balance or "insufficient balance" message), but it can perform functions like pre-checking the balance, pause the checkout flow so that the user can perform a top-up flow and return to the checkout flow to finalise the checkout.

对于用户来说，该过程类似于结账过程引导用户到Paypal来完成交易，唯一的区别是该过程在更强大的本地用户代理中发生。
To the user, the process resembles a bit like the checkout processs leads the user to Paypal to finalise the transaction, except the process happens locally in an enhanced user-agent.

我们再次抢到，目前的方法不适合创造完全市场，但是TBML可以，通过提供*互操作性*，*可扩展性*和*安全性*来创造完全市场。
We again argue that current prevailing method is not suitable for creati
ng a frictionless market, while TBML could, by providing reasons in the areas of *interoperability*, *scalability* and *security*.

总之，Pizza网站没有必要自行处理支付方逻辑的所有事情。 传统方法是让Pizaa网站使用MakerDAO项目提供的javascript。 javascript可能使用也可能不使用MakerDAO提供的RESTful API
As concluded, Pizza website would not have the necessary payment side logic to handle everything on its own. The traditional approach is to let the Pizza website use the javascript sourced by MakerDAO project. The javascript may or may not use a RESTful API provided by MakerDAO

这种方法通过引入其他一些问题解决了一个问题。
This approach solves one problem by introducing quite a few others.

#### 安全性
#### Security
当用户进行购买尝试时，使用本地javascript（Pizza shop javascript）和DAI提供的所谓安全javascript的组合来创建交易。 向用户呈现交易载荷，该交易的载荷包含访问DAI合同的参数，例如， 支付金额，以及访问比萨网站合同的参数，例如 购买比萨饼的数量和选择的浇头。 显然，这样的交易必须发送到DAI合同并通过（代理）到披萨店合同。
When the user makes the purchase attempt, the transaction is created with the combined effort of local javascript (Pizza shop javascript) and the supposedly secure javascript supplied by DAI. The user is presented with a transaction payload that contains both the parameters to access DAI contract, e.g. amount to pay, and the parameters to access the Pizza website contract, e.g. amount of pizzas to buy and the toppings of choice. Apparently such a transaction has to be sent to DAI contract and channeled (proxed) to the Pizza shop contract.


有两个直接[^minor-security-concerns]安全问题。 首先，网站没有正确使用MakerDAO javascript库，其中包含最终的交易构建器。 其次，它不是MakerDAO真正的的javascript，而是由黑客取代的版本。
There are two immediate[^minor-security-concerns] security concerns. First is that the website didn't use the MakerDAO javascript library correctly, which has the final transaction builder in it. Second is that it is not MakerDAO's javascript at work, but a version replaced by a hacker.

[^ minor-security-concerns]：当两个系统集成网络上时，通常存在大量安全问题。 举一个例子，如果一方未更新代码以反映另一方的更改，则可能会生成格式错误的交易。 跟踪这些交易允许攻击者定位未更新的网站。
[^minor-security-concerns]: When two systems plug on the web, usually there are a hoard of security concerns. To give one example, if a side didn't update the code to reflect the other side's change, the resulting malformed transaction might be rejected. Tracing these transactions allow an attacker to target websites not updated.

这些问题通过TBML中使用的封装方法解决。
These issues are addressed by the encapsulation method used in TBML.

首先，交易生成代码由MakeDAO单独签名，并与用户代理方分开更新。 网站的代码不必签名，因为它只提供业务逻辑，而不是支付逻辑。 比如，如果发现错误，DAI可以通过更新这些签名的指令来暂停付款，而且Pizza网站的行为就像已经更新并解决问题一样。 如果发现该错误存在于DAI控股合同中，并且部署了替换合同，MakerDAO将更新TBML并再次签署，而Pizza网站不需要任何事情。
First, the transaction forming code is signed by MakeDAO separately and updated separately from user-agent side. The website's code doesn't have to be signed because it just supplies the business logic, not payment logic. Say, if a bug is found, DAI can suspend the payment by updating these signed instructions, and the Pizza website would behave as if it has been updated to address the issue. If the bug is found to be in the DAI holding contract, and a replacement contract is deployed, MakerDAO would update TBML and sign it again, without Pizza website having to do anything.

其次，通过明确要求用户信任MakerDAO签署的TBML，用户不需要信任Pizza网站对交易内容的呈现，因为它将由受信任的MakerDAO TBML呈现
Second, by explicitly asking the user to trust the TBML signed by MakerDAO, the user would not need to trust Pizza website's rendering of the transaction content, since it would be rendered by the trusted MakerDAO TBML.

！[使用TBML付款。 请注意，* Complete Order *按钮不在网站上，而是在Dapp浏览器生成的TBML令牌区域中，其中呈现交易的代码已预先签名。]（payment-in-wallet.jpeg）
![A payment using TBML. Notice that the *Complete Order* button is not on the website, but in the TBML token area generated by Dapp browser, where the code to render the transaction is pre-signed.](payment-in-wallet.jpeg)

第三，如果需要添加安全协议，例如，来自网站的证明（可以重新使用SSL证书）来证明接收智能合约的交易，或智能合约通过域名返回网站的明确信任， 额外的逻辑是升级dapp浏览器来提供对新的TBML功能的支持和通证发现者对新TBML代码的更新，而无需触及网站。
Third, if secure protocols needs to be added, for example, an attestation from the website (can re-use the SSL certificate) to certify the transaction receiving smart contract, or the smart contract returning explicit trust of the website by domain name, the additional logic can be a combined effort of upgrading the dapp browser's support of new TBML feature and the token issuer's new TBML code, without touching the website.

#### 互操作性
#### Interoperability

添加对DAI本身的支持是很麻烦的，更不用说添加其他付款方通证了。 在2017-2018年的狂热中，许多支付方通证被发明并投入大量资金。几乎任何宣传不作为加密货币的东西都概述了他们的通证可用于支付或共同支付某些商品和服务的某种方式。 例如，电力通证被发明为未来象征化电力的货币。 他们中的大多数只是笑话，但如果他们开始工作呢？ 即使这些通证中只有10％由自己的ICO团队完成，但所有这些通证都会在将DAI通证集成到市场中时遇到类似的麻烦。
Adding support for DAI itself is trouble enough, not to mention adding other payment side tokens. In the 2017-2018 frenzy, a lot of payment side tokens are invented and heavily invested in. Pretty much anything advertised not as a security token outlines some way their token can be used to pay or co-pay some goods and services. Electricity tokens, for example, is invented as the currency of the future tokenised electricity. Most of them are jokes, but what if they are put to work? Even if only 10% of these tokens are done by sincerer ICO teams, all of them would forsee similiar trouble as the integration of DAI token into the market.

每种付款方货币都有自己的付款方逻辑。以DAI为例，它具有以下支付方逻辑：
And each payment side currency brings its own payment side logic. Take DAI for example, it has these payment side logic:

1. DAI令牌的创建需要一个称为CDP的设置阶段。
2. CDP的风险等级发生变化。用户应收到其CDP处于清算风险的通知。我们将在下一章再次讨论这种情况。
3. 如果余额不足，但用户在他/她的帐户上有相当多的Ethers，她可以暂停结账，然后返回结帐。
1. The creation of DAI tokens requires a set-up phase, called CDP.
2. The risk level of a CDP changes. Users should receive a notification of their CDP is at liquidation risk. We will cover such case again in the next chapter.
3. If the balance runs low, but the user has quite a bit of Ethers on his/her account, she may pause the checkout to top up before returning to the checkout.

当架构师读到这里的时候，他可能会决定这些都在外部完成。如果发生任何这些情况，只需将用户踢回MakerDAO网站即可。这不不是像Point + Pay这样的支付方创新，其中选择与支付在同一屏幕上选择。 事实上，您可以观察到中国支付方创新的大量例子，例如：
An architect might read it here and decide these can all be done out of band. Just kick the user back to the MakerDAO website if any of these happens. This would not address payment side innovation like Point+Pay, where the points are selected at the same screen as payment. In fact, you can observe a proliferationDictionary of payment side innovations in China for examples:

- 小额信贷和抵押贷款
- Micro-credit (e.g. 花唄) and collatoralised credit
- 当购物行为与小额信贷的鼓励行为相匹配时使用积分，例如 在海外购物。
- Points to use when the shopping behaviour matches the encouraged behaviour of micro-credit, e.g. shopping overseas.

- 每天花费超过1000元的现金返还。
- Cashback when you spent more than ¥1000 in a day.

 - 红包，只能用于支付消费。
- Red packet that can only be used in paying consumption.

 - 第100次，第200次..600次付款的彩票。
- Lottery on being the 100th, 200th.. 600th payment.

 - 针对特定购物行为的免费送货保险（例如，鼓励购物者倾向于降价运输，因为它因交货缓慢而失去优势）。
- Free shipping insurance on selected shopping behaviour (e.g. to encourage shoppers to favour drop-shipping as it loses advantage thanks to its slow delivery).

 - 预付费网上购物支付卡，如在澳大利亚邮政中销售的支付宝卡。
- Prepaid online shopping payment cards, like the Alipay cards sold in Australia Post.

TBML打算为支付方创新和可交付方提供空间。 传统上，合作伙伴支持抑制了支付方创新。 美国运通实施了支付API的积分，但在过去几年中，只有不到5％的合作伙伴电子商务网站将此作为结账选项提供。
TBML intends to give room for payment side innovation as well as deliverable side. Traditionally, partner support used to curb payment side innovation. American Express implemented points to pay API but after years only less than 5% of partner e-commerce websites provided this as a checkout option.

#### 可扩展性
#### Scalability

付款和交付可能不在同一区块链上。
The payment and delivery may not be on the same blockchain.

在dapp网站中呈现用户的余额简要提到几页后的隐私问题，但作为区块链扩展，dapp的服务器端可能无法在某些数据（如余额）上同等访问客户端。 网站可能只会观察交易结果，并乐意按规则交付实物或象征性商品。
Rendering user's balance in dapp website is briefly mentioned as a privacy issue a few pages back, but as blockchain scales, the dapp's server side may not have equal access to the client on some data like balance. It's possible that the website only observes the result of the transaction and happy to deliver physical or tokenised goods by rules.

任何可扩展性计划都不太可能不涉及dapp浏览器和钱包的参与。 他们使得dapps使用他们可以提供的任何高级JavaScript来处理付款方面的情况。
It's unlikely any scalability plan will not involve the participation of dapp browsers and wallets. They results in situation that dapps could not take care of the payment side with whatever advanced javascript they can supply.

## Address the "Integrate the web" need

We trace the reason that the web is poorly integrated to the only link between the units of the web, i.e. URL links. A link carries no business process, authentication or trust relationship. There are no anchoring points for integration on links.

We believe the token is the anchor points for integration. Again, this is best illustrated by examples.

Suppose a user purchases an iPhone from Harvey Norman, an online retailer, using the blockchain. The input of the transaction will be a type of currency; the output, in this case, will be three tokens:

- a shipping token, which can be used to redeem the product from a local pick-up station.

- a warranty token, issued by Apple, which allows the iPhone to be serviced in shops other than Harvey Norman (e.g. Apple Centre).

- A receipt token, issued by Harvey Norman, which allows the product to be returned in 90 days. It's also useful for getting a Tourism Tax Refund if you want to take the phone out of Australia.

If without tokens as the integration anchor, the three different services might be carried out by various means.

### The Shipping Token

Without it, a user might get a tracking number instead of a token, which itself carries no authentication information, so it can't be used to pick up the product unless a pickup code is provided, perhaps in SMS - even more poorly integrated with the process.

With the use of a shipping token, the token status can be remotely updated by the shipping company, even messaging to users to inform an upcoming delivery (if the token is held in a mobile wallet). With a bit of cryptography, it's easy to authorise someone else to pick up a product.

### Warranty Token

Without this token, a user might need the serial number and an online registration process to activate the warranty. She might even need to create an account for that, whose password she will probably soon forget.

With the use of a warranty token, the terms and expiration would be easy to find, as it is token properties. The user can log in to the warranty service website with the token, forgoing an account. The token can be programmed to receive messages like product call back or emergency security updates.

### Receipt Token

Lacking a reliable way to authenticate the purchase, an online purchased product usually cannot be returned to the store but might be returned via online means such as a postback. A token carries the methods for authentication sufficient for the process to be done in store.

Despite such a token not being transferable or authorised, it is still useful for 3rd party integrations.  The Tax office will be satisfied that the receipt can't be faked without collaboration from the seller, and allows a swift and easy tax-refund process. If the phone is purchased for work, the employee can easily reclaim the expense from an employer with the trust implied.

![Purchase with one token, getting three tokens. They can be used to access services, like delivery and repair.](purchase-without-shipment-token.jpeg)

As we can observe by the use of tokens, usually scattered business processes and web experiences can finally be integrated. This ties closely to the other benefit of the blockchain: a frictionless market. In this example:

- When the phone traded is second hand, it would be easy to pass the warranty to the next user through a token transfer, opening the market further.

- Since shipping can be tokenised, it would be easy for the buyer to choose his favourite shipping company without having to supply it with business context (address, product, weight, dates) manually, further opening the market for competition.

This example can be further extended to solve complicated and innovative business cases. Suppose the purchase is not made with fiat currency but with American Express points. The iPhone purchase will be insured for screen damage, and as a result, the transaction will have a 4th insurance token as the output.

When the mobile phone is repaired for screen damage, an invoice is issued concerning the purchase record of the phone to prove it is the same phone purchased with the points, enabling the insurance to be paid on the spot.

Without such tokens, the user will have to submit a billing statement, invoice and evidence of repair in order to submit a claim. Many users will surely miss one of those documents; the claim may take a few days, and still be prone to fraud.

In this insurance case, the blockchain allowed business process innovation that otherwise would require the user to sacrifice convenience, for the mere fact that too many parties are involved and there lacks an integration anchor.

The power of integration is further strengthened by the use of the Internet of Things. Let's imagine a future version of AirBNB, where the bookings are tokenised. A traveller can enter a booked AirBNB house by unlocking the smart-lock with his or her token, and the smart-lock would recognise who the current owner of the booking token is.

If Alice owns a token that represents the right to use a room during a specific time window, or "a booking" in user's terms, then the actions she could perform are:

Check-in - either produce a QR code to verify the booking to the landlord or use an NFC-enabled phone to open a smart-lock.

![AirBnB Token integrates IoT, allowing the token to open a smart-lock.](airbnb.jpeg)

Observing the desirable integration, we can see TBML has to satisfy the following needs:

- Allow token actions to be defined. In the case of a shipping token, there would be a "redeem" action (via a QR code or NFC) and an "authorise" action which would allow someone else to pick up a delivery.

- Allow blockchain functions to be accessed in an action.

- Allow web functions to be accessed in an action

- Allow the token status to be updated, via a web API or signed message (more on that later).

# The design of TBML

## Relate tokens to smart contract and tokens to web services

Early public blockchain projects attempted to implement both token logic and business process into smart contracts. Using an online retail project as an example, such a smart contract would not only process an order but also manages the inventory. The token transaction logic, like under what condition the transaction is valid, is tied with business process, like checking inventory. This method is, naturally, inherited from the way people build websites.

Using an analogy to demonstrate the inappropriate method, suppose an IKEA manager decides to format the furniture sales contract to include information like which aisle a patron should go to fetch the furniture package, would it work in real life? Of course not, the contract would have to be modified too many times to reflect Ikea warehouse management; which aisle has the product has no impact on the validity of the trade.

When these attempts failed to work, developers, in a resolved effort pounding heads against the wall, complained about the performance and privacy issues in current generation blockchains. It is true that the current generation blockchains lack greatly in performance and privacy, but extending them would be the wrong approach to address business process problems. Realising that current Ethereum does not fit to be a business engine, ICO hustlers in 2017 touted the idea of new generations of blockchains with tens of thousands of transactions per seconds. 2018 saw the renewal of such disinformation picturing blockchain as "the new cloud", a superset of AWS' functionalities. The underlying thinking is that blockchain as a new technology must be a faster and stronger version of the previous ones: the Cloud; much akin to the way we imagined the 2000s transportation solution being flying cars, not Uber.

Thanks to its additional security assumptions, Byzantine Fault tolerance blockchains would never outperform AWS's business engines. Furthermore, it's not practical to build a firewall around a blockchain business process. If performance, privacy and security reasons are not persuasive enough, the compelling argument this paper provides lies in the life cycle management: the contractual relationship, reflected by the tokens the user holds, will stay for a long time, while the business process is, ideally, perfected from day to day.

The authors of this paper advocate a method to draw the line between a smart contract and a business process.

1. A smart contract dictates the transaction rules of tokens, not the utility of the tokens.

2. A smart contract and business process are integrated through the tokens.

Going further along the online iPhone purchase example, at the time of purchase, a shipment token is created, representing the user's right to receive the delivery. It does not imply that in the very few seconds the purchase is recorded on the blockchain, an inventory management database selected a warehouse, deducted the iPhone from its inventory count, labelled it with a shipment tracker and returned the tracker to the token. It would be absurd to use blockchain like a cloud platform and outright impossible thanks to the atomic nature of blockchain transactions.

Preferably instead, the online retailer obtained a point of integration - the shipment token, which will allow the warehouse to find the product, label it at its own pace, inform the user that the product is ready to be shipped (the token carries the definition of what communication is allowed to the holder), and send it on its way.

As the business matures and markets become less frictional, two changes happen.

### Change in the business process

The first change is that the online retailer found a better shipment company. In this case, the new shipment company will integrate the same shipment token, sending shipping progress information in place of the old one. The customers can still prove ownership of the shipping with his token, e.g. by using an NFC mobile phone to touch the deliverer's hand-held device.

There is no need to change the smart contract transaction rules. The online retailer can even change the shipping company when the product is first under-delivered without the user changing his token.

This change illustrated that the business process should decouple from the token, instead, integrated through the token.

### Change in the market

Business went on for a while; then, there is an innovation from the blockchain market. Some users bulk-purchased a year's shipping from a delivery company, to enjoy the AmazonPrime-like free shipping privileges without using Amazon[^last-mile-market]. Seeing an opportunity, a credit card company even went so far as to provide such a privilege to the subscribers of their card, which is also represented by a toke.

[^last-mile-market]: The market condition for such an innovation might exist, because only the buyer is most familiar with the last-mile delivery experience. Usually, an online retailer negotiates a higher bulk delivery discount than their buyers could, but they are just a proxy of the buyers' experience. Their interest is not perfectly aligned with the buyers. A buyer driving 30 minutes to pick up a parcel knows that the discount is no match for her time. The delivery company can also optimise the process better than the online retailer, for example, by requesting access to the buyer's calendar, which the online retailer couldn't do safely. Ultimately, more value can be created with the collaboration between buyer and the delivery company.

The online retailer decided to join the game to stay competitive. This time, he would need to modify his smart contract, changing the transaction rule that a shipping token can be accepted at the time of purchase. In such a case, the output of the transaction will not have a shipping token, since one is already provided.[^fungible-shipping-token]

[^fungible-shipping-token]: In practical implementations, bulk-purchased shipping labels, if tokenised, may or may not be used as shipment tokens. Shipping labels can be designed as a semi-fungible token, while the shipment token must be non-fungible, each mapped to a specific parcel. The authors of this paper decided to leave out such implementation detail for clarity.

The online retailer will necessarily modify his business process to expect pick-ups from any delivery company the user purchased shipping tokens from.

This change illustrated that a new transaction rule would result in a change of smart contract.

### Business processes may not change smart contract. Market condition may.

To recap, business process changes should not lead to a smart contract change. An improvement in a free market, in the form of a transaction rule change, should naturally lead to a smart contract change. Blockchain serves to provide a frictionless market, not to optimise business processes.

This vision is made possible through TBML. Without which the clear separation of integration needs and business process needs would be difficult and the result would be not interoperable.

In the first case, TBML described a shipping token to be able to receive messages. In the simplist form, the message is entrusted and rendered to the user interface

We will demonstrate the portion of TBML related to messaging.

    <token>
      <name xml:lang="en">Shipment</name>
      <name xml:lang="zh">貨單</name>
      <name xml:lang="es">Despacho</name>
      [...]
      <states>
         <state name="initialised"/>
         <state name="dispathced"/>
	 <state name="collectable"/>
	 <state name="used"/>
	 <state name="expired"/>
	 <state name="returned"/>
      </states>
      <messages-acl>
         <trust signed="issuer">
	     <permission>
	         <display type="history"/>
		 <display type="notification"/>
             </permission>
             <condition state="initialised"/>
	 </trust>
	 <trust certified="issuer">
	     <permission>
	         <display type="history"/>
		 <display type="notification"/>
             </permission>
             <condition state="dispatched"/>
	 </trust>
	 [...]


The section between `<states>...</states>` gives a list of states which is the basis of defining messages the token holder is allowed to receive.

The first `<trust>...</trust>` structure causes the user agent to accept and display any signed messages from the token issuer, in this case the online retailer, as notification and an entry in message history, when the token's state is initialised.

The second `<trust>...</trust>` structure causes the user agent to accept and display any signed messages, whose signing verification key is certified by the issuer of the token, as notification and as an entry in message history, when the token's state is "dispatched". This effectively allows any entity the token issuer explicitly trust to issue a message at "dispatched" state.

When the online retailer changes his delivery company, the retailer could issue a certificate on the public key of the new delivery company, thereby authorising them to send messages to the token holders (buyers) to update them the delivery status, yet restricting the messages to only certain stages of business process.

This code snipet shows that by giving such flexibility TBML connected to a new business process without requiring change in the smart contract or affecting user experience. It also allowed communication to the token holder without sending messages through smart contracts.

The method of actual communication is left open to be implemented by other layers of blockchain technology like a message queue or even a distributed message queue.

It's worth noting that messaging is not the only part connected to the business process. We will explain a broader scope of integration in the "Web integration" chapter.

It's also possible to write TBML in such a way that only messages from the online retailer is trusted and displayed, therefore, any new delivery company must send their delivery status message to the online retailer's systems to be forwarded to the buyer. There are availability and privacy reasons why this may not be a good idea. For example, a delivery company should be able to operate when the online retailer is offline; the user might send the door entrance passcode to the delivery company which the online retailer should not learn.

##  Types of tokens

Since 2018, Ethereum community has roughly categorised tokens as fungible tokens and non-fungible tokens.

Fungible tokens refer to the currency-like token with a balance, typically implemented in ERC20, although in practice currency functions like pre-authorisation and setting up of state channel requires richer functions than typical ERC20.

Non-fungible tokens refer to crypto-kittens and typically have one unit per token.

The categorisation isn't capturing the full spectrum of the tokens we could and may overlap in some cases. Taking the 1% per cent property token we demonstrated earlier as an example, each of such token is fungible with another issued by the same issuer for the same property. Maybe with the exception of the Chinese community which usually overvalue the token with a sequence number of 88, but if we allow any percentage number to be tokenised, say, allowing one to purchase 0.88%, then the sequence number will be refactored out of the way too, making each partial ownership token of the same property strictly fungible. However, apparently, a percentage of ownership of property A  and a percentage of ownership of property B are not fungible with each other.

This paper re-introduces the concept of attestations - it has been there for decades but wasn't fully utilized. From there, this paper categorises tokens as "blockchain token" and "attestation". The former type includes both fungible and non-fungible tokens. The latter type "attestation" will be explained here.

## Attestations

Attestation is a cryptographically signed message testifying something on a subject - a person, a token, or another attestation. Since it is specific to that subject being attested, it is not transferrable on its own on the blockchain.

In our previous car ownership token example, the car ownership token would be a blockchain token, where the typical buy, sell and transfer rules can apply. The insurance token on it, however, is not a blockchain token. If the insurance is compulsory, it is an attestation on that car, therefore cannot be transferred on its own. If the insurance is comprehensive, it is an attestation on the car and the driver, and cannot be seamlessly transferred even if the car is transferred.

If an attestation is not transferrable, then why does it have to be on the blockchain? The answer is it doesn't.

Take a person identity attestation for example. Unless it is used for a blockchain transaction or revoked for some reason, there is no reason that it should have any trace on blockchains like public Ethereum. They are, still, an item in the user's wallet, since they might need to be prolonged, re-attested due to change of a person's identity or used to login to services the same way Estonian e-residency attestation can be used to login to web services.

An attestation can affect transactions. For example, a VIP member can enjoy a 10% discount on services - such business rule would require a VIP member attestation to be used for the cryptocurrency transaction for purchasing the service. An attestation of Holden Capped Car services, which is valid for 5 years, allow the car to be serviced with the bill capped to a certain amount before its expiry.

Sometimes, an attestation dictates what transactions can happen.

As a subscriber of *The Economist*, I commit to paying for each issue as they are published. This is done by me sending a pre-authorisation to withdraw a subscription fee bi-weekly from my Ethereum account. Such a pre-authorisation would be an attestation in the wallet of The Economist, which provides a "charge" action that The Economist could use bi-weekly.

For privacy reasons, or to combat linkability (the subject of an attestation being identified by the public use of such an attestation), the attestation used in transactions is of a different form than the one that lies in a user's wallet. The authors of this paper addressed this issue in another paper [cite].

In all of the previous examples, attestations only leave traces when a transaction needs it. There are cases when attestations leave traces on the blockchain when they are created, or revoked.

To explain the use case where the *issuing* of attestation has to happen on the blockchain or with blockchain trace, take the aeroplane engine for example, with a substantial resale value, the repair facts of this engine, in the form of attestations, affects valuation significantly. Such attestations are in the seller's wallet, but an aeroplane service provider must add a hash of such an attestation each time the engine undergoes maintenance. The buyers would not purchase if they are not presented with these attestations that match the blockchain records.

To explain the use case when the *revocation* of an attestation has to happen on the blockchain, let's consider an attestation called FIFA ticket.  Issued by the event's organiser, it attests the owner's right to enter the venue, usually after the user has paid or was gifted the ticket. Let's assume 90% of the tickets are purchased with non-crypto currency, therefore these tickets would not have a trace on the blockchain. However, if a ticket's owner decides to sell his tickets on the blockchain following the corresponding smart contract rules, the ticket has to be used as the input of such a transaction and considered consumed, while a blockchain token representing the same entitlement would be created and traded. The writes of this paper organised a FIFA ticket experiment in mid-2018 to test the concepts, and internally we call such an attestation "a spawnable" as its use spawns a blockchain token. The detail of that experiment can be found in another paper [cite].

# The components of TBML

## Actions

We seperate the rendering portion of TBML and the actionable portion. Action refer the things you can do with a token. There are generally either:

- Use the token to access to a web service
- Use the token to control IOT devices
- Transacte with the token.

All examples of these actions can be found in the car example in the first chapter. For example:

Car token's actions:

Unlock
:   The token has enough credential information to answer a challenge-response from a car in order to unlock it while offline.

Authorise
:   The user can also authorise another person to use it, sending an authorisation (which is an attestation - see Attestation chapter) as easy as sending an instant message.

Lend
:   The difference between authorising and lending is the latter also authorises the borrower to use Holden Capped Service and to open the garage gate.

Holden Capped Service token's actions

Book a service
:   This token allows the user to login to any holden service center and book an appointment.

Check-in
:   He further uses this token to enter the service station (swipe his mobile to enter the sliding gate).

Pay
:   By including the Holden Capped Service token in a transaction, the service cost is capped, either on the web through pre-pay or on the POS.

Not all actions are provided by the token. Typically:

Transfer
:   Provided by a generic token's TBML. You can imagine for example the TBML file of ERC721 allows any conforming tokens to be transferred, and the car token might be one of them. In reality it can hardly be the case because car token's transaction rules usually require attestations, such as the buyer is of the legal age to conduct such a transaction, but even in such cases, the rule might be supplied by a TBML regulating the car trade.

Auction
:   Provided by an auction market. When the user accesses an auction market, using the same mechanism that allows a token to login to a website, the user's agent (wallet) would show a list of tokens that can enjoy the auction service. If the user trusts the auction market, she can then add its action to all of the supported tokens.

List for sharing
:   A startup company, let's call it CarNextDoor, offers to manage the process so the car owners can safely list the car for sharing and automatically gets income. Once listed, the car owner will obtain a listing token and has to book his use of his own car through it. In exchange, when he is not using it, the car goes out and earn money for him. Naturally, the action is provided by CarNextDoor, not by Holden.

## Magic links

Magic links are simply a shortcut to an action on a specific asset. It's usually sent to the owner of the asset. It comes with required attestations for a transaction (e.g. an atomic swap).


## Attestations

Attestations are like Tokens except that they are not transferable, in the case that a smart contract allows them to be transferred, the original attestation is render invalid after the transfer.  This makes it possible for things like friendship to be defined in a way similar to the token, and therefore, we may as well call such attestations "tokens". A token of friendship would be a signed message from someone, recognising someone else as a friend, and it would be an asset in TBML terminology. Apparently a token of friendship from Michael Jackson can be of high value, especially since he cannot produce any more of these tokens, but even a humble token like "Friend of Weiwu" has some value. It, for example, allows a friend of Weiwu to sign a delivery recipt for him, or allows such a friend to get a mate-rate for signing up in the same dojo Weiwu practises in. There is even a neat trick, which, by using secret sharing protocols, having Weiwu's friendship token allows one to learn common friends shared with Weiwu. Notice that this definition does not require the asset to be a blockchain token, nor that it even exists on the blockchain. More on that in the latter chapter "attestation".

Assets and attestations (tokens in general) can have financial value and utility value.

## Assets

In TBML terminology, an asset is something that can be owned and has value. This is a broad definition and doesn't require, like the financial assets, that an asset produces a return, or is anticipated to.

Examples of assets: crypto kitties, FIFA tickets, right to a bottle of wine, 1% ownership of a house, a piece of armour in a video game or dice in a video game.

Examples of attestations: crypto-kitten vouchers, FIFA ticket redeem coupons, American Express Centurion status, Friendship Tokens (a signed message from Michael Jackson saying that Victor Zhang is a friend) or proof of identity.


# Join the game

The work to define TBML as a specification is a work in progress. We aim to produce a yellow paper of the key methods and considerations and extend it from there. More methods of collaborations are being put to work as you read this draft. For now, the contact points are:

weiwu.zhang@alphawallet.com
james.sangalli@alphawallet.com
victor.zhang@alphawallet.com