# 白皮书

## 作者注
## Author's note
在2017-2018区块链发生了非常引人注目的投机行为把我们的注意集中到了crypto tokens上。当我们交易时，我们甚至忘记了它们真正的用途; 就像房地产泡沫，一味的把房屋当作投机资产，而忘记了这是居住的地方。
The remarkable blockchain speculations that took place in 2017 - 2018 brought everyone's attention to crypto tokens. As we bought and sold them, we forgot their intended purpose was to be used; this is analogous to the housing bubble in which people forgot that houses were not merely speculative assets but rather a place to live.

为了让区块链提供实际的用途，我们必须了解它对世界经济和互联网的作用。这篇文章的作者是对金融机构和初创公司进行了长期的学习和探索的技术专家。凭借这些经验，我们逐步意识到区块链有**两个主要的功能**:
To provide a practical use of the blockchain, we must understand its utility to the world economy and the internet. The authors of this paper are technical experts who went through years of study and exploration into its applications both via financial institutions and startups. With this experience, we came to realise that the blockchain has **two primary functions**：

- 提供无摩擦市场(译者注:”无摩擦市场(Frictionless Capital Markets)又称完全资本市场是金融经济学家所假想出来的一种资本市场环境，旨在简化或深化理论分析，促进理论的发展。完全资本市场，是指在这个资本市场中，任何投资人都无法拥有通过自身交易行为而影响或操纵市场上的证券价格的力量；投资者可以平等地免费获得影响股票价格的全部信息；证券发行不存在发行成本、交易费用等)

- 集成网络

- providing a frictionless market; and

- integrating the web

尽管2017-2018年发生了很多蠢事，但是这对于token获得早期的关注并不是坏事。作者即将详细阐述的token，将是两个主要功能的推动者。我们将定义并实现“Tokenisation”的技术。
Despite the great folly in 2017-2018, it is not a bad thing to initially focus on tokens. Tokens, as the authors will elaborate, are the enabler of the two primary functions. We define the technique to make it happen in "Tokenisation".

区块链行业共同的努力主要是集中在丰富技术能力上。这篇文章将集中在Tokenisation，并且介绍一个称作Tokenscript(token行为标记语言)的标准化工作，它将使区块链技术具备完整的技术栈，为经济和互联网提供实用性。
Previous efforts in this industry primarily focused on enriching the capacity of the technology. This paper will focus on tokenisation and introduce a standardisation effort known as Tokenscript (Token Behaviour Markup Language) which will make the blockchain technical stack complete, providing utility for the economy and the internet.

等tokenscript.org搭建好时，欢迎加入我们的工作。指导开发者为其tokens和dapps使用Tokenscript的黄皮书，将花费数月时间。但是，我们一直保持过程开放。现在参与可避免我们制定的语言规范草案没有考虑到你的token模型。
Please join our work at tokenscript.org - when it is set-up of course. A Yellow Paper to guide implementors to use Tokenscript for their tokens and dapps will take months to make. However, we keep the process open. Participate now to avoid the draft language specification being made without consideration your token model.


## Abstract
## 摘要

我们认识到区块链技术的真正应用是提供完全市场和集成网络方面的实用性。这是通过Tokenisation完成的。 被Tokenized的股权可以在市场上交易并集成到系统中，形成无摩擦的市场并允许自由集成。
We recognise the blockchain technology's utility in providing a frictionless market and integrating the web. This is done through tokenization. Tokenized rights can be traded on the market and integrated across systems, forming a frictionless market and allowing free integration.

如今，访问、呈现和交易的token的方式分散在Dapps和智能合约中。 如果关于一个token的所有信息都在dapp中，那么dapp必须参与该token的市场和所有集成，这重现了数据的互操作性，安全性和可用性 - 同样的问题在区块链发明之前就已出现，并阻碍了tokenisation。
Today, the way tokens are accessed, rendered and transacted are scattered across Dapps and Smart Contracts. If all knowledge about a token is in a dapp, the dapp has to participate in the marketization and all integrations of that token, recreating data interoperability, security and availability barrier - exactly the same set of issues that prevented tokenisation before blockchain was invented.exactly the same set of issues that prevented tokenisation before blockchain was invented.

Tokenscript是一种抽象出token信息，访问模式和UI呈现的方法，以便它们可以有效地进行市场化并用于集成。
Tokenscript is a method to abstract out the token information, access methods and UI rendering so that they can be efficiently marketized and used for integration.


## 加入我们

请加入我们在xxx的工作。 一份指导实现者使用Tokenscript作为其tokens和dapps的黄皮书将花费数月时间来制作，但中间的工作和进度会一直在网上公开。现在参与以避免制定的语言规范草案没有考虑到您的token模型。

## Join the game
Please join our work at xxx. A Yellow Paper to guide implementors to use Tokenscript for their tokens and dapps will take months to make, but a work in progress is always available online. Participate now to avoid the draft language specification being made without consideration your token model.



# 介绍：区块链*能做什么*?
# Introduction: What does blockchain *do*?

区块链技术具有**两个主要功能**，并服务于未来的经济和互联网的重要目的：
 - 提供无摩擦市场(译者注:”完全资本市场又称无摩擦资本市场(Frictionless Capital Markets)是金融经济学家所假想出来的一种资本市场环境，旨在简化或深化理论分析，促进理论的发展。完全资本市场，是指在这个资本市场中，任何投资人都无法拥有通过自身交易行为而影响或操纵市场上的证券价格的力量；投资者可以平等地免费获得影响股票价格的全部信息；证券发行不存在发行成本、交易费用等)
 - 集成网络。
Blockchain technology has **two primary functions** that serve essential purposes for the future economy and the future Internet:
- providing a frictionless market; and
- integrating the web.

本文将从愿景开始，然后解释设计以及区块链上层需求架构背后的原因。随后我们将解释Tokenscript，这是一个关键的缺失层，并回顾其设计原则以及我们是如何构建的。
This paper will address the vision of where we can be and follow up with the design and reasoning behind the architecture needed on top of the blockchain. We will then explain Tokenscript which is a critical missing layer and go over its design principles and how we are building it.


## 区块链提供了一个无摩擦市场
## Blockchain provides a frictionless market

上世纪80年代的“回到未来”描绘了一个拥有悬浮滑板和飞行汽车的强大机械世界。但是他们并没发生。正如彼得·泰尔曾经著名的哀叹，“我们曾经承诺飞行汽车，结果只得到140字符（注：隐喻Twitter）。但是我们所处时代的技术进步依旧超出了80年代科幻电影的想象，不是通过更强大的机器，而是有效使用互联网。
The 80s' "Back to the Future" featured a world of powerful machines filled with hovering boards and flying cars. It didn't happen. As Peter Thiel once famously lamented, "we were promised flying cars; instead, we got 140 characters". The technological advancement of our time is beyond the imagination of the 80s science fiction movies, albeit not through more powerful machinery, but efficient use of the Internet.

共享行程彻底改变了我们的日常生活，airbnb改变了我们旅行的方式。这个是一个全新的、较少摩擦的市场。Airbnb的运营成本更低，更易于使用，并且拥有精细的运营部门。
Ride-sharing transformed the way people get around, and AirBNB changed the way we travel. These are the new, less frictional markets. They incur less cost to operate, are more accessible and have finer operational units.

然而，尽管已经进行了Web 2.0革命，大多数市场仍然以高成本运营。例如，股票市场由于依靠对于规章制度的信任来运作，开销非常大，它只适合价值数百万美元的商业。
However, despite this web 2.0 revolution, the majority of markets still operate with high costs. The stock market, for example, has so much overhead that it is only justifiable for multi-million dollar businesses which rely on the trust of rules and regulations to operate.

使用区块链，任何Tokenisation的资产都可以随时进行交易，只要遵循规则，没有中间商或中间人，给我们提供最高的市场效率-完全市场。除了不依赖中间商之外，在Tokenisation的市场模型中，买方和卖方不在需要”进入“市场。相反，token*总是在市场上*[^market-model]，这样的模式当然比中间商更好。
With blockchain, any tokenised asset can be transacted any time, as long as it follows the rules, without middlemen or intermediary, gives us maximum market efficiency - the frictionless market. On top of the benefits of not relying on an intermediary, in a tokenised market model, the buyers and sellers do not need to "enter" the market; instead, tokens are *always on the market*[^market-model], making such a model better than intermediaries.

[^market-model]: 传统的中介操作市场模式，交易分为两个阶段：进入市场，达成交易。 区块链可以将其简化为协议; 因此，区块链token资产可以被视为始终在市场上。

[^market-model]: With the traditional intermediary-operated market model, a trade is made in two stages: entering the market, making a deal. Blockchain can simplify that into a protocol; therefore the blockchain token assets can be considered always on the market.

### 我们能够通过Tokenisation创造完全市场吗？
### Can we create a frictionless market through tokenisation?

我们是否可以tokenise房产，举个例子，1％的房产，以便地产市场能够比传统的长达一个月的房地产购买 - 销售周期更快地做出反应？ 
Can we tokenise, for example, 1% of a property, so that the property market can react faster than the typical month-long property purchase-sales cycle?

我们是否可以tokenise电力，让电力用户能够从更精细的资源使用安排中受益，让家庭从收集太阳能的剩余中受益。
Can we tokenise electricity, allowing power users to benefit from finer scheduling of the use of resources, and households to benefit from collecting surplus sun energy?

我们是否可以tokenise Airbnb的预订，以便房屋主人可以从市场上获得有保证的现金流，而市场分析者可以通过预测旅行需求获利。
Can we tokenise AirBNB bookings, so that hosts can purchase a guaranteed cash flow from the market, while speculators profit from predicting the travel needs?

我们是否能够tokenise国际贸易的风险和回报，让没有足够信用的小型进口商和出口商，能够在国际市场上参与竞争，也许能够超过像Airbnb这样的传统供应商。
Can we tokenise the risk and reward of international trades, so that small importers and exports, not significant enough to obtain letters of credit, can compete in global markets and perhaps eventually outcompete the traditional model like AirBNB outcompetes hotels?

我们是否可以创建一个依赖于加密证据的保险token，以便保险公司可以从其定价中删除提供欺诈性文件所产生的费用？ 我们可以完全去中心化保险公司吗？
Can we create an insurance token that depends on cryptographic proofs, so that the insurer can remove from their pricing, the costs incurred by fraudulent documents? Can we decentralise the insurers altogether?

区块链可以提供基础层来实现这些。虽然区块链的可扩展性和隐私性有待提高，但一个有效的，无摩擦的市场也依赖于有效的方法来定义如何使用和交易token - 这是我们Tokenscript工作的重点。
Blockchain can provide the foundational layer to achieve these. While blockchain scalability and privacy will improve, a working, frictionless market also depends on quality methods to define how tokens should be used and transacted - the focus of our work on Tokenscript.

token具有不同的属性。token是否会过期？ AirBNB预订token当然会，但1％的房产token可能不会。token所有者是否应收到有关特定事件的通知？电力token肯定需要，因为电力是不断变化的。token是否流通？
Tokens have different properties. Do tokens expire? AirBNB booking tokens certainly do, but 1% ownership of property tokens probably don't. Should the token owner receive a notification on a specific event? Power tokens certainly need that, for the change in the power supply is dynamic. Is a token stream-able?

它如何在用户的手机上显示，用户如何使用？
How does it look on the user's mobile, and how is it called in a users language?

如果买家想要从卖家那里采购被Tokenisation的乡村庄园，他们如何进行有效的沟通？
If a buyer wants to purchase a tokenised country estate from a seller, how do they establish a trusted method of communication?

如果token允许用户在线执行特定操作，用户如何使用token登录特定web服务？
If a token entitles the user to do specific actions online, how can the user login to the web services with that token?

所以我们很容易知道需要一个定义token的框架，让他们适应不同的交易，上市以及评级。我们确实在2017-2018期间拥有数百种token，但它们统一是类似货币的 ERC20 token，填补了市场的付款方面的空白[^payment]。但几乎没有让token在代表*商品和服务*上做任何努力，这是一个可交付的市场运作的基本需求。
It's easy to see the need for a framework defining tokens and making them interoperable with different methods of trading, listing and rating. We did end up having hundreds of tokens in 2017-2018, but they are uniformly the currency-like, ERC20 tokens, filling up the payment side of the market[^payment]. There is nearly zero effort devoted to making tokens represent *goods and services* - the deliverable side of market and a fundamental need for a market to work.


[^payment]：在后面的章节中，我们将token分类为付款token和可交付token。 带有*支付代币*标志的ERC20代币只能用tokens填充市场的一面，因此无法提升市场。
[^payment]: In the later chapters we will categorise tokens as payment tokens and deliverable tokens. ERC20 tokens bearing the hallmarks of *payment tokens* only filles one side of market with tokens, therefore can't lift a market.

举个例子，在2017年的投机泡沫期间，电力token的ICO不需要提供关于如何使用token的任何解释。 所有投机者仅仅只知道它们代表着“在未来的电力化世界中占有一席之地”。 只要token可以满足投资者的想象力，这对ICO来说就足够了。 因此，除了ERC20接口之外，他们没有任何其他功能。 对于这样的投机电力token来说，它不依赖任何证据，如实际发电量的证明，电力提供的来源在哪，以及可用的时间长短。
During the speculative bubble of 2017, a power token ICO does not need to provide any explanation of how the tokens can be used. All speculators need to know is that they represent a "stake in the future world of tokenised electricity". As long as the token can inspire investors with imagination, it's good enough for an ICO. There is, no more functionality needed other than an ERC20 interface. Such a speculative token doesn't depend on attestations - the proof of actual power production - nor does it need properties like where the energy is provided or for how long it is available.

