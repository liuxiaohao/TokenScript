# TokenScript
# TokenScript

TokenScript 制作 SmartTokens （感谢[Virgil Griffith]（https://twitter.com/virgilgr）提出“SmartToken”这个名称)。这些类似于传统ERC20或ERC721 tokens，但是具有可扩展的结构和经过签名的JavaScript，以实现以前DApps难以实现的丰富功能，并通过灵活的自定义交易规则进行交易。
TokenScript makes SmartTokens (Credit to [Virgil Griffith](https://twitter.com/virgilgr) for coming up with the name ‘SmartToken’). These are like traditional ERC20 or ERC721 tokens but with extendable structure and signed JavaScript to go with it to realise rich functions that previously DApps struggle to implement, and be traded with flexible, customized trading rules.

一个TokenScript的文件由两部分组成 a）JavaScriptr让token在用户的钱包中工作或者跨多个应用程序工作; b）XML数据以提取token 的状态和值。
A TokenScript file is made of a) JavaScript to make Token work in the user's wallet or across multiple apps and b) XML data to extract status and value of the token.

简而言之，它就像是令牌的前端。
In short, it's like a front-end for tokens.

## 难道我们还没有token的前端吗？
## Don't we already have a front-end for tokens?

是的，它叫做DApp网站。 但它不便携并且不安全。
Yes, it's called DApp websites. But it's not portable and secure.

用户想要使用该token执行的所有操作都需要在DApp网站上完成，则该token对其他DApp不是很有用。 人们习惯于削减token功能，将其用于ERC20或ERC721,以便携带。
If everything the user wanted to do with that token is done on a DApp website, that token isn't very useful on other DApps. People used to cut out token functions, shoe-horn it to ERC20 or ERC721 to make it portable.

token的TokenScript就像使token的dapp可移植并可在多个DApp上使用。 它进一步使用沙盒和代码签名模型来保护它。
TokenScript of a token is like making the dapp of the token_ portable and usable across multiple DApps. It further secures it with a sandboxed and code signed model.

[TokenScript设计论文]（https://github.com/AlphaWallet/TokenScript/releases）概述了为什么TokenScript必须可移植才能Tokenisation。 设计论文的作者认为，在没有Tokenisation的情况下使用区块链没有任何实际的好处。
The [TokenScript design paper](https://github.com/AlphaWallet/TokenScript/releases) outlines why TokenScript has to be portable for Tokenisation. The authors of the design paper holds that there is no tangible benefit of using blockchain without tokenisation.

## 如何创建和使用TokenScript？
## How is TokenScript created and used?

TokenScript通常由token的建模者创建，该建模者构建指示token交易规则的基础智能合约。 

A TokenScript is typically created by the token's modeler, the team which builds the underlying smart contracts dictating the token's transaction rules.

当用户使用时（通过用户代理，例如Dapp浏览器），Tokenscript可视地呈现token并提供与token相关的交易的可靠组装。 
When used by a user (through user-agent, e.g. a DApp browser) TokenScript visually renders the token and provides trustworthy assembling of transactions related to the token.

当dapp开发人员使用TokenScript时，TokenScript允许Dapp与其接口交互，而不是直接访问智能合约，因此可以独立于其支持的所有token升级Dapp。
When used by a DApp developer, TokenScript allows a DApp to interact with its interface instead of directly accessing smart contracts, so that the DApp can be upgraded independently of all the tokens it supports.

当市场或任何其他token相关服务（例如拍卖或抵押）使用时，它允许token被正确地呈现和签名以与这些服务一起使用。 
When used by a market or any other token related service (e.g. an auction or collateralisation), it allows the token to be correctly rendered and signed for use with these services.

## TokenScript文件中有什么？

## What's in a TokenScript file?

Tokenscript是一种XML方言。 它描述了token提供的功能（通过智能合约与否），在用户界面上呈现它的方法，它使用的ERC toekn行为模板 以及javascrip来构造token所需的交易和呈现。它还定义了如何使用证明来修饰，转换或验证交易。
TokenScript is an XML dialect. It describes the functions provided by the token (through smart contract or not), the method to render it on the user's interface, the ERCs token behaviour templates it uses and the JavaScript needed to construct transactions and render the token. It also defines how attestations are used to decorate, or convert to, or validate a transaction.

## 为什么是 Tokenscript
## Why TokenScript?

今天，访问，呈现和交易的令牌方式分散在Dapps和Smart Contracts中。 这限制了令牌的使用。
Today, the way tokens are accessed, rendered and transacted are scattered across DApps and Smart Contracts. This limited the use of Tokens.

通常 ，所有关于一个token的知识都在dapp中，那么dapp必须参与该token的市场和所有集成，重建数据并提供互操作性，安全性和可用性 - 同样的问题在区块链发明之前就已出现，并阻碍了tokenisation。
Typically, all knowledge about rendering a token and constructing a transaction about the token is in a "host" web app. The "host" web app becomes a centre in the token's marketisation and integration, recreating data interoperability, security and availability barrier - precisely the same set of issues that prevented tokenisation before blockchain's invention.

通过将包括智能合约接口在内的token知识输出并将其放入便携式Tokenscript中，我们允许token可访问且有用。 
By taking the knowledge of tokens including smart contract interfaces out and put them into a portable TokenScript we allow tokens to be accessible and useful.

## TokenScript 项目介绍
## TokenScript Project introduction

TokenScript项目是一项旨在设计，推进Tokenscript和培育Tokenscript使用的计划。
The TokenScript project is an initiative to design, progress TokenScript and nurture the use of TokenScript.

# Git repo
# Git repo

这个项目包括 
This project holds:

doc：
关于语言和设计的文档
doc
:   documents about the language and the design

lib/browser
:
Tokenscript的浏览器插件支持
lib/browser
:   browser plugin-support of TokenScript

lib/web
: 在dapp-browser环境下下，Dapps的库可以呈现token 但不支持Tokenscript。 某些功能不可用需要底层（例如，切换节点或访问不同的链）的dapp浏览器支持。
lib/web
:    library for DApps to render tokens in the case the DApp-browser does not support TokenScript. Some features are not available (e.g. switching nodes or accessing multiple Plasma Chain) as they require underlying DApp browser support.

# 试用TokenScript
# Trying out TokenScript


加入我们的电报群<https://t.me/AlphaWalletGroup>， 要求“使用TokenScript进行一个Admission Ticket Token示例”。 告诉我们您的以太坊地址，以便我们向您发送令牌。
Join our Telegram group <https://t.me/AlphaWalletGroup> and ask for "an example Admission Ticket Token to play with TokenScript". Tell us your Ethereum address so we can send you a token.

对于iOS：
For iOS:

1. 访问<https://testflight.apple.com/join/aHUxcsro>安装TestFlight版本
1. Install the TestFlight build by visiting <https://testflight.apple.com/join/aHUxcsro>
2.在AlphaWallet应用程序中，转到设置（最后一个选项卡）>`启用网络'，然后点击`Ropsten（test）`启用它。 点击“完成”
2. In the AlphaWallet app, go to Settings (last tab) > `Enabled Networks` and tap `Ropsten (test)` to enable it. Tap `Done`
3.在AlphaWallet应用程序中，转到Wallet（第一个选项卡）并点击“+”按钮并粘贴合约地址“0x0C8D487DD27D7c4A027D9f92915659139e0b2FF2”以使钱包显示应该已转移给您的token
3. In the AlphaWallet app, go to Wallet (first tab) and tap the `+` button and paste the contract address `0x0C8D487DD27D7c4A027D9f92915659139e0b2FF2` to make the wallet display the token which should have been transferred to you
4. 访问我们的库<https://github.com/AlphaWallet/TokenScript/tree/master/examples/ticket>和 把文件`AdmissionTicket.xml`，`token.en.shtml`，`shared.css 从你的Mac到你的iPhone的`和`enter.en.shtml`, 从你的Mac AirDrop到你的iPhone中。如果您可以访问移动版Safari中的文件，也可以从iOS共享菜单中选择“在AlphaWallet中打开”

4. Go to our repository at <https://github.com/AlphaWallet/TokenScript/tree/master/examples/ticket> and AirDrop the files `AdmissionTicket.xml`, `token.en.shtml`, `shared.css` and `enter.en.shtml` from your Mac to your iPhone. If you have access to the files in mobile Safari, you can also choose to "Open in AlphaWallet" from the iOS share menu
In the AlphaWallet app, go to Wallet tab and tap on the token "Admission Ticket Token (DAT2)"

5. 在AlphaWallet应用程序中，检查TokenScript文件列表的Settings选项卡> TokenScript Overrides。 滑动即可删除或点按即可分享。 您可以将文件AirDrop到另一台安装了AlphaWallet TestFlight的iPhone
5. In the AlphaWallet app, check the Settings tab > `TokenScript Overrides` for the list of TokenScript files. Swipe to delete or tap to share. You can AirDrop the files to another iPhone which has AlphaWallet TestFlight installed
