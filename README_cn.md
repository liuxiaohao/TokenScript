# Tokenscript
TokenScript使用后端的智能合约构建令牌dapp的前端逻辑。
TokenScript builds the front end logic of a token dapp with the smart contract on the backend. 

TokenScript文件包含token的业务逻辑，token UI呈现和程序接口，由token的建模者签名
A TokenScript file contains a token's business logic, token UI rendering and program interface, signed by the token's modeller.

##难道我们还没有token的前端吗？
## Don't we already have a front-end for tokens?

在以太坊中，大多数tokens都有一个Web应用程序，它提供与token相关的所有内容。 我们称之为token_的“Dapp”。
In Ethereum, most tokens have a web application which serves all the content relevant to the token. Let's call it _the "Dapp" of the token_.

如果用户想要在该网站上完成该token所需的一切，那么肯定已经有该token的前端。 但是该token作为区块链token并不是非常有用，因为它不能用于其他Dapps。
If everything the user wanted to do with that token is done on that website, then yes there is already a front-end for that token. But that token isn't very useful as a blockchain token, since it can't be used on other Dapps.

token的TokenScript就像使token的dapp可移植并可在多个dapps中使用。 在这个框架中，一个dapp可以提供与token相关的服务和上下文（例如，你在WoW dapp中有一把剑，还有一把突击步枪）。
TokenScript of a token is like making _the dapp of the token_ portable and usable across multiple dapps. In this framework, a dapp can provide services and context related to the token (e.g. you have one sword in the WoW dapp and an assault rifle in call of duty).

这种区分和分离对于tokenisation很重要 - 这里是[the design paper]（https://github.com/AlphaWallet/TokenScript/releases）中提出的概念。 设计论文的作者认为，如果没有tokenisation，就没有使用区块链的好处。
This distinction and separation is important for tokenisation - a concept addressed in [the design paper](https://github.com/AlphaWallet/TokenScript/releases). The authors of the design paper holds that there is no tangbile benifit of using blockchain without tokenisation.

##如何创建和使用Tokenscript？
## How is a Tokenscript created and used?
TokenScript通常由token的建模者创建，该建模者构建指示token交易规则的基础智能合约。
A TokenScript is typically created by the token's modeler, the team which builds the underlying smart contracts dictating the token's transaction rules.

当用户使用时（通过用户代理，例如Dapp浏览器），Tokenscript可视地呈现token并提供与token相关的交易的可靠组装。
When used by a user (through user-agent, e.g. a Dapp browser) Tokenscript visually renders the token and provides trustworthy assembling of transactions related to the token.

当dapp开发人员使用TokenScript时，TokenScript允许Dapp与其接口交互，而不是直接访问智能合约，因此可以独立于其支持的所有token升级Dapp。
When used by a dapp developer, TokenScript allows a Dapp to interact with its interface instead of directly accessing smart contracts, so that the Dapp can be upgraded independently of all the tokens it supports.

当市场或任何其他token相关服务（例如拍卖或抵押）使用时，它允许token被正确地呈现和签名以与这些服务一起使用。
When used by a market or any other token related service (e.g. an auction or collateralisation), it allows the token to be correctly rendered and signed for use with these services.

## TokenScript文件中有什么？
## What's in a TokenScript file?

Tokenscript是一种XML方言。 它描述了token提供的功能（通过智能合约与否），在用户界面上呈现它的方法，它使用的ERC toekn行为模板 以及javascrip来构造token所需的交易和呈现。它还定义了如何使用证明来修饰，转换或验证交易。
TokenScript is an XML dialect. It describes the functions provided by the token (through smart contract or not), the method to render it on the user's interface, the ERCs token behaviour templates it uses and the javascript needed to construct transactions and render the token. It also defines how attestations are used to decorate, or convert to, or validate a transaction.

## 为什么是 Tokenscript
## Why Tokenscript?

今天，访问，呈现和交易的令牌方式分散在Dapps和Smart Contracts中。 这限制了令牌的使用。
Today, the way tokens are accessed, rendered and transacted are scattered across Dapps and Smart Contracts. This limited the use of Tokens.

通常 ，所有关于一个token的知识都在dapp中，那么dapp必须参与该token的市场和所有集成，重建数据并提供互操作性，安全性和可用性 - 同样的问题在区块链发明之前就已出现，并阻碍了tokenisation。
Typically, all knowledge about rendering a token and constructing a transaction about the token is in a "host" web app. The "host" web app becomes a centre in the token's marketisation and integration, recreating data interoperability, security and availability barrier - precisely the same set of issues that prevented tokenisation before blockchain's invention.

通过将包括智能合约接口在内的token知识输出并将其放入便携式Tokenscript中，我们允许token可访问且有用。
By taking the knowledge of tokens including smart contract interfaces out and put them into a portable Tokenscript we allow tokens to be accessible and useful.

## TokenScript 项目介绍
## TokenScript Project introduction

TokenScript项目是一项旨在设计，推进Tokenscript和培育Tokenscript使用的计划。
The TokenScript project is an initiative to design, progress Tokenscript and nurture the use of Tokenscript.

# Git repo
# Git repo

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
lib/web 
: library for Dapps to render tokens in the case the dapp-browser does not support Tokenscript. Some features are not available (e.g. switching nodes or accessing multiple Plasma Chain) as they require underlying dapp browser support.