现在疯狂已经结束，是时候提出技术框架来使市场发挥作用。
Now that the madness is over, it's time to present the technical framework to make the market work.

## 区块链集成网络
## Blockchain integrates the web

Tim Berners-Lee和万维网的创新者主要以公共图书馆模型和计算机人机交互模型为网络建模。
Tim Berners-Lee and the innovators of the world wide web modelled the web primarily on a public library model and computer-human interaction model.

在图书馆模型中，信息可以免费获得，并通过URI进行索引和交叉引用。 它的化身，既URL就是数据所在的位置，它对你能够访问的地方没有限制。
In the library model, information is freely available, indexed and cross-referenced by a URI. Its incarnation, the URL, is where the data is, and there is no restriction on where you can go.

在人机交互模型中，两个玩家进行对话，人问，机器回答。虽然计算机知识有限，但它可以帮助用户访问正确的计算机。
In the computer-human interaction model, two players are having a conversation - the human asks and the machine answers. A computer has limited knowledge, but it can help the user to reach the right computer.

因此，网络被构建为一个巨大的图书馆，每本书都是一台可以与之交谈的计算机。 这可能是Facebook获得同名灵感的地方 - 一个网站就是一本书。
Therefore the web was built as a giant library where each book is a computer with whom one can have a conversation. The analogy probably is where Facebook got its namesake inspiration - a website is a book after all.

正是这种设计造成了许多现代的不便。用户有一天会在她的月结账单上收到一封电子邮件，但她无法识别出一些条目，比如"亚马逊"，这是一个鞋子的订单吗？她必须复制订单号并在亚马逊中查找。在另一种情况下，同一个用户可能会在预订两张歌剧门票时暂停，切换到她的常旅客应用程序，复制该号码并将其粘贴到订单中以收集积分。 她需要会在一开始就安装那个常旅客应用程序。
This design has caused a lot of modern inconveniences. A user would one day receive an email on her monthly statement, yet she couldn't recognise a few entries on them. It says "Amazon". Was it about ordering a pair of shoes? She has to copy the order number and look it up in Amazon. In another occasion, the same user might pause as she books two tickets for an opera, switch to her frequent flyer app, copy that number over and paste it into the order to collect the points. She might struggle a bit installing that frequent flyer app at the outset.

我们为什么要做这么多的复制和粘贴，这些明明机器就能做好的事情？这是因为网络就像一个巨大的图书馆，我们就像读者一样在袖子上面记录索引号。他们并没有设计得像一个私人助理。[^pda]
Why are we doing so much copy and pasting when machines are exceptionally good at doing this? It's because the web is like a giant library by design, and we are like readers keeping notes of the index numbers under our sleeves. It's not, as we would hope to have, designed like a personal assistant..[^pda]

[^pda]：令人惊讶的是，即使是为满足创建私人助理的角色而发明的技术仍然失败了，就像智能手机。原因同样如此：单靠客户端的努力无法集成本来就非集成的网络，基础设施必须支持集成。智能手机的模型类似于拨号互联网连接，每个应用程序代表一个网站。 在进入对话之前，用户仍然需要找出要与之通话的计算机（app），并且在他交换应用程序时仍然可以复制信息。 例如，要求您的智能手机通过在线银行的app汇总你所有的资金是不可能的。
[^smart-phone]: Surprisingly, even the technology that was created to fill the role of a personal assistant, the Smart Phone, still failed, for the same reason: the efforts from client side alone can't integrate a Web that is not designed to integrate. The infrastructure has to support integration. A smartphone is modelled like a dial-up Internet connection, with each app representing a website. The users still need to figure out which computer (app) to talk to before entering the conversation, and still copies information around as he swaps apps around. It's not possible, for example, to ask your smartphone to sum up all the money one may access by his online banking apps.

很容易就能看出造成不便的原因：不同的网络之间没有更好的集成。继续举几个不好的例子；

It's easy to see the cause of the inconvenience; the web is poorly integrated. The bad examples go on and on:

- 当用户在网站上结账时，她不确定她的卡上是否有足够的余额，因为银行未与购物系统集成。
- When a user checks out on the web, she isn't sure if she has enough balance on her card, since the bank is not integrated with the shopping system.
- 当患者订购服务时，在账单结算之前，她无法看到保险可以支付多少费用，也不知道她是否达到年度上限，因为诊所没有与保险公司集成。
- When a patient orders a service, she can't see how much the insurance can cover until the bill settles, nor can she know whether she has reached the annual cap since the clinic is not integrated with the health insurance company.

集成网络的答案需要一些不在网络蓝图中的模块：身份验证，所有权，价值转移和交易。
The answer to integrating the web requires a few building blocks that weren't in the Web's blueprint: authentication, ownership, transfer of value and trading.

Web没有内置的身份验证机制。 像“使用Facebook登录”这样的附加组件仅仅试图通过受信任的第三方提供身份验证[^tls]，尽管存在隐私和可用性问题，但它仅适用于帐户身份验证，而不适用于业务逻辑。
The web doesn't have a built-in authentication mechanism[^tls]. The add-on "Sign in with Facebook" merely tried to provide authentication through a trusted 3rd party, which, despite privacy and availability concerns, is only good for account authentication and not for integration.

[^tls]：尽管在TLS中对客户端/服务器证书做出了巨大努力，但这些身份验证方法不适用于过程，仅适用于站点。这其实是一个委托模型。想象一下，买方不检查所有权契约是否真实，但只检查卖方的名称是否与契约上的名称相匹配。 这就是TLS中使用的委托模型。 事实上，TLS无法保证网站上的任何内容是真实的，只有网站是真实的.Facebook使用TLS，但人们在上面投放了很多假新闻。 毫无疑问，这里的信任单位不足以让网络提供集成体验。
[^tls]: Despite the excellent efforts on client/server certificates in TLS, these authentication methods are not for processes, but only for sites. It's a delegation model. Imagine a buyer not checking if a title deed is real, but only checks if the seller's name matches the one on the deed. That would be the delegation model used in TLS. In this model, TLS can't guarantee anything on the website is real; only that the website itself is. Facebook uses TLS, but people put much fake news on it. The unit of trust here is undoubtedly not granular enough for the web to deliver an integrated experience.

### “帐户身份验证”不能取代Web集成
### "Account authentication" is not a substitute for web integration.

例如，简单的业务逻辑：“汽车的所有者可以检查其服务历史记录”，这并不需要帐户。 如果您强行使用“帐户身份验证”模型，就会出现很糟糕的情况：
For example, the simple business logic: "the owner of a car can check its service history", doesn't require an account. If you force the "Account authentication" model, bad things happen:

 - 当汽车售出时，新车主现在需要在服务网站上创建一个新帐户，并且加密它，用来证明自己的所有权。这是繁重且不可靠的。
- When the car is sold, the new car owner would now need to create a new account at the service website and secure it with the proof of ownership to the car. This is onerous and unreliable.

 - 当车辆改装车间或保险公司等第三方需要访问维修历史记录时，没有简单的方法可以在不泄露帐户的情况下对其进行授权。这是不灵活的。
- When a 3rd party like a Vehicle Modification workshop or an insurer needs to access the repair history, there is no easy way to authorise them without giving away the account. This is inflexible.

很容易在医疗保健、零售和网络上几乎其他所有业务中找到更多此类示例。今天，我们不断添加越来越多的帐户来满足这种集成需求。这就像是你手里有一把锤子，看什么都是钉子。以下章节将演示通过token集成而非帐户是一个可靠的解决方案。

Such integration needs, poorly addressed by adding accounts, are easily found in healthcare, retail and almost every web-based business. Today, we are still adding more and more accounts to address the growing integration needs. It's a case of hammering every problem down as if it is a nail. The following chapters will demonstrate that integration through token, not account, is the solution.

同样，网络没有内置的所有权，价值转移和交易机制。
Similarly, the web doesn't have a built-in mechanism for ownership, transfer of value and trading.

来看看汽车故事的未来发展，汽车销售商需要在网站上发布汽车信息，在过程中创建另一个帐户。 买方不能点击“购买”并一次性获得所有权证明，强制保险，未使用的服务配额等，并进行付款处理。 所有这些操作都必须使用易于篡改的纸张样张和表格单独完成。 该过程从Web开始，在其他地方结束。
Taking the car story further, a car seller would need to post the car information on a website, creating yet another account on the way. The buyer cannot click "buy" and acquire the ownership proof, compulsory insurance, unused service quota and so like in one go, and have payment processed. All these actions have to be done separately, using easily-tampered paper proofs and forms. The process starts at the web and ends somewhere else.
相反，同样的过程在区块链上是自动的，防伪的[^attestations]和原子的[^atomic]。
In contrast, the same process on blockchain would be automatic, fraud-proof[^attestations] and atomic[^atomic].

[^attestations]：提供加密签名的证明作为交易条件的方法将在后面的“证明”章节中讨论。
[^attestations]: the method to provide cryptographically signed attestations as a condition for a transaction is discussed later in the "Attestation" chapter.

[^atomic]：在区块链术语中，原子交易可以发生或者不发生。 如果定义明确，买方不可能成功支付汽车而没有获得所有权token，或者只是转让了汽车的所有权而没有强制性保险。
[^atomic]: In blockchain terms, an atomic transaction either happens or not. If well defined, it's not impossible for a buyer to have successfully paid for a car yet not getting the ownership token, or only have transferred the car's ownership but not the compulsory insurance on it.

网络的这些缺失特征是区块链众所周知的功能。 这对完美契合夫妇的虚拟婚礼需要虚拟交换token，或者本文称之为“tokenisation”。
These missing features of the web are the well-known functions of the blockchain. The virtual wedding of this perfect fit couple requires a virtual exchange of tokens, or what this paper called "tokenisation".

token无缝地跨越系统，承载其交易规则和用户界面以及业务环境。
Tokens seamlessly go across systems, carries their trading rules and user interfaces and business context.

## 例子：汽车所有权token
## Example: Car Ownership Token

我们将概括这两个概念：通过token资产的无摩擦市场; 通过使用token作为Web服务的集成点来集成Web。 我们将演示一个包含这两个概念的示例：汽车token。

We will comine the two concepts: frictionless market, achieved by tokenising assets; integrate the web, by using token as integration point for web services. We will demonstrate an example that encompasses both concepts: car token.

一方面，汽车是一种被Tokenisation的资产，可以通过区块链来购买，出售，转让，拍卖，合作和投保。
On the one hand, a car is a tokenised asset, that can be bought, sold, transferred, auctioned, collaborated and insured, all enabled by blockchain.

另一方面，汽车也有实用性。 汽车的所有权token可以将区块链钱包转换为汽车钥匙，其他功能如图形化表示汽车的当前位置。 授权某人访问您的汽车或租用它以获取利润，可以通过签署区块链交易或证明无缝完成，而无需传递车钥匙。
On the other hand, a car also has utility. A car's ownership token can convert a blockchain wallet into a car key, with additional functions like graphically representing the car's current location. Authorising someone to access your car, or renting it for profit, would be seamlessly done by signing blockchain transactions or attestations, without passing car keys around.

以下汽车token的屏幕截图代表了tokenisation的最后阶段。
The following screenshot of a car token represents the final stage of tokenisation.

![汽车token。 四个token：Rego，封顶保养，保险和购买，要么是依赖或者与汽车所有权token有关。](img/car-token.jpeg)
![A car token. Four tokens: Rego, Capped Service, Insurance and Purchase, either depeneds or relates to the car ownership token.](img/car-token.jpeg)

咋一看，它只是一个便捷的能够做关于汽车所有事情的门户网站，包括市场功能和实用程序。然而传统的网络模型是不可行的。
At first glance, it is just a handy portal to do everything about the car, including market functions and utility. However, it's not possible with the traditional web model.

在web2.0模型中，你只能自己处理每个元素。要注册汽车，有一个单独的过程，需要创建一个道路与海洋服务处的账户，并且在没有密码学的帮助下证明所有权。当您想为汽车提供保险时，您必须创建另一个帐户并手动提供其注册到该新服务的证明。（如果你发现不需要这样做，这部分无法支付的保险费用仅仅是隐藏起来了，将会由市场来承担）同样，如果您想让汽车能通过优步或基于小时的汽车租赁来参与分享经济，那么显然，结算付款和保险成本的工作会给市场带来摩擦。
In the web 2.0 model, you are restricted to handling every element on its own. To register the car, there is a separate process which involves creating an account with the Road and Maritime Services and proving ownership manually without the aid of cryptography. When you want to provide insurance to the car, you have to create another account and manually offer proof of its registration to that new service. (If you find not needing to do so, the cost of unpayable insurance merely is hidden and borne by the market.) Likewise, if you want to make the car available to share economy through Uber or hour-based car rental, the work of proving and settling payments and insurance cost adds friction to the market.

现在让我们在web3的世界中构想这一点，这些元素能够被tokenised。供应商（在这个例子里面是holden）向新的拥有者提供所有权token，在购买时转移给所有权者的token又用于获取注册token。内置的物联网允许汽车通过token来证明所有权。
Now let's reimagine this in the web3 world whereby such elements can be tokenised. Vendor (in this case Holden) provides an ownership token to the new owner which can be used to operate the car. The token, transferred to the owner at the time of purchase, is in turn used to acquire the registration token. An inbuilt IoT device allows the car to be operated with proof of ownership via a token.

