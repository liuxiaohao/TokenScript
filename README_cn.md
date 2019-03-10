# Tokenscript
Tokenscript是tokenisation的编程接口
Tokenscript is a program interface for tokenisation.

token的建模者，通常是智能合约的作者，制定token的交易规则，写入tokenscript并且签名
A token's modeler, typically the author of smart contracts dictating
the token's transaciton rules, writes tokenscript and signs it.

Dapp浏览器和Web应用程序（在以太坊中称为Dapp）
利用这样一个签名的Tokenscript来直观地呈现token和提供有关token的可信交易
Both a Dapp browser and a web application (called Dapp in Ethereum)
make use of such a signed Tokenscript to visually render the token and
provide trustworthy signed transactions about the token.

## 为什么是 Tokenscript
## Why Tokenscript?
如今，访问、呈现和交易的token的方式分散在Dapps和智能合约中。 如果所有关于一个token的知识都在dapp中，那么dapp必须参与该token的市场和所有集成，重建数据并提供互操作性，安全性和可用性 - 同样的问题在区块链发明之前就已出现，并阻碍了tokenisation。
Today, the way tokens are accessed, rendered and transacted are scattered across Dapps and Smart Contracts. All knowledge about rendering a token and constructing a transaction about the token, is in a "host" DApp. The "host" DApp becomes a center in the token's marketization and integration, recreating data interoperability, security and availability barrier - exactly the same set of issues that prevented tokenisation before blockchain was invented.

Tokenscript 允许token逻辑和呈现从“主机”中分离出来，允许token轻松便携，并且可以轻松地为其创建市场。
TokenScript allows token logic and rendering to be seperated out of the "host", allows token to be easily portable and market to be easily created for it.

它允许不同的token提供者，不仅可以描述他们的token的特征，还能描述他们如何“行动”，例如，转让。 这个想法的关键在于，token发行者可以随时更新这种标记描述，并追溯已经发行的token的行为。 除了允许不同token提供者之间可以轻松的交互之外，这还消除了在特定类型的token的业务逻辑改变时，更新DApp或智能合约的必要。
It allows different token providers to, not only describe the features of their tokens but also how they are allowed to “act”, e.g. transferability. The crux of the idea is that such a markup description can be updated at any time by the token issuer and retroactively reflect the behaviour of already issued tokens. Besides allowing easy interoperability between different token providers, this also eliminates the need to update the DApp or smart contract whenever the business logic of a particular type of token changes.

## 什么是token script
## What's in a token script

Tokenscript是一种XML方言。 它描述了token提供的功能（通过智能合约与否），在用户界面上呈现它的方法，它使用的ERC toekn行为模板 以及javascrip来构造token所需的事务和呈现。
Tokenscript is a XML dialect. It describes the functions provided by the token (through smart contract or not), the method to render it on the user's interface, the ERCs token behaviour templates it uses and the javascript needed to construct transactions and render the token.

## TokenScript 项目 介绍
## TokenScript Project introduction: 
TokenScript Project，旨在开发和帮助大家更好的使用TokenScript，TokenScript是用于创建和使用加密token（例如区块链token）和DApps的标准标记语言。
TokenScript Project is to develop and help with adoption of TokenScript, the standard markup language for creating and using cryptographic tokens(e.g. blockchain tokens) and DApps.
在2017-2018区块链发生了非常引人注目的投机行为把我们的注意集中到了加密token上。当我们交易时，我们甚至忘记了它们真正的用途; 就像房地产泡沫，一昧的把房屋当作投机资产，忘记了这是居住的地方。为了让区块链提供实际的用途，我们必须了解他对世界经济和互联网的作用。这篇文章的作者是对金融机构和初创公司进行了长期的学习和探索的技术专家。凭借这些经验，我们逐步意识到区块链有两个主要的功能，提供完全市场和 集成网络
The remarkable blockchain speculations that took place in 2017 - 2018 brought everyone's attention to crypto tokens. As we bought and sold them, we forgot their intended purpose was to be used; this is analogous to the housing bubble in which people forgot that houses were not merely speculative assets but rather a place to live. To provide a practical use of the blockchain, we must understand its utility to the world economy and the internet. The people behind this project are technical experts who went through years of study and experimentation into its applications both via financial institutions and startups. With this experience, we recognise the blockchain technology's utility in providing a frictionless market and integrating the web.

尽管2017-2018年发生了很多蠢事，但是这对于token获得一开始的关注并不是坏事。token，作者即将详细阐述的，将是两个主要功能的推动者。我们将定义并实现“token化”的技术。区块链行业共同的努力主要是集中在丰富技术能力上。这篇文章将集中在token化，并且介绍一个称作TBML(token行为标记语言)的标准化工作，它将使区块链技术具备完整的技术堆栈，为经济和互联网提供实用性。
Despite the great folly in 2017-2018, it is not a bad thing to initially focus on tokens. Tokens are the enabler of the two primary functions. We define the technique to make it happen in "Tokenisation". Tokenized rights can be traded on the market and integrated across systems, forming a frictionless market and allowing free integration. Previous efforts in this industry primarily focused on enriching the capacity of the technology. This project will focus on tokenisation and introduce a standardisation effort known as Tokenscript (Token Behaviour Markup Language) which will make the blockchain technical stack complete, providing utility for the economy and the internet.

## Git repo 
## Git repo

这个项目包括
This project holds:

doc：
关于语言和设计的文档
doc
:   documents about the language and the design

lib/brower：
Tokenscript的浏览器插件支持
lib/brower
:   browser plugin-support of Tokenscript
lib/web
在dapp-browser环境下下，Dapps的库可以呈现token
但不支持Tokenscript。 某些功能不可用需要底层（例如，切换节点或访问不同的链）的dapp浏览器支持。
lib/web : library for Dapps to render tokens in the case the dapp-browser does not support Tokenscript. Some features are not available (e.g. switching nodes or accessing multiple Plasma Chain) as they require underlying dapp browser support.