希望购买保险的所有者只需提供所有权证明和注册token即可满足保险公司的要求。通过将token与其要求相匹配来自动满足保险公司标准，并且一旦经过验证，保险公司可以向所有者发送保险token以换取用户付款。 保险token具有自己的功能和服务。
The owner, wishing to purchase insurance, only needs to provide the proof of ownership and registration token to be qualified to fulfil the requirements with the insurance company. The insurance companies standards are met automatically by matching the tokens to their requirements and once validated, the insurance company can send the owner an insurance token in exchange for payment. The insurance token carries its own functions and services.

如果车主希望成为优步司机，她可以通过提供所有权证明，保险轻松证明她的车辆足够好，并且通过token注册。 然后优步自动向她提供一个Ubertoken，根据所有者的需要，可以用来让自己成为Uber司机或允许第三方司机这样做。 这些流程都不需要手动验证或帐户创建。
If the owner would like to become an Uber driver, she can easily prove her vehicle is good enough by providing proof of ownership, insurance and registration with her tokens. Uber then automatically provides her with an Uber token which, depends on the owner's need, can be used to get himself started as an Uber driver or allow a 3rd party driver to do so. None of these processes requires manual verification or account creation.

更进一步，车主可以跳过优步，直接将车租给陌生人。 她不想让她的汽车被一些随意的陌生人破坏。她可以将她的租车者限制在那些拥有“优良司机”颁发证明token的人身上。 承租人证明他们有这个token，向所有者支付一笔款项，并且原子性的发放一个临时token，允许他们解锁并使用汽车一段时间。 这是在没有创建帐户的情况下完成的，或者需要提交大量文档由车主手动验证完成。
Taking this even further, the owner can skip Uber all together and rent her car directly to strangers. Not wanting her car to be trashed by some random stranger, she can restrict her renters to those who have an attestation token issued by the 'better drivers bureau'. The renter proves they have this token, pays a sum to the owner and is atomically issued with a temporary token that allows them to unlock and use the car for a certain period of time. This is done without the creation of an account or need to submit tons of documents to be validated manually by the owner.

如果车主希望出售汽车，她只需要在任何网站上列出价格。 所有权token和付款可以原子方式交换（确保买方或卖方都不会受到欺骗），新的所有者可以驾车离开，甚至无需面对面地与原始所有者会面。 新买家事先知道汽车是否已经注册，并且仅通过验证其钱包中的原始所有者的所有权token而合法拥有。 一旦发生交换，原始所有者的token就会失效，并且她无法再操作汽车。 一旦交换发生，也可以自动使保险单无效，并为原始所有者提供过早取消的折扣。
If the owner wishes to sell the car, she only has to list it on any website with a price. The ownership token and payment can be swapped atomically (ensuring neither the buyer or seller is cheated) and the new owner can drive away with the car without even meeting the original owner face to face. The new buyer knows in advance whether the car has been registered and is legally owned by merely validating the original owner's ownership token in their wallet. The original owner's token is invalidated once the swap occurs and she can no longer operate the car. It is also possible to automatically void the insurance policy once the exchange has occurred and provide the original owner with a rebate for premature cancellation.

本章用于展示愿景。我们将在后面的章节中再次核查这种良好集成的tokenised汽车token的技术层面。
This chapter serve to present the vision. We will have the opportunity to inspect the technical aspect of this well-integrated well-tokenised car token in later chapters again.

--
#### Tokenisation的挑战
#### The challenge of tokenisation

Tokenisation需要构建一个token并且与其事务规则和行为模式捆绑在一起，将他们从最初生成的系统中取出，他们可以在不同的场景下进行交易和使用。
Tokenisation requires bundling a token with its transaction rules and behaviour patterns, taking them off the system where they initially grew in, free them to be traded or used in different context.

允许用户通过token与不同系统进行交互：在汽车示例中，汽车token由制造商Holden发布，因为它包含与智能锁（*开锁*，*发动*，*锁住* 操作）和Holden自己的Web服务（ *定位* 行为）相互作用的代码，但它需要在其他环境中工作。例如 *拍卖* 动作由第三方拍卖网络服务提供。用户通过token访问拍卖服务，无需注册和证明所有权。*共享清单* 由第三方服务提供，该服务将汽车的使用Tokenisation为数小时或者数天，并逐个销售。所有者可以通过此token访问这个市场，买家将通过此token获得知晓汽车gps位置，开门和使用它的能力。
Allow users to interact with different systems through the tokens
:   In the car example, the car token is issued by Holden, the maker, and necessarily so because it contains code to interact with a smart lock (the *Open*, *Start*, *Lock* actions) and Holden's own web service (the *Locate* action), yet it needs to work in other environments. The *Auction* action, for example, is provided by a third party auction web service. The user access auction service through the token without the need of signing up and proving ownership. The *List for sharing* is provided by a third party service which tokenises the usage of the car by hours or days and sells them piecemeal. The owner can access such a market through this Token. The buyers will have information about the car's GPS location, the capacity to unlock the door and use it, through this token as well.

渲染token并将其与可在用户钱包中执行的操作相关联：在汽车的示例中，如果注册过期，工作中的web组件会将注册token绘制为红色或显示警告。过期的汽车将无法使用 *共享清单* 等操作，并且汽车的token页面应该明确的将消息传递给用户。
Rendering a token and associate it with the actions they can perform in the user's wallet
:   In the car example, if the registration expired, the web component at work would paint the Registration Token red or display a warning. Actions like *List for sharing* will not be available with an expired car rego, and the integrated token interface should clearly pass that message to the user.

允许在token上开发新协议：在汽车示例中，抵押可能是附加协议，也就是以太坊上下文中的ERC。 该协议可能有自己的实现，并且汽车token可能会预先约定它。 同样，有流媒体、通信、赌注或其他协议（参见“魔术”章节）。 框架必须允许它们存在并通过token使用。
Allow new protocols to be developed on tokens
:   In the car example, collateralization might be an additional protocol, an ERC in Ethereum context. The protocol might have its own implementation and the car token might pre-date it. Similarly, there are streaming, communication, staking or other protocols (See "Magic" chapter). The framework must allow them to exist and work with tokens.

将信任关系和业务背景传递给第三方：在汽车示例中，保险token通过NRMA提供道路救援服务，NRMA是另一家未与驾驶员直接签约的公司。 然而，驾驶员可以通过保险token访问此功能，并立即被确定为有资格获得帮助。 在此示例中，*信任关系*表示用户间接信任NRMA以提供路边援助，以在紧急情况下获取用户的GPS位置和身份信息。 *业务背景* 是指客户对路边援助的资格，例如保险支付，服务范围内的位置和未达到的年度上限等。在这个故事中，*信任关系*和*业务背景* 都必须在token中，而不是通过中心化的保险公司的网络服务，因为两者有不同的 a）可用性、b）隐私和c）集成要求[^abc]。
Carry trust relationship and business context to 3rd parties
:   In the car example, the insurance token provides Roadside Assistance service through NRMA, another company not directly contracted by the driver. Yet the driver might access this function through the insurance token and immediately be identified as qualified for help. In this example, *Trust relationship* means that the user indirectly trusts NRMA to provide roadside assistance, to obtain the user's GPS location and identity information at the time of emergency. *Business context* means the customer's qualification for roadside assistance, like insurance paid, location in the range of service and annual cap not reached etc. In this story both *trust relationship* and *business context* has to be in the token, not centralised through the insurance company's web service since the two have different a) availability, b) privacy and c) integration requirements[^abc].

[^abc]: 可用性：NRMA 24/7小时在线，但是澳航保险可能在公众假期或者晚上暂停服务。隐私：NRMA可以获取用户的GPR，但是澳航保险在法律上不允许。集成：大多数NRMA的客户不是通过Qantas Insurance 获得的，因此它将成为NRMA集成和额外安全问题的附加系统，以集成到Virgain Insurance的网络服务。在这三个小时中，可用性可能是最明显的。想象一下客户会有多生气，当他的汽车在澳大利亚贫瘠的内陆地区抛锚，这个时候发现无法得到道路援助，因为保险公司的网络服务器正在为了“更好的用户体验”而升级。
[^abc]: Availability: NRMA is online 24/7 but Qantas Insurance can suspend their services in public holidays or at night. Privacy: NRMA can learn user's GPS location but Qantas Insurance isn't legally allowed to learn it. Integration: Most of NRMA's customers are not obtained through Qantas Insurance, so it would be an additional system to integrate and extra security concern for NRMA to integrate to Virgain Insurance's web service. Of all three, availability might be the most visible. Just imagine how angry a customer will be, having his car breaking down in the middle of the barren Australian outback, and learn that the road-side assistance can't be authorised because the insurer's web service is upgrading "For a better user experience".

# 设计需求
# Design requirements

我们断言需要一种描述性语言（Tokenscript）来允许区块链技术实现“完全市场”和“集成网络”。 Tokenscript代表token行为标记语言。
We assert that a descriptive language (Tokenscript) is needed to allow blockchain technology to enable "frictionless markets" and an "integrated web". Tokenscript stands for Token Behaviour Markup Language.

由于Tokenscript是一个解决方案层，而不是像以太坊和Plasma(译者注：一种以太坊的二层Layer 2扩容框架)这样的基础层技术，我们选择通过实例介绍该技术，并为观众提供丰富的商业环境讨论。
By virtue of Tokenscript being a solution layer rather than base-layer technologies like Ethereum and Plasma, we choose to introduce the technology by example and provide rich business-context based discussion for a broader spectrum of audience.

## 解决无摩擦市场的需求
## Address "Frictionless Market" needs

仔细研究“市场”，市场并不是一个拥有大量信息的嘈杂渠道; 更重要的是，这是一个交割与付款的地方。 由于区块链不依赖于中间商，即交易主机，我们的重点转变为交易的token，即 *可交付成果* 和 *支付* ，以及它们在市场中的角色。
Taking a closer look at "market", a market is not a noisy channel overloaded with information; more importantly, it is a place where delivery versus payment happens. With blockchain relying less on the middlemen, the host of the trades, our focus is turned into the tokens being traded, that is, *deliverables* and *payments*, and their role in market.

交付
：金钱可以买到各种各样的东西：资产、商品和服务。
deliverables
:    All sorts of things money can buy: assets, goods and services.

付款
：Ether，DAI，Sovereign。 任何类似货币的东西。只有可编程货币才与本文相关
payment
:    Ether, DAI, Sovereign. Anything currency-like. Only programmable currencies are relevant to this paper.

市场
：市场是交割与付款发生的地方。 *市场*是一个概念，而不是一个实体市场。 在网站上结账的用户正在访问市场。 她不必在市场（例如亚马逊）这样做。
market
:    Market is where delivery versus payment happens. *Market* is an concept, not a marketplace. A user who checks out on a website is accessing a market. She doesn't have to be in a marketplace (e.g. Amazon) to do so.

Tokenscript 向*市场*提供*可交付的*及*付款*方面token的“插件”。
Tokenscript provides both *the deliverable* and *the payment* side tokens to "plug-in" to the *market*. 
这样的框架对于token的呈现，索引，交易，贸易，拍卖，组合......以实现完全市场是至关重要的。
Such a framework is essential for tokens to be presented, indexed, transacted, traded, auctioned, combined... to work towards a frictionless market.

我们将通过每个*可交付*方面和*付款*方面的示例介绍Tokenscript。
We will introduce Tokenscript through an example on each of the *deliverable* side and on *payment* side.

## 可交付方面的示例： 1% 房产token
### Deliverable side example: 1% property token

让我们想象一下“1％房产”的市场。房产所有者可以发放许多token，每个token代表1％的房产所有权。他可以出售这些token以换取现金。
Let's imagine a market for "1% property". A property owner can issue many pieces of a token, each represents 1% ownership of the property. He can sell these tokens for cash.

买家需要了解相当多的信息。很容易理解，如果基础token被出售，这样的token将获得1％的销售收入，但这中间还有很多细节问题。
A buyer needs to know quite a bit of information. It's easy to understand that such a token would fetch 1% of the sales revenue if the underlying property is sold, but a lot more details are needed:

1. 房产在哪里以及它的状态如何？
1. Where is the property and what status is it in?

2. 1％的房产代币所有者可以投票吗？例如，有关丛林火灾保险的购买决定？
2. Can a 1% property token owner vote?  For example, on the purchase decision to insurance against a bush fire?

3. 1％是否在房产销售时自动转换为货币，或者代币持有人是否可以选择继续持有？
3. Is the 1% automatically converted into currency at the time of property sales, or can the token holder elect to continue holding it?

4. 是否正确承保了token以防止双重抵押？
4. Is the token properly underwritten to prevent double-collateralization?

5. 如果房产是抵押贷款的抵押品，清算事件的条件是什么？
5. If the property was collateralized for a mortgage, what is the condition for a liquidation event?

6. 提供买方身份证明是购买的条件吗？
6. Is providing a buyer's identity attestation a condition of a purchase?

7. 卖方是房产的实际所有人吗？
7. Is the seller the actual owner of the property?

8. 过去几年该地区类似物业的表现如何？
8. What was the performance of similar properties in the region in the past years?

9. 该房产的历史销售价格是多少？
9. What was the historical sales price of this property?

具体到区块链，我们还有：
Specific to blockchain, we also have:

10. 如何正确安全地为资产建立交易（购买，投票等）

10. How to correctly and securely construct a transaction for the asset (purchase, voting etc)

我们将这些贸易敏感信息分为四类：

- 产品说明 [^pd]。 在PD中的项目2,3,5,6
- 证明信息。 在Attestations中的项目1,4,6,7
- 参考信息。 项目8,9
- 行为信息（如何执行资产行动）。项目10

We categorise these trade-sensitive information into four categories:

- product description[^pd]. Item 2, 3, 5, 6 are in PD
- attested information. Item 1, 4, 6, 7 are in Attestations.
- reference information. Item 8, 9.
- action information (how to perform an asset action). Item 10.

可以理解的是，买家需要访问所有这些信息以做出明智的决定。
Understandablly, the buyers need to access all these for an informed decision.

[^pd]这个词来自金融部门，通常用于描述包装的投资产品。它基本上是指计算利润的公式和公式中的变量的当前值。
[^pd] The word is loaned from the financial sector, usually used to describe packaged investment products. It basically means the formular which profit is calculated and the current values of the varibales in the formular.

#### 产品描述
#### Product description

产品描述信息通常在智能合约中。 在以太坊的情况下，这些可以通过进行一些智能合约函数调用来获得，因此，唯一需要的工作是将它们转换为演示文稿 - 通常意味着转换成为用户语言并将“实际”值转换为精心打勾的复选框。 这有助于介绍Tokenscript的第一个功能：充当智能合约的表现层。
Product description information is typically in the smart contract. In Ethereum cases, these can be obtained by making a few Smart Contract function calls, therefore, the only needed work is to convert them into presentation - usually it means translating to the language user speaks and converting "True" value into a nicely ticked checkbox. This serve to introduce the first functionality of Tokenscript: acting as a presentation layer for smart-contracts.

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

这个简化的 `attribute-type` 代码片段允许从 `holding-contract` 获取投票权的值，这是一个在Tokenscript中其他地方定义的智能合约，并以几种语言之一呈现。

This simplified `attribute-type` code snippet allows the value for Voting Right to be fetched from `holding-contract`, which is a smart contract defined somewhere else in the Tokenscript, and present it in one of a few languages.

#### 证明信息
#### Attested information

证明只是一条经过签名的用来说明事实的信息。通常使用证明来表示满足交易的条件，更多关于证明的信息如下。
Attestation is just a signed message stating a fact. Attestations are often used to satisfy the conditions of the transactions. More on that in the chapter Attestations.

在1％财产token的示例中，涉及的证明是：
In the 1% property token example, the involved attestations are:

- 通过身份管理机构和所有权契约办公室，以证明发行人对财产的所有权。
- by identity authority and title deeds office, to attest the issuer's ownership of the property.
- 通过抵押权限[^set-operation]来防止双重抵押
- by collateralization authority[^set-operation] to prevent double collateralization
- 由买方提供投资此类资产的身份或能力
- by buyers, for providing identity or capacity to invest in this type of asset

[^set-operation]：最终，这可能是一个加密集合操作，但即使发生这种情况，也需要在Tokenscript中描述指示上下文（用户代理）进行计算的元数据。
[^set-operation]: Eventually, this could be a cryptographic set operation, but even if that happens, the metadata directing the context (user-agent) to proform the computation still needs to be described in Tokenscript.

前两个证明并未存储在智能合约中，由于成本（交易的大小和数量）和隐私的原因。可以采用零知识证明来证明该证明适用于所述财产和所述所有者的通用证据，并且它尚未过期。 Tokenscript中还描述了预期和可验证的证据。
The first two attestations are not stored in smart contract for cost (size and number of transactions) and privacy reasons. It's possible to utilise zero knowledge proof to provide a generic proof that the attestation is for the said property and said owner, and it has not expired. What proofs are expected and can be validated is also described in Tokenscript.

此外，交易需要来自买方的身份证明或投资能力证明。 这些也在Tokenscript中描述，因此上下文（例如，用户代理）可以防止用户在没有限定证据的情况下提交交易或帮助用户为购买交易选择合适的证明。
Furthermore, the fact that the transaction requires an identity attestation or investment capacity attestation from the buyers. These are described in Tokenscript as well so the context (e.g. user-agent) can prevent the user to submit a transaction without qualifying proof or help the user to select suitable attestations for a purchase transaction.

#### 参考信息
#### Reference information

参考信息与token相关，由Web服务提供，通常通过RESTful API调用。[^trusted-information]
Reference information is what relevant to the token and provided by web services, typically through a RESTful API call.[^trusted-information]

[^trusted-information] 最初我们将其称为“可信信息”，这意味着以前的房产销售价格或区域性能数据等数据只是“提供”，没有区块链证据或证明，因此，必须由用户自己信任。 事实证明，这个用语是错误的，因为一些开发人员认为它意味着“经过验证的信息”，并且已经提供了可靠信息。 因此，我们使用了一个不太精确的用语“参考信息”，遗憾的是，它就像一个包罗万象的短语。
[^trusted-information]: Originally we call it "Trusted information", meaning data such as previous property sales price or regional property performance data is just "provided", without blockchain proofs or attestations, hence, it has to be explicitly trusted by the user. As it turned out, this term misfired as some developers think it means "proven information" and provided as trusted already. So we used a less precise term "Reference information", which, unfortunately, feels like a catch-all phrase.

由于Tokenscript由token发行者签署（不是token所有者 - token发行者通常是部署智能合约的实体），因此假定来自Tokenscript中指定的网络API的参考信息是可信的。 安全章节将详细说明不同的信任级别。
Since Tokenscript is signed by the token issuer (not token owner - the token issuer is often entity that deployed the smart contrat), the reference information sourced from the web apis specified in Tokenscript is assumed trusted. The security chapter will detail different levels of trust.

今天，与token相关的所有此类信息，通常一起保存在由部署token的同一实体制作的DAPP网站上。 我们认为，要使token有效地市场化，需要将其抽象出来并置于token行为语言Tokenscript中。
Today, all such information related to a token is usually held together on a DAPP website made by the same entity that deployed the token. We argue that for tokens to be effectively marketized, It needs to be abstracted out and placed in the token behaviour language Tokenscript.

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

这些信息是一套超级智能合约可编程接口（以太坊中称为ABI），附加部分是业务逻辑（例如财产必须仍然有效且卖方仍然拥有它）和表示逻辑（例如消息“该物业已被清算，不再出售“）。
These information is a super-set of smart contract programmable interface (In Ethereum, called ABI), with the additional part being business logic (e.g. property must be still valid and seller still have it) and presentation logic (e.g. the message "The property is liquidated. Purchase no longer possible").

总之，Tokenscript允许以下的上下文（用户代理或交易引擎）：

- 从持有智能合约、证明和参考资料中获取token相关信息。
- 生成token的视觉或音频呈现
- 生成可执行的操作列表以及如何构建交易。
In conclusion, Tokenscript allows the context (user-agent or trading engine) to:

- Fetch token related information from its holding smart contract, attestations and references.
- Produce a visual or audio rendering of the token
- Produce a list of actions that can be performed and how to constrct the transactions.

任何一方都能够使用Tokenscript渲染和应用函数到token，包括通用市场，用户代理和第三方应用等实体。 我们将这部分称为“上下文”。
Any party is able to render and apply functions to the token using Tokenscript, including entities like generic marketplaces, user-agents and 3rd party apps. We call these parties "context" in general.

### 为什么需要Tokenscript
### Why Tokenscript

通过演示的第一个示例，我们利用这个机会阐明了为什么需要Tokenscript，而不是目前通过DApp提供资产访问的主流方式。我们认为目前流行的方法不适合创建完全市场，而Tokenscript可以提供*互操作性*、*可扩展性*和*安全*等保障。
With the first example demonstrated, we use the opportunity to articulate why Tokenscript is needed, over the current prevailing way of providing asset access with a host DApp. We argue that the current prevailing method is not suitable for creating a frictionless market, while Tokenscript could, by providing reasons in the areas of *interoperability*, *scalability* and *security*.

#### 互操作性：
#### Interoperability:

假设名为Peter的房产大亨希望创建一个名为“Peter's Pride Asset”的网站，在那里有市场上最好的房产。他可以创建这些房产的列表，其中包含当前价格、位置、建筑物年头甚至照片等丰富信息，用户可以点击购买。但是他没有理由必须要这样做，因为token的数据在区块链上并且交易不需要中间人就能执行。但是，他需要获得如何在其网站上呈现token的本地知识，例如如何从其持有智能合约中获得token的到期时间。如果基础智能合约经历了变化，例如添加属性（例如议会费率），他的网站将需要升级。
Suppose a property guru named Peter wishes to create a website called "Peter's Pride Asset", where he selects the best properties available on the market. He can create a listing of those properties with rich information of the current price, location, age of the building and even photos, which the users can purchase with a click. There is no reason that he needs permission to do so because the data of those tokens are on the blockchain and the transaction of those tokens requires no middlemen. However, he would need to obtain the knowledge local to how to render the token on his website, like how to get the expiration of a token from its holding smart contract. If the underlying smart contract has gone through changes, like adding an attribute (e.g. council rate), his website would need to upgrade.

同样，交易规则也可能会更新，要求买房者提供身份证明作为交易环节的一部分。如果没有快速升级，他的用户将提交不符合要求的交易，并且在接下来的区块中被拒绝。最终，他会将token的呈现和交易，交给与该token绑定的Dapp，这就回到中心化状态，并限制该领域的创新和竞争。
Similarly, the transaction rule might be updated to require the buyer to submit an identity attestation as part of a purchase. Without a speedy upgrade, his users would submit transactions not conforming and get rejected later in the blockchain. In the end, he would resort to passing the rendering and trading of the token to the Dapp tied to this token, returning to a centralised status and limit the innovation and competition in this space.

类似的方式，假设一个投资者论坛允许成员使用他们的1%房产token登录，每个帖子下的token呈现都需要来自与token绑定的Dapp。这将会是一个非常大的工作量，为论坛提供token并且保持代码更新，并且这个将会和Dapp的可用性强耦合。
In a similar fashion, suppose an investors' forum where the members are allowed to login using their 1% property token, the rendering of the token, under each post, would need to be sourced from the Dapp tied to the token, since it's too much work for a forum to render the token and keep the code updated. Such sourcing would require permission and might be tied to the availability of that Dapp.

#### 可扩展性
#### Scalability

横向来看，相同类型的资产可能在多个网络（如 Plasma 链）上具有其token实例。买方可能只对澳大利亚的资产感兴趣，因此仅与澳大利亚1％房地产网络相关联。可能难以拥有一个全知的节点来为所有现有token提供呈现的token信息，尤其是在设计网络时考虑到隐私的情况。因此，为了扩展，必须从对token的访问中分离关于token（Tokenscript）的知识。
Horizontally, the same type of asset might have its token instances across multiple networks like Plasma Chains. A buyer is likely to be interested only in assets in Australia, and therefore only connected to the Australian 1% Property network. It can be difficult to have an all-knowing node to provided rendered token information for all existing tokens, especially if a network is designed with privacy in mind. Therefore, to scale, the knowledge about the token (Tokenscript) must be detached from the access to the token.

纵向来看 - 通过说*垂直方向*，我们的意思是向上构建，在token之上使用token交易或创建结构化token的方式来构建结构化的交易。此类交易和token访问基础token(component token)。例如，如果我们想要一个token，其组成是来自全球100个城市的样本的1％资产token，对于中型投资者来分摊风险，一个可以操作这样token的系统必须以成员token的知识来构建。再次它不能依赖于与该资产相关的原始Dapp的可用性、安全性和开放性。 Tokenscript可以在中间用于制作这样的token。
Vertically - by speaking *vertical*, we mean to build upward, to building structured transactions using a token transaction or creating structured tokens on top of a token. Such transaction and token access the component tokens. For example, if we desire a token whose make up is a 1% property token from a sample of 100 global cities, for mid-size investors to distribute the risk, a system that can manipulate such a token must be built with the knowledge about member tokens. It again cannot depend on the availability, security and openness of the original Dapp tied to that asset. Tokenscript would work in the middle for the making of such tokens.

如果我们以Peter's Pride Property网站的例子作为Hello World示例，可能需要用户提交交易，不仅要购买token，同时还要Peter付费（tips）。如果只有token发行者的DAPP知道如何组装token购买交易，这对Peter来说是不切实际的。
If we follow the example of Peter's Pride Property website as a Hello World example, it might need the user to submit a transaction not only purchase a token, but also tips Peter in the meanwhile. If only the token's issuer's DAPP knows how to assemble a token purchase transaction, this will be impractical for Peter.

即使在简单的场景中，垂直情况自然也会比这复杂得多。您将在本章“基础网络”部分的电子商务故事中看到一个例子。
The vertical stack naturally can be a lot more complicated than this, even in simple scenarios. You will see one revealed in an e-commerce story in the "Integrate the web" section of this chapter.

#### 安全性
#### Security

即兴创建一种模型是不切实际的，其中用户可能签署的每个事务都以用户可读的格式呈现。使用事务可视化工具开始这样的工作很简单，向用户解释一个神秘的事务负载，类似于Linux的`identify（1）`命令，但最终系统集成和UX需求将超过字典样式事务可视化器能够完成的范围。
It is impractical to improvise a schema where every transaction the user might sign is rendered in a user-readable format. It's easy to start with such an effort with a transaction visualiser tool, interpreting an enigmatic transaction payload to the user, similar to Linux's `identify(1)` command, but ultimately the system integration and UX needs would surpass what a dictionary style transaction visualiser can do.

以1％房产token为例; 确认信息可能会是这样的：您打算用45个Ethers购买1％的房产＃802820，您确定吗？
Take the 1% property token as an example; a confirmation might look like this: You are going to purchase 1% of property #802820 with 45 Ethers, are you sure?

用户不确定他正在观看的玻璃天花板设计的两居室的房子是否是＃802820。
The user will be unsure if the glass ceiling designer 2-bedroom house he is watching is #802820.

基于字典的翻译可视化器不能做的更好，因为正确呈现属性标记需要的不仅仅是文字处理。这个限制很容易发现，即使没有在本章的“集成网络”部分中介绍集成方案。
A dictionary based translation visualiser cannot go further because correctly rendering the property token requires more than word processing. This limit is easily hit even without introducing integration scenarios in the "Integrate the web" section of this chapter.

最终，使用代码生成交易，用户必须将信任委托给代码。用用户的话说，我正在访问与此token绑定的网站，所以我相信我签署的这个交易是为了我在使用网站时的意图而生成的。这是一个破碎的信任模型，就像的TLS模型一样是对网站的信任而不是内容。
Eventually, a transaction is generated with code, and the user would have to delegate the trust to the code. In a user's words, I am accessing the website tied to this token, so I will trust that this transaction I am signing is generated for the intention I have while using the site. This is a broken trust model, a regression to the TLS model of trusting the site instead of the content.

Tokenscript旨在分离token呈现代码和交易生成代码，并将它们打包到其容器中，由用户可能信任的一方签名（通常由用于部署智能合约的相同密钥签名）。有不同的信任级别，我们将在后面的章节中详细介绍。
Tokenscript is designed to separate token rendering code, and transaction generating code and package them into its container, signed by a party that the user is likely to trust (often, signed by the same key used for deploying a smart contract). There are a few trust levels, which we will detail in later chapters.

从Peter's Pride Property推荐网站购买1％房产token的用户可以获得一个渲染和交易包，由创建此类代币的持有合同的同一组人签名。因此，用户可以从具有类似信任级别的任何网站购买资产，或者从微信或Facebook私人消息购买资产，并且知道它是正在呈现和交易的真实token。
A user who is purchasing a 1% property token from Peter's Pride Property recommendation website can be supplied with a rendering and transaction package, signed by the same group of people who created the holding contract of such tokens. Therefore the user can purchase assets from any website with a similar level of trust, or purchase it from a WeChat or Facebook private message and know it is the real token being rendered and transacted.

## 付款方示例：DAItoken
## Payment side example: DAI token

DAI是一种用于支付的代币 - 购买加密货币，购买商品和服务等等。它锚定美元的价格。没有固定供应上限，它本身不是一个投资品。
DAI is a token designed for payment - purchasing security token, purchasing goods and services and so like. It's intended to match USD in value. Not fixing the supply cap, it is not itself an investiment candidate.

在许多方面，DAI的功能类似以太网，它是以太坊的基础货币。 但是，它不能成为Ether的替代品。
In many ways DAI functions like Ether, the base currency in Ethereum. However, it can't be a drop-in replacement for Ether.

首先，为以太坊编写的Dapps可能不知道用户有DAI令牌，除非它明确支持DAI。 例如，接受以太币作为付款的比萨订购服务不能轻易地开始接受DAI令牌。 即使DAI提供DAI-to-Ether网关服务也是如此，该服务以原子方式在同一事务中将DAI转换为以太网，使用生成的Ether来购买Pizza。
First, the Dapps written for Ethereum may not be aware that the user has DAI token, unless it explicitly support DAI. A Pizza ordering service that accepts Ether as payment, for example, cannot trivially start to accept DAI token. This is true even if DAI provides a DAI-to-Ether gateway service which, in an atomic fashion, converts DAI to Ether in the same transaction which uses the resulting Ether to purchasing Pizza.

如果Pizza网站没有升级，用户必须首先将DAI转换为Ether，然后通过第二次交易购买Pizza。 这样的过程不仅不方便，而且缺乏原子性，这意味着用户需要通过努力将DAI转换为Ether，但是由于Pizza已经售罄而无法结账，用户必须处理他已经购买的eth
If Pizza website doesn't upgrade, the user has to convert DAI to Ether first, then, purchase Pizza with a second transaction. Such a process is not only inconvenient, but lack atomicity, meaning that the user could have converted DAI to Ether trough the effort, only to fail the checkout since the Pizza is sold out, and ended up with additional Ethers that she has to deal with.

值得注意的是，披萨网站无法升级到支持DAI，因为不知道如何获取用户的DAI余额[^ balance-is-privacy]（为了不浪费交易费结果只发现DAI余额不足），如何构建DAI撤销事务或DAI-Ether网关事务，并对DAI持有合同进行直接智能合约函数调用。
It's worth noticing that the Pizza website cannot upgrade to support DAI without knowing how to discover the user's DAI balance[^balance-is-privacy] (to not to to waste a transaction fee just to find the DAI balance is insufficient), how to construct a DAI withdraw transaction or DAI-Ether gateway transaction and make direct smart contract function calls to the DAI holding contract.

[^balance-is-privacy]:最终，披萨网站不仅不需要检查余额，因为Tokenscript会处理它，也不需要知道余额。 这将需要底层区块链的支持，但如果我们继续当前的趋势，继续关注业务逻辑的网站也关心支付逻辑，这最终无法完成。
[^balance-is-privacy]: Eventually, the Pizza website would not only be oblivious about how to check balance, since Tokenscript handles it, but also not possible to know the balance. This would require underlying blockchain's support, but ultimately cannot be done if we continue the current trend where website, who should care about business logic, also care about payment logic.

当然，Pizza网站不是管理这些付款方详细信息的最佳位置。 Tokenscript通过以下方式解决了这个问题：
Naturally, the Pizza website isn't in the best position to manage these payment-side details. Tokenscript addreses this problem by

1.封装支持DAI所需的智能合约函数调用，以及用于在Tokenscript中构建所需事务的javascript，由DAI发行者签名。
1. Encapsulating the smart contract function calls needed for supporting DAI, along with the javascript to construct needed transactions in Tokenscript, signed by DAI issuer.
2.Tokenscript，兼容性提供浏览器端实现和基于javascript的实现，以便Pizza商店可以调用泛型操作来返回ETH（或任何可接受的货币）并使用Tokenscript中的支付逻辑来交易。
2. Providing a browser side implementation and a javascript based implementation for Tokenscript compatibility, so that the Pizza shop could just call a generic action to return Ether (or any acceptable currency) and let the payment logic in Tokenscript work at transaction.

Tokenscript嵌入支付逻辑和表示的能力意味着它不仅可以用用户的语言显示消息（如余额或“余额不足”消息），而且可以执行预检余额等功能，暂停结账流程以便用户可以执行充值流程并返回结帐流程以完成结账。
Tokenscript's capacity to embed payment logic and presentation means that not only it can display messages in user's language (like balance or "insufficient balance" message), but it can perform functions like pre-checking the balance, pause the checkout flow so that the user can perform a top-up flow and return to the checkout flow to finalise the checkout.

对于用户来说，该过程类似于结账过程引导用户到Paypal来完成交易，唯一的区别是该过程在更强大的本地用户代理中发生。
To the user, the process resembles a bit like the checkout processs leads the user to Paypal to finalise the transaction, except the process happens locally in an enhanced user-agent.

我们再次强调，目前的方法不适合创造完全市场，但是Tokenscript可以，通过提供*互操作性*，*可扩展性*和 *安全性* 来创造完全市场。
We again argue that current prevailing method is not suitable for creati
ng a frictionless market, while Tokenscript could, by providing reasons in the areas of *interoperability*, *scalability* and *security*.

总之，Pizza网站没有必要自行处理支付方逻辑的所有事情。 传统方法是让Pizaa网站使用MakerDAO项目提供的javascript。 javascript可能使用也可能不使用MakerDAO提供的RESTful API
As concluded, Pizza website would not have the necessary payment side logic to handle everything on its own. The traditional approach is to let the Pizza website use the javascript sourced by MakerDAO project. The javascript may or may not use a RESTful API provided by MakerDAO

这种方法通过引入其他一些问题解决了一个问题。
This approach solves one problem by introducing quite a few others.

#### 安全性
#### Security
当用户尝试进行购买时时，使用本地javascript（Pizza shop javascript）和DAI提供的所谓安全javascript的组合来创建交易。 向用户呈现交易载荷，该交易的载荷包含访问DAI合同的参数，例如，支付金额，以及访问比萨网站合同的参数，例如购买比萨饼的数量和选择的浇头。 显然，这样的交易必须发送到DAI合同并通过（代理）到披萨店合同。
When the user makes the purchase attempt, the transaction is created with the combined effort of local javascript (Pizza shop javascript) and the supposedly secure javascript supplied by DAI. The user is presented with a transaction payload that contains both the parameters to access DAI contract, e.g. amount to pay, and the parameters to access the Pizza website contract, e.g. amount of pizzas to buy and the toppings of choice. Apparently such a transaction has to be sent to DAI contract and channeled (proxed) to the Pizza shop contract.


存在两个直接[^minor-security-concerns]安全问题。 首先，网站没有正确使用MakerDAO javascript库，其中包含最终的交易构建器。 其次，它不是MakerDAO真正的的javascript，而是由黑客取代的版本。
There are two immediate[^minor-security-concerns] security concerns. First is that the website didn't use the MakerDAO javascript library correctly, which has the final transaction builder in it. Second is that it is not MakerDAO's javascript at work, but a version replaced by a hacker.

[^ minor-security-concerns]：当两个系统集成在网络上时，通常存在大量安全问题。 举一个例子，如果一方未更新代码以反映另一方的更改，则可能会生成格式错误的交易。 跟踪这些交易允许攻击者定位未更新的网站。
[^minor-security-concerns]: When two systems plug on the web, usually there are a hoard of security concerns. To give one example, if a side didn't update the code to reflect the other side's change, the resulting malformed transaction might be rejected. Tracing these transactions allow an attacker to target websites not updated.

这些问题通过Tokenscript中使用的封装方法解决。
These issues are addressed by the encapsulation method used in Tokenscript.

首先，交易生成代码由MakeDAO单独签名，并与用户代理方分开更新。 网站的代码不必签名，因为它只提供业务逻辑，而不是支付逻辑。 比如，如果发现错误，DAI可以通过更新这些签名的指令来暂停付款，而且Pizza网站的行为就像已经更新并解决问题一样。 如果发现该错误存在于DAI控股合同中，并且部署了替换合同，MakerDAO将更新Tokenscript并再次签署，而Pizza网站不需要任何事情。
First, the transaction forming code is signed by MakeDAO separately and updated separately from user-agent side. The website's code doesn't have to be signed because it just supplies the business logic, not payment logic. Say, if a bug is found, DAI can suspend the payment by updating these signed instructions, and the Pizza website would behave as if it has been updated to address the issue. If the bug is found to be in the DAI holding contract, and a replacement contract is deployed, MakerDAO would update Tokenscript and sign it again, without Pizza website having to do anything.

其次，通过明确要求用户信任MakerDAO签署的Tokenscript，用户不需要信任Pizza网站对交易内容的呈现，因为它将由受信任的MakerDAO Tokenscript呈现
Second, by explicitly asking the user to trust the Tokenscript signed by MakerDAO, the user would not need to trust Pizza website's rendering of the transaction content, since it would be rendered by the trusted MakerDAO Tokenscript.

！[使用Tokenscript付款。 请注意，* Complete Order *按钮不在网站上，而是在Dapp浏览器生成的Tokenscript令牌区域中，其中呈现交易的代码已预先签名。](img/ayment-in-wallet.jpeg)
![A payment using Tokenscript. Notice that the *Complete Order* button is not on the website, but in the Tokenscript token area generated by Dapp browser, where the code to render the transaction is pre-signed.](img/payment-in-wallet.jpeg)

第三，如果需要添加安全协议，例如，来自网站的证明（可以重新使用SSL证书）来证明接收智能合约的交易，或智能合约通过域名返回网站的明确信任， 额外的逻辑是升级dapp浏览器来提供对新的Tokenscript功能的支持和token发现者对新Tokenscript代码的更新，而无需触及网站。
Third, if secure protocols needs to be added, for example, an attestation from the website (can re-use the SSL certificate) to certify the transaction receiving smart contract, or the smart contract returning explicit trust of the website by domain name, the additional logic can be a combined effort of upgrading the dapp browser's support of new Tokenscript feature and the token issuer's new Tokenscript code, without touching the website.

#### 互操作性
#### Interoperability

添加对DAI本身的支持是很麻烦的，更不用说添加其他付款方token了。 在2017-2018年的狂热中，许多支付方token被发明并投入大量资金。就连是不安全的token，也在宣传他们的token可用于支付或共同支付某些商品和服务的某种方式。 例如，电力token被发明为未来象征化电力的货币。 他们中的大多数只是笑话，但如果他们开始工作呢？ 即使这些token中只有10％由自己的ICO团队完成，但所有这些token都会在将DAItoken集成到市场中时遇到类似的麻烦。
Adding support for DAI itself is trouble enough, not to mention adding other payment side tokens. In the 2017-2018 frenzy, a lot of payment side tokens are invented and heavily invested in. Pretty much anything advertised not as a security token outlines some way their token can be used to pay or co-pay some goods and services. Electricity tokens, for example, is invented as the currency of the future tokenised electricity. Most of them are jokes, but what if they are put to work? Even if only 10% of these tokens are done by sincerer ICO teams, all of them would forsee similiar trouble as the integration of DAI token into the market.

每种付款方货币都有自己的付款方逻辑。以DAI为例，它具有以下支付方逻辑：
And each payment side currency brings its own payment side logic. Take DAI for example, it has these payment side logic:

1. DAI令牌的创建需要一个称为CDP的设置阶段。
2. CDP的风险等级发生变化。用户应收到其CDP处于清算风险的通知。我们将在下一章再次讨论这种情况。
3. 如果余额不足，但用户在他/她的帐户上有相当多的Ethers，她可以暂停结账，然后返回结帐。
1. The creation of DAI tokens requires a set-up phase, called CDP.
2. The risk level of a CDP changes. Users should receive a notification of their CDP is at liquidation risk. We will cover such case again in the next chapter.
3. If the balance runs low, but the user has quite a bit of Ethers on his/her account, she may pause the checkout to top up before returning to the checkout.

当架构师读到这里的时候，他可能会绝的这些都可以在外部完成。如果发生任何这些情况，只需将用户踢回MakerDAO网站即可。这不是像Point + Pay这样的支付方创新，其中选择与支付在同一屏幕上选择。 事实上，您可以观察到中国支付方创新的大量例子，例如：
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

Tokenscript打算为支付方创新和可交付方提供空间。 传统上，合作伙伴支持抑制了支付方创新。 美国运通实施了支付API的积分，但在过去几年中，只有不到5％的合作伙伴电子商务网站将此作为结账选项提供。
Tokenscript intends to give room for payment side innovation as well as deliverable side. Traditionally, partner support used to curb payment side innovation. American Express implemented points to pay API but after years only less than 5% of partner e-commerce websites provided this as a checkout option.

#### 可扩展性
#### Scalability

付款和交付可能不在同一区块链上。
The payment and delivery may not be on the same blockchain.

在dapp网站中呈现用户的余额简要提到几页后的隐私问题，但作为区块链扩展，dapp的服务器端可能无法在某些数据（如余额）上同等访问客户端。 网站可能只会观察交易结果，并乐意按规则交付实物或象征性商品。
Rendering user's balance in dapp website is briefly mentioned as a privacy issue a few pages back, but as blockchain scales, the dapp's server side may not have equal access to the client on some data like balance. It's possible that the website only observes the result of the transaction and happy to deliver physical or tokenised goods by rules.

任何可扩展性计划都不太可能不涉及dapp浏览器和钱包的参与。 他们使得dapps使用他们可以提供的任何高级JavaScript来处理付款方面的情况。
It's unlikely any scalability plan will not involve the participation of dapp browsers and wallets. They results in situation that dapps could not take care of the payment side with whatever advanced javascript they can supply.
需要解决“集成网络”
## Address the "Integrate the web" need

我们发现网络很难集成的原因是各个网站之间只有一个链接，即URL链接。 链接不包含业务流程，身份验证或信任关系。 链接上没有集成锚点。
We trace the reason that the web is poorly integrated to the only link between the units of the web, i.e. URL links. A link carries no business process, authentication or trust relationship. There are no anchoring points for integration on links.

我们相信token是集成的锚点。 同样，最好可以通过示例来说明。
We believe the token is the anchor points for integration. Again, this is best illustrated by examples.

假设用户使用区块链从在线零售商Harvey Norman购买iPhone。 交易的输入将是一种货币; 在这种情况下，将输出三个token：
Suppose a user purchases an iPhone from Harvey Norman, an online retailer, using the blockchain. The input of the transaction will be a type of currency; the output, in this case, will be three tokens:

- 物流服务兑换token，可用于从本地提货站兑换产品。
- a shipping token, which can be used to redeem the product from a local pick-up station.

- 由Apple发行的保修token，允许iPhone在Harvey Norman以外的商店（例如Apple Center）进行维修。
- a warranty token, issued by Apple, which allows the iPhone to be serviced in shops other than Harvey Norman (e.g. Apple Centre).

 - 由Harvey Norman发行的收据token，允许产品在90天内退回。 如果您想将手机带出澳大利亚，这对于获得旅游税退税也很有用。
- A receipt token, issued by Harvey Norman, which allows the product to be returned in 90 days. It's also useful for getting a Tourism Tax Refund if you want to take the phone out of Australia.

如果没有token作为集成锚点，就必须通过不同的方式执行三种不同的服务。
If without tokens as the integration anchor, the three different services might be carried out by various means.
### 物流服务兑换token
### The Shipping Token

没有它，用户可能会得到一个跟踪号而不是一个token，跟踪号本身不携带任何认证信息，所以它不能用于提取产品，除非提供了提取码，可能会在短信供提供，这将会是这个过程变得更加困难。
Without it, a user might get a tracking number instead of a token, which itself carries no authentication information, so it can't be used to pick up the product unless a pickup code is provided, perhaps in SMS - even more poorly integrated with the process.

通过使用物流服务兑换token，运输公司可以远程更新token的信息，甚至可以像用户发送消息以通知即将到来的快递（如果token保存在移动钱包中）。通过一些加密技术，可以轻松授权其他人购买产品。
With the use of a shipping token, the token status can be remotely updated by the shipping company, even messaging to users to inform an upcoming delivery (if the token is held in a mobile wallet). With a bit of cryptography, it's easy to authorise someone else to pick up a product.

### 保修token
### Warranty Token

如果没有此token，用户可能需要序列号和在线注册过程来激活保修。 她甚至可能需要为此创建一个帐户，她可能很快就会忘记密码。
Without this token, a user might need the serial number and an online registration process to activate the warranty. She might even need to create an account for that, whose password she will probably soon forget.

通过使用保修token，可以轻松找到条款和到期日期，因为它是token属性。 用户可以使用token登录保修服务网站，放弃帐户。 token以被编程为接收诸如产品召回或紧急安全更新之类的消息。
With the use of a warranty token, the terms and expiration would be easy to find, as it is token properties. The user can log in to the warranty service website with the token, forgoing an account. The token can be programmed to receive messages like product call back or emergency security updates.

### 收据token
### Receipt Token

由于缺乏可靠的方式来验证购买，在线购买的产品通常无法返回商店，但可能通过在线方式（如回调）返回。 token携带足以过程完成的认证方法回调到商店。
Lacking a reliable way to authenticate the purchase, an online purchased product usually cannot be returned to the store but might be returned via online means such as a postback. A token carries the methods for authentication sufficient for the process to be done in store.

尽管这样的token不可转让或授权，但它仍然适用于第三方集成。 如果没有卖方的协作，税务局将确信收据不能伪造，并且执行快速简单的退税流程。 如果购买手机是为了工作，员工可以轻松地从信任他的的雇主那里报销费用。
Despite such a token not being transferable or authorised, it is still useful for 3rd party integrations.  The Tax office will be satisfied that the receipt can't be faked without collaboration from the seller, and allows a swift and easy tax-refund process. If the phone is purchased for work, the employee can easily reclaim the expense from an employer with the trust implied.

！[购买一个token，获得三个token。 它们可用于访问服务，如交付和维修。]（
![Purchase with one token, getting three tokens. They can be used to access services, like delivery and repair.](purchase-without-shipment-token.jpg)

正如我们通过使用token所观察到的那样，通常可以最终集成分散的业务流程和Web体验。 这与区块链的其他好处密切相关：比如完全市场。 在这个例子中：
As we can observe by the use of tokens, usually scattered business processes and web experiences can finally be integrated. This ties closely to the other benefit of the blockchain: a frictionless market. In this example:


 - 当手机进行二手交易的时候，很容易通过token转账将保修转给下一位用户，进一步打开市场。
 - When the phone traded is second hand, it would be easy to pass the warranty to the next user through a token transfer, opening the market further.

 - 由于运输能够被Tokenisation，买方很容易选择他最喜欢的运输公司，而无需手动提供商业信息（地址，产品，重量，日期），这将会进一步打开竞争市场。
- Since shipping can be tokenised, it would be easy for the buyer to choose his favourite shipping company without having to supply it with business context (address, product, weight, dates) manually, further opening the market for competition.

可以进一步扩展此示例以解决复杂和创新的业务案例。 假设购买不是使用法定货币，而是使用美国运通积分。 iPhone具有屏幕损坏保险，因此，交易将输出第四个保险token。
This example can be further extended to solve complicated and innovative business cases. Suppose the purchase is not made with fiat currency but with American Express points. The iPhone purchase will be insured for screen damage, and as a result, the transaction will have a 4th insurance token as the output.

当手机被修复屏幕损坏时，会发出有关手机购买记录的发票，以证明它是与积分一起购买的手机，从而可以当场支付保险费。
When the mobile phone is repaired for screen damage, an invoice is issued concerning the purchase record of the phone to prove it is the same phone purchased with the points, enabling the insurance to be paid on the spot.

如果没有此类token，用户必须提交账单，发票和维修证明才能提交索赔。 许多用户肯定会遗漏其中一个文件; 索赔可能需要几天时间，而且容易发生欺诈。
Without such tokens, the user will have to submit a billing statement, invoice and evidence of repair in order to submit a claim. Many users will surely miss one of those documents; the claim may take a few days, and still be prone to fraud.

在这种保险案例中，区块链允许业务流程创新，否则用户将会因为仅涉及太多方并且缺乏集成锚点这一点。牺牲便利性，
In this insurance case, the blockchain allowed business process innovation that otherwise would require the user to sacrifice convenience, for the mere fact that too many parties are involved and there lacks an integration anchor.

使用物联网进一步加强集成的能力。 让我们想象一下AirBNB的未来版本，其中预订被Tokenisation。 旅行者可以通过用他或她的token解锁智能锁来进入预订的AirBNB房屋，并且智能锁将识别预订token的当前所有者是谁。
The power of integration is further strengthened by the use of the Internet of Things. Let's imagine a future version of AirBNB, where the bookings are tokenised. A traveller can enter a booked AirBNB house by unlocking the smart-lock with his or her token, and the smart-lock would recognise who the current owner of the booking token is.

如果Alice拥有在特定时间窗口内使用房间的权利的token，或者用户的条款中的“预订”，那么她可以执行的操作是：
If Alice owns a token that represents the right to use a room during a specific time window, or "a booking" in user's terms, then the actions she could perform are:

登记 - 生成二维码以验证房东的预订，或使用支持NFC的手机打开智能锁。
Check-in - either produce a QR code to verify the booking to the landlord or use an NFC-enabled phone to open a smart-lock.

！[AirBnB token集成了物联网，允许token打开智能锁。]
![AirBnB Token integrates IoT, allowing the token to open a smart-lock.](img/airbnb.jpeg)

观察到理想化的集成，我们可以看到Tokenscript必须满足以下需求：

Observing the desirable integration, we can see Tokenscript has to satisfy the following needs:

- 允许定义token操作。 在运送token的情况下，将存在“兑换”动作（通过QR代码或NFC）和“授权”动作，其将允许其他人接收交付。
- Allow token actions to be defined. In the case of a shipping token, there would be a "redeem" action (via a QR code or NFC) and an "authorise" action which would allow someone else to pick up a delivery.

- 允许在操作中访问区块链功能。
- Allow blockchain functions to be accessed in an action.

- 允许在操作中访问Web功能
- Allow web functions to be accessed in an action

- 允许通过Web API或签名消息更新token状态（稍后将详细介绍）
- Allow the token status to be updated, via a web API or signed message (more on that later).

# Tokenscript的设计
# The design of Tokenscript

## 将token关联到智能合约和Web服务
## Relate tokens to smart contract and tokens to web services

早期的公共区块链项目试图将token逻辑和业务流程实现为智能合约。 以在线零售项目为例，这种智能合约不仅可以处理订单，还可以管理库存。 token事务逻辑（如交易有效的条件）与业务流程相关联，如检查库存。 当然，这种方法继承自人们构建网站的方式。
Early public blockchain projects attempted to implement both token logic and business process into smart contracts. Using an online retail project as an example, such a smart contract would not only process an order but also manages the inventory. The token transaction logic, like under what condition the transaction is valid, is tied with business process, like checking inventory. This method is, naturally, inherited from the way people build websites.

使用类比来证明这个并不是合适的做法，假设一个宜家经理决定格式化家具销售合同，以包括一个信息，哪一个顾客会去取家具包裹，它能在现实生活中运作吗？ 当然不会，合同必须反复修改以反映宜家库存管理状态，那个顾客拥有产品对贸易的有效性没有影响。
Using an analogy to demonstrate the inappropriate method, suppose an IKEA manager decides to format the furniture sales contract to include information like which aisle a patron should go to fetch the furniture package, would it work in real life? Of course not, the contract would have to be modified too many times to reflect Ikea warehouse management; which aisle has the product has no impact on the validity of the trade.

当这些尝试不起作用的时候，不顾一切撞墙的开发人员，开始抱怨当前一代区块链中的性能和隐私问题。确实，当前一代的区块链在性能和隐私方面存在很大的缺陷，但扩展它们来解决业务流程是解决问题的错误方法。 意识到当前的以太坊不适合作为业务引擎，ICO骗子在2017年吹捧了新一代区块链的想法，每秒有数万笔交易。 2018年，将区块链的虚假信息更新为“新云”，这是AWS功能的超集。 根本的想法是，区块链作为一种新技术必须是比以前更快更强的版本：云; 很像我们憧憬的2000年代运输的解决方案是飞行汽车，而不是优步。
When these attempts failed to work, developers, in a resolved effort pounding heads against the wall, complained about the performance and privacy issues in current generation blockchains. It is true that the current generation blockchains lack greatly in performance and privacy, but extending them would be the wrong approach to address business process problems. Realising that current Ethereum does not fit to be a business engine, ICO hustlers in 2017 touted the idea of new generations of blockchains with tens of thousands of transactions per seconds. 2018 saw the renewal of such disinformation picturing blockchain as "the new cloud", a superset of AWS' functionalities. The underlying thinking is that blockchain as a new technology must be a faster and stronger version of the previous ones: the Cloud; much akin to the way we imagined the 2000s transportation solution being flying cars, not Uber.

由于其额外的安全假设，拜占庭容错区块链永远不会超越AWS的业务引擎。 此外，围绕区块链业务流程构建防火墙是不切实际的。 如果性能，隐私和安全性原因不够具有说服力，那么本文提供的令人信服的论点在于生命周期管理：用户持有的token反映的契约关系将保留很长时间，而业务流程在理想情况下，每天都在完善。
Thanks to its additional security assumptions, Byzantine Fault tolerance blockchains would never outperform AWS's business engines. Furthermore, it's not practical to build a firewall around a blockchain business process. If performance, privacy and security reasons are not persuasive enough, the compelling argument this paper provides lies in the life cycle management: the contractual relationship, reflected by the tokens the user holds, will stay for a long time, while the business process is, ideally, perfected from day to day.

本文的作者提倡一种方法来划分智能合约和业务流程之间的界限。
The authors of this paper advocate a method to draw the line between a smart contract and a business process.

1. 智能合约规定了token的交易规则，而不是token的效用。
1. A smart contract dictates the transaction rules of tokens, not the utility of the tokens.

2. 通过token集成智能合约和业务流程。
2. A smart contract and business process are integrated through the tokens.

让我们沿着iphone购买示例继续阐述。在购买时创建了一个物流服务兑换token，代表用户接受货物的权利。这并不意味着在短短几秒钟之内购买被记录在区块链上，库存管理数据库选择一个仓库，从库存计数中扣除iphone，用货运跟踪器标记，并将跟踪器返回给token。由于区块链的原子性，像云平台那样使用区块链是荒谬的，并且是不可行的。
Going further along the online iPhone purchase example, at the time of purchase, a shipment token is created, representing the user's right to receive the delivery. It does not imply that in the very few seconds the purchase is recorded on the blockchain, an inventory management database selected a warehouse, deducted the iPhone from its inventory count, labelled it with a shipment tracker and returned the tracker to the token. It would be absurd to use blockchain like a cloud platform and outright impossible thanks to the atomic nature of blockchain transactions.

更好的方式是，在线零售商获得集成点，物流服务兑换token，它将允许仓库找到产品，用它自己的方式标记，通知用户产品已经准备好运输（token带有定义允许持有人进行什么通信），并且发货。
Preferably instead, the online retailer obtained a point of integration - the shipment token, which will allow the warehouse to find the product, label it at its own pace, inform the user that the product is ready to be shipped (the token carries the definition of what communication is allowed to the holder), and send it on its way.

随着业务的成熟和市场的摩擦减少，两种变化都会发生。

As the business matures and markets become less frictional, two changes happen.

### 业务流程的变化
### Change in the business process

第一个变化是在线零售商找到了一家更好的货运公司。 在这种情况下，新的货运公司将整合相同的物流服务兑换token，发送货运进度信息代替旧的货运进度信息。 客户仍然可以使用他的token证明运输的所有权，例如 通过使用NFC手机接触送货员的手持设备。
The first change is that the online retailer found a better shipment company. In this case, the new shipment company will integrate the same shipment token, sending shipping progress information in place of the old one. The customers can still prove ownership of the shipping with his token, e.g. by using an NFC mobile phone to touch the deliverer's hand-held device.

无需更改智能合约交易规则。 当产品无法在首次完全交付在线零售商甚至可以更改运输公司而无需用户更改其token。
There is no need to change the smart contract transaction rules. The online retailer can even change the shipping company when the product is first under-delivered without the user changing his token.

此更改说明业务流程应与token分离，并且通过token集成。
This change illustrated that the business process should decouple from the token, instead, integrated through the token.

### 市场变化
### Change in the market

生意持续了一段时间，伴随区块链市场有一项创新，一些用户从从运输公司批量购买了一年的运输服务，以享受AmazonPrime般的免费送货特权而无需使用亚马逊（最后一公里）。看到机会，信用卡公司甚至为他们的卡的订户提供了这样的特权，这也将是一个代表。
Business went on for a while; then, there is an innovation from the blockchain market. Some users bulk-purchased a year's shipping from a delivery company, to enjoy the AmazonPrime-like free shipping privileges without using Amazon[^last-mile-market]. Seeing an opportunity, a credit card company even went so far as to provide such a privilege to the subscribers of their card, which is also represented by a toke.
[^ 最后一公里市场]：这种创新的市场是可能存在的，因为只有买方最熟悉最后一英里的交付体验。通常，在线零售商通过谈判获得比买家更高的批量交付折扣，但它们只是买家体验的代表。 他们的关注点并不完全与买家保持一致。一个买主开车30分钟去取包裹这个折扣和她的时间并不匹配。送货公司还可以比在线零售商更好的优化工程，例如，通过请求访问买家的日历，在线零售商并不能安全做这件事。最终，通过买方和交付公司之间的协作，可以创造更多价值。
[^last-mile-market]: The market condition for such an innovation might exist, because only the buyer is most familiar with the last-mile delivery experience. Usually, an online retailer negotiates a higher bulk delivery discount than their buyers could, but they are just a proxy of the buyers' experience. Their interest is not perfectly aligned with the buyers. A buyer driving 30 minutes to pick up a parcel knows that the discount is no match for her time. The delivery company can also optimise the process better than the online retailer, for example, by requesting access to the buyer's calendar, which the online retailer couldn't do safely. Ultimately, more value can be created with the collaboration between buyer and the delivery company.

在线零售商决定加入其中以保持竞争力。 这一次，他需要修改他的智能合约，更改交易规则，即在购买时可以接受交货token。 在这种情况下，交易的输出将没有交货token，因为已经提供了一个。[^可替代的物流服务兑换token]
The online retailer decided to join the game to stay competitive. This time, he would need to modify his smart contract, changing the transaction rule that a shipping token can be accepted at the time of purchase. In such a case, the output of the transaction will not have a shipping token, since one is already provided.[^fungible-shipping-token]

[^可替代的物流服务兑换token]：在实际实施中，批量购买的运输标签，如果被Tokenisation话，可能会也可能不会被用作运输token。 物流服务兑换token可以设计为半可替代的token，而运输token必须是不可替代的，每个都映射到特定的包裹。 本文的作者为了清晰起见，决定省略这样的实现细节。
[^fungible-shipping-token]: In practical implementations, bulk-purchased shipping labels, if tokenised, may or may not be used as shipment tokens. Shipping labels can be designed as a semi-fungible token, while the shipment token must be non-fungible, each mapped to a specific parcel. The authors of this paper decided to leave out such implementation detail for clarity.

在线零售商必须修改他的业务流程，以期望用户购买的物流服务兑换token支持任何交付公司提取货物。
The online retailer will necessarily modify his business process to expect pick-ups from any delivery company the user purchased shipping tokens from.

此更改说明新的交易规则将导致智能合约的更改。
This change illustrated that a new transaction rule would result in a change of smart contract.

### 业务流程可能不会改变智能合约。 市场可能会。
### Business processes may not change smart contract. Market condition may.

总而言之，业务流程变更不应导致智能合约变更。 以交易规则变化的形式改善自由市场自然应该导致智能合约的变化。 区块链用于提供完全市场，而不是优化业务流程。
To recap, business process changes should not lead to a smart contract change. An improvement in a free market, in the form of a transaction rule change, should naturally lead to a smart contract change. Blockchain serves to provide a frictionless market, not to optimise business processes.

通过Tokenscript实现这一愿景。 没有它，就很难将集成需求和业务流程需求明确分开，结果将无法实现互操作。
This vision is made possible through Tokenscript. Without which the clear separation of integration needs and business process needs would be difficult and the result would be not interoperable.

在第一种情况下，Tokenscript描述了能够接收消息的物流服务兑换token。 在简化形式中，将消息委托并呈现给用户界面
In the first case, Tokenscript described a shipping token to be able to receive messages. In the simplist form, the message is entrusted and rendered to the user interface

我们将演示与消息传递相关的Tokenscript部分。
We will demonstrate the portion of Tokenscript related to messaging.

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

'`<states> ... </ states>`之间的部分给出了状态列表，这是定义允许token持有者接收的消息的基础。
The section between `<states>...</states>` gives a list of states which is the basis of defining messages the token holder is allowed to receive.

第一个`<trust> ... </ trust>`结构使得用户代理接受并显示来自token发行者的任何签名消息，在这种情况下是在线零售商，展示通知和消息历史记录中的条目，当token的状态是已经被初始化的时候。
The first `<trust>...</trust>` structure causes the user agent to accept and display any signed messages from the token issuer, in this case the online retailer, as notification and an entry in message history, when the token's state is initialised.

第二个`<trust> ... </ trust>`结构使用户代理接受并显示任何签名消息，其签名验证密钥由token的颁发者证明，展示通知和消息历史记录中的条目， 当token的状态是dispatched时。 这有效地允许token发行者明确信任的任何实体以“dispatched”状态发出消息。
The second `<trust>...</trust>` structure causes the user agent to accept and display any signed messages, whose signing verification key is certified by the issuer of the token, as notification and as an entry in message history, when the token's state is "dispatched". This effectively allows any entity the token issuer explicitly trust to issue a message at "dispatched" state.

当在线零售商更改其递送公司时，零售商可以在新递送公司的公钥上颁发证书，从而授权他们向令牌持有者（买家）发送消息以更新他们的递送状态，同时将消息限制为，只有业务流程的某些阶段才能发送。

When the online retailer changes his delivery company, the retailer could issue a certificate on the public key of the new delivery company, thereby authorising them to send messages to the token holders (buyers) to update them the delivery status, yet restricting the messages to only certain stages of business process.

此代码片段表明，通过提供这种灵活性，Tokenscript连接到新的业务流程，而无需更改智能合约或影响用户体验。 它还允许与token持有者进行通信，而无需通过智能合约发送消息。
This code snippet shows that by giving such flexibility Tokenscript connected to a new business process without requiring change in the smart contract or affecting user experience. It also allowed communication to the token holder without sending messages through smart contracts.

实际通信的方法保持开放以由区块链技术的其他层实现，例如消息队列或甚至分布式消息队列。
The method of actual communication is left open to be implemented by other layers of blockchain technology like a message queue or even a distributed message queue.

值得注意的是，消息传递并不是与业务流程相关的唯一部分。 我们将在“Web集成”一章中解释更广泛的集成范围。
It's worth noting that messaging is not the only part connected to the business process. We will explain a broader scope of integration in the "Web integration" chapter.

还可以以这样的方式编写Tokenscript，即只有来自在线零售商的消息被信任和显示，因此，任何新的递送公司必须将其递送状态消息发送到在线零售商的系统以转发给买方。 由于可用性和隐私原因这可能不是一个好主意。 例如，当在线零售商离线时，交付公司应该能够运营; 用户可能会将门入口密码发送给在线零售商而不是递送公司。

It's also possible to write Tokenscript in such a way that only messages from the online retailer is trusted and displayed, therefore, any new delivery company must send their delivery status message to the online retailer's systems to be forwarded to the buyer. There are availability and privacy reasons why this may not be a good idea. For example, a delivery company should be able to operate when the online retailer is offline; the user might send the door entrance passcode to the delivery company which the online retailer should not learn.

##  token的种类
##  Types of tokens

自2018年以来，以太坊社区大致将token分类为可替代的和不可替代的token。
Since 2018, Ethereum community has roughly categorised tokens as fungible tokens and non-fungible tokens.

虚拟token是指具有余额的类似货币的token，通常在ERC20中实现，但在实践中，诸如预授权和设置状态通道之类的货币功能需要比典型的ERC20更丰富的功能。
Fungible tokens refer to the currency-like token with a balance, typically implemented in ERC20, although in practice currency functions like pre-authorisation and setting up of state channel requires richer functions than typical ERC20.

不可替代的token是指加密小猫，通常每个token有一个单位。
Non-fungible tokens refer to crypto-kittens and typically have one unit per token.

分类并未包含我们可能的所有token，并且在某些情况下可能会重复。 以我们之前演示的1％的房产token为例，每个这样的token都可以与同一发行人为同一财产发行的另一个token互换。 也许除了华人社区通常会高估序列号为88的token，但如果我们允许任何百分比数字被Tokenisation，比如允许购买0.88％，那么序列号将被重构。 同样，使相同属性的每个部分所有权token都可以完全互换。 然而，显然，财产A的所有权百分比和财产B的所有权百分比彼此不可互换。
The categorisation isn't capturing the full spectrum of the tokens we could and may overlap in some cases. Taking the 1% per cent property token we demonstrated earlier as an example, each of such token is fungible with another issued by the same issuer for the same property. Maybe with the exception of the Chinese community which usually overvalue the token with a sequence number of 88, but if we allow any percentage number to be tokenised, say, allowing one to purchase 0.88%, then the sequence number will be refactored out of the way too, making each partial ownership token of the same property strictly fungible. However, apparently, a percentage of ownership of property A  and a percentage of ownership of property B are not fungible with each other.

本文重新介绍了证明的概念 - 它已存在数十年但尚未得到充分利用。 从那里开始，本文将标记分类为“区块链token”和“证明”。 前者包括可互换和不可替代的token。 后面的类型“证明”将在这里解释。
This paper re-introduces the concept of attestations - it has been there for decades but wasn't fully utilized. From there, this paper categorises tokens as "blockchain token" and "attestation". The former type includes both fungible and non-fungible tokens. The latter type "attestation" will be explained here.

## 证明
## Attestations

凭证是一种用于证明某个主题加密签名的消息， - 某人，某个token或其他证明。 由于它是特定于某主题的凭证，因此它不能在区块链上自行转移。
Attestation is a cryptographically signed message testifying something on a subject - a person, a token, or another attestation. Since it is specific to that subject being attested, it is not transferrable on its own on the blockchain.

在我们之前的汽车所有权token示例中，汽车所有权token将是区块链token，其中可以应用典型的买入，卖出和转移规则。 但是，它上面的保险toen不是区块链token。 如果保险是强制性的，则是对该车的认证，因此不能自行转让。 如果保险是全面的，它是对汽车和司机的凭证，即使汽车被转移也不能无缝转移。
In our previous car ownership token example, the car ownership token would be a blockchain token, where the typical buy, sell and transfer rules can apply. The insurance token on it, however, is not a blockchain token. If the insurance is compulsory, it is an attestation on that car, therefore cannot be transferred on its own. If the insurance is comprehensive, it is an attestation on the car and the driver, and cannot be seamlessly transferred even if the car is transferred.

如果凭证不可转让，那为什么它必须在区块链上吗？ 答案是否定的。
If an attestation is not transferable, then why does it have to be on the blockchain? The answer is it doesn't.

以个人身份证明为例。 除非它被用于区块链交易或由于某种原因而被撤销，否则它没有理由对像公共以太坊这样的区块链进行任何追踪。 它们仍然是用户钱包中的一个项目，因为它们可能需要延长，由于个人身份的变化而重新证明或者用于登录服务，比如爱沙尼亚电子居住证明可用于登录网页服务。
Take a person identity attestation for example. Unless it is used for a blockchain transaction or revoked for some reason, there is no reason that it should have any trace on blockchains like public Ethereum. They are, still, an item in the user's wallet, since they might need to be prolonged, re-attested due to change of a person's identity or used to login to services the same way Estonian e-residency attestation can be used to login to web services.

凭证可能会影响交易。 例如，VIP会员可享受10％的服务折扣 - 此类商业规则要求VIP会员证明用于加密货币交易以购买服务。 Holden Capped Car服务的证明有效期为5年，允许汽车在到期前将账单上限到一定金额。
An attestation can affect transactions. For example, a VIP member can enjoy a 10% discount on services - such business rule would require a VIP member attestation to be used for the cryptocurrency transaction for purchasing the service. An attestation of Holden Capped Car services, which is valid for 5 years, allow the car to be serviced with the bill capped to a certain amount before its expiry.

有时，凭证决定了交易可能发生的事情。
Sometimes, an attestation dictates what transactions can happen.

作为* The Economist *的订阅者，我承诺在每个发行时付费。 这是通过我发送预授权从我的以太坊帐户中每两周提取一次订阅费来完成的。 这种预授权将是 Economist 钱包中的证明，它提供了 Economist 可以每两周使用一次 “charge” 行动。
As a subscriber of *The Economist*, I commit to paying for each issue as they are published. This is done by me sending a pre-authorisation to withdraw a subscription fee bi-weekly from my Ethereum account. Such a pre-authorisation would be an attestation in the wallet of The Economist, which provides a "charge" action that The Economist could use bi-weekly.

出于隐私原因或为了打击可联系性（通过公开使用此类证明来确定证明）的考虑，交易中使用的证明与位于用户钱包中的证明的形式不同。 本文的作者在另一篇论文[引用]中讨论了这个问题。

For privacy reasons, or to combat linkability (the subject of an attestation being identified by the public use of such an attestation), the attestation used in transactions is of a different form than the one that lies in a user's wallet. The authors of this paper addressed this issue in another paper [cite].

在前面的所有示例中，凭证只在事务需要时留下痕迹。有些情况下，证明在创建或撤销时会在区块链上留下痕迹。
In all of the previous examples, attestations only leave traces when a transaction needs it. There are cases when attestations leave traces on the blockchain when they are created, or revoked.

为了解释必须在区块链或区块链跟踪上发出*颁发证明*的用例，以飞机引擎为例，具有巨大的转售价值，该引擎的修理情况，以证明的形式，显著影响着估值。 这种证明存在于卖方的钱包中，但是每当发动机进行维护时，飞机服务提供商必须添加这种凭证的散列。 如果没有提供与区块链记录匹配的证明，买家将不会购买。
To explain the use case where the *issuing* of attestation has to happen on the blockchain or with blockchain trace, take the aeroplane engine for example, with a substantial resale value, the repair facts of this engine, in the form of attestations, affects valuation significantly. Such attestations are in the seller's wallet, but an aeroplane service provider must add a hash of such an attestation each time the engine undergoes maintenance. The buyers would not purchase if they are not presented with these attestations that match the blockchain records.

为了解释在区块链上必须发生凭证的*撤销*时的案例，让我们来看看一个名为FIFA票证的凭证。 由活动组织者发布，它证明了所有者进入场地的权利，通常是在用户付款或赠送门票之后。 假设90％的门票都是使用非加密货币购买的，因此这些门票不会对区块链进行跟踪。 但是，如果票证所有者决定按照相应的智能合约规则在区块链上出售他的票证，则票证必须用作此类交易的输入并被视为已消耗，而代表相同权利的区块链令牌将被创建并且成交。 本文的写作在2018年中期组织了一次FIFA门票实验来测试这些概念，在内部我们将这种认证称为“一个可产生的”，因为它的使用产生了一个区块链token。 该实验的细节可以在另一篇论文[引用]中找到。
To explain the use case when the *revocation* of an attestation has to happen on the blockchain, let's consider an attestation called FIFA ticket.  Issued by the event's organiser, it attests the owner's right to enter the venue, usually after the user has paid or was gifted the ticket. Let's assume 90% of the tickets are purchased with non-crypto currency, therefore these tickets would not have a trace on the blockchain. However, if a ticket's owner decides to sell his tickets on the blockchain following the corresponding smart contract rules, the ticket has to be used as the input of such a transaction and considered consumed, while a blockchain token representing the same entitlement would be created and traded. The writes of this paper organised a FIFA ticket experiment in mid-2018 to test the concepts, and internally we call such an attestation "a spawnable" as its use spawns a blockchain token. The detail of that experiment can be found in another paper [cite].

# Tokenscript的组件
# The components of Tokenscript

## 行动
## Actions

我们将Tokenscript的渲染部分和可操作部分分开。 操作引用您可以使用token执行的操作。 通常有：
We seperate the rendering portion of Tokenscript and the actionable portion. Action refer the things you can do with a token. There are generally either:

 - 使用token访问Web服务
 - 使用token控制物联网设备
 - 使用token进行交易。
- Use the token to access to a web service
- Use the token to control IOT devices
- Transacte with the token.

这些操作的所有示例都可以在第一章的汽车示例中找到。 例如：
All examples of these actions can be found in the car example in the first chapter. For example:

汽车token的动作：

Car token's actions:

开锁
：token具有足够的凭据信息来回答来自汽车的质询 - 响应，以便在离线时解锁。
Unlock
:   The token has enough credential information to answer a challenge-response from a car in order to unlock it while offline.

授权
：用户还可以授权其他人使用它，发送授权（这是证明 - 参见证明章节）就像发送即时消息一样简单。
Authorise
:   The user can also authorise another person to use it, sending an authorisation (which is an attestation - see Attestation chapter) as easy as sending an instant message.

借
：授权和出借之间的区别是后者还要授权借款人使用Holden Capped Service并打开车库门。
Lend
:   The difference between authorising and lending is the latter also authorises the borrower to use Holden Capped Service and to open the garage gate.

Holden Capped Service token 的操作

Holden Capped Service token's actions

预订服务
：此token允许用户登录任何holden服务中心并预约。
Book a service
:   This token allows the user to login to any holden service center and book an appointment.
报到
：他进一步使用此token进入服务站（刷他的手机进入门）。
Check-in
:   He further uses this token to enter the service station (swipe his mobile to enter the sliding gate).

支付
：通过在交易中包含Holden Capped Service令牌，服务成本可以通过预付款或POS在网络上设置上限。
Pay
:   By including the Holden Capped Service token in a transaction, the service cost is capped, either on the web through pre-pay or on the POS.

并非所有操作都由token提供。典型：
Not all actions are provided by the token. Typically:

转移
由通用token的Tokenscript提供。你可以想象，例如ERC721的Tokenscript文件允许传输任何符合标记的token，并且汽车token可能是其中之一。 实际上很难出现这种情况，因为汽车代币的交易规则通常需要证明，例如买方是进行此类交易的法定年龄，但即使在这种情况下，规则也可能由规范汽车贸易的Tokenscript提供。。
Transfer
:   Provided by a generic token's Tokenscript. You can imagine for example the Tokenscript file of ERC721 allows any conforming tokens to be transferred, and the car token might be one of them. In reality it can hardly be the case because car token's transaction rules usually require attestations, such as the buyer is of the legal age to conduct such a transaction, but even in such cases, the rule might be supplied by a Tokenscript regulating the car trade.

拍卖
由拍卖市场提供。 当用户访问拍卖市场时，使用允许token登录网站的相同机制，用户的代理（钱包）将显示可以享受拍卖服务的token列表。 如果用户信任拍卖市场，则可以将其操作添加到所有支持的token。
Auction
:   Provided by an auction market. When the user accesses an auction market, using the same mechanism that allows a token to login to a website, the user's agent (wallet) would show a list of tokens that can enjoy the auction service. If the user trusts the auction market, she can then add its action to all of the supported tokens.

分享清单
：一家初创公司，我们称之为CarNextDoor，提供管理流程，以便车主可以安全地列出汽车进行分享并自动获得收入。 一旦列出，车主将获得一个上市token，并且必须通过它预订,来使用自己的车。 作为交换，当他不使用它时，汽车会外借并为他赚钱。 当然，这个动作是由CarNextDoor提供的，而不是由Holden提供的。
List for sharing
:   A startup company, let's call it CarNextDoor, offers to manage the process so the car owners can safely list the car for sharing and automatically gets income. Once listed, the car owner will obtain a listing token and has to book his use of his own car through it. In exchange, when he is not using it, the car goes out and earn money for him. Naturally, the action is provided by CarNextDoor, not by Holden.

## 魔术链接

魔术链接只是特定资产上操作的快捷方式。 它通常发送给资产所有者。 它带有事务所需的证明（例如原子交换）。
## Magic links

Magic links are simply a shortcut to an action on a specific asset. It's usually sent to the owner of the asset. It comes with required attestations for a transaction (e.g. an atomic swap).


## 凭据
证明就像token，除了它们不可转让，如果智能合约允许转让，原始证明在转让后无效。这使得友谊之类的东西可以以类似于token的方式定义，因此，我们也可以将这些证明称为“token”。友谊的象征将是来自某人的签名消息，将其他人视为朋友，并且它将成为Tokenscript术语中的资产。显然，迈克尔·杰克逊的友谊的象征可能具有很高的价值，特别是因为他不能再生产这些代币，但即使像“weiwu之友”这样的卑微的代币也具有一定的价值。例如，它允许weiwu的一个朋友为他签署一张收货单，或者允许这样的朋友在weiwu练习道场中成为队友。甚至有一个巧妙的伎俩，通过使用秘密共享协议，拥有威武的友情令牌可以让人们知道与weiwu一样的共同还有。请注意，此定义不要求资产是区块链token，也不要求它甚至存在于区块链中。更多内容将在后一章“凭据”中阐述。

## Attestations

Attestations are like Tokens except that they are not transferable, in the case that a smart contract allows them to be transferred, the original attestation is render invalid after the transfer.  This makes it possible for things like friendship to be defined in a way similar to the token, and therefore, we may as well call such attestations "tokens". A token of friendship would be a signed message from someone, recognising someone else as a friend, and it would be an asset in Tokenscript terminology. Apparently a token of friendship from Michael Jackson can be of high value, especially since he cannot produce any more of these tokens, but even a humble token like "Friend of Weiwu" has some value. It, for example, allows a friend of Weiwu to sign a delivery recipt for him, or allows such a friend to get a mate-rate for signing up in the same dojo Weiwu practises in. There is even a neat trick, which, by using secret sharing protocols, having Weiwu's friendship token allows one to learn common friends shared with Weiwu. Notice that this definition does not require the asset to be a blockchain token, nor that it even exists on the blockchain. More on that in the latter chapter "attestation".

Assets and attestations (tokens in general) can have financial value and utility value.

## 资产

在Tokenscript术语中，资产是可以拥有并具有价值的东西。 这是一个广义的定义，并不像金融资产那样要求资产产生回报或预期回报。

资产示例：加密小猫，国际足联门票，一瓶葡萄酒，1％房屋所有权，视频游戏中的盔甲或视频游戏中的骰子。

证明的例子：加密猫代金券，国际足联门票兑换优惠券，美国运通百夫长身份，友谊代币（迈克尔杰克逊的签名消息说Victor Zhang是朋友）或身份证明。
## Assets

In Tokenscript terminology, an asset is something that can be owned and has value. This is a broad definition and doesn't require, like the financial assets, that an asset produces a return, or is anticipated to.

Examples of assets: crypto kitties, FIFA tickets, right to a bottle of wine, 1% ownership of a house, a piece of armour in a video game or dice in a video game.

Examples of attestations: crypto-kitten vouchers, FIFA ticket redeem coupons, American Express Centurion status, Friendship Tokens (a signed message from Michael Jackson saying that Victor Zhang is a friend) or proof of identity.


# 加入游戏

将Tokenscript定义为规范的工作正在进行中。 我们的目标是制作关键方法和考虑因素的黄皮书，并从那里开始扩展它。 当您阅读本草案时，更多的协作方法正在付诸实施。 目前，联系人是：

# Join the game
The work to define Tokenscript as a specification is a work in progress. We aim to produce a yellow paper of the key methods and considerations and extend it from there. More methods of collaborations are being put to work as you read this draft. For now, the contact points are:

weiwu.zhang@alphawallet.com
james.sangalli@alphawallet.com
victor.zhang@alphawallet.com
