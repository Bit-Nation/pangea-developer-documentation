# **Pangea "dApp Engine" Documentation**
Welcome to the Pangea dApp engine non-technical documentation. This is provided for future developers and users of third-party dApps sold or distributed without charge in our Pangea dApp store, which we expect to have available early Q4, 2018.

#### Index
  1. Introduction
  2. Quickstart
  3. Prerequisites
  4. Tools
  5. Building Smart Contracts
  6. Monetize your dApp! (we should format dApp or dApp in a consistent manner)
  7. VM Functionality
  8. Conclusion
  9. Relevant Links

## 1. Introduction

We provide you a powerful sandbox of an ecosystem. Our SDK and our CLI together let you build and execute powerful decentralized application on our Pangea virtual machine.

As new citizens join Bitnation and create nations (frequently thought of as “communities”) they will require applications to meet their needs efficiently. You will start with our documentation, our templates and our suggestions - but ultimately it is you who will build the million and billion dollar dApps of the future.

#### _Pre-requisites_
For experienced developers, researching the technology necessary to make the best use of our services should be very easy with our document. But for the non-technical reader who hopes to design smart contracts, we have listed out a set of links which will help you wrap your mind around coding in Solidity for the blockchain, even if you’re a beginner.

#### _Tools_
We provide a software development kit, dApp templates and a command line interface to help you build decentralized applications in our system. By incorporating the Truffle migration method we can test and deploy your contracts using npm.

#### _Smart Contracts_ We will be constantly be expanding our foundry of concept smart-contracts for you to rely on in order to expand and improve your decentralized applications. For now, please take a look at our prospective send_to dApp.

#### _Monetize your dApps_
With the potential in the future to reach out to millions of customers, making money in this enterprising new market will be up to your creativity. Why don't you let us show you how we believe the monetization of your app will look.

#### _VM Functionality_
Our virtual machine provides eight functions and four additional subfunctions. These functions let you send Eth, store key values, perform a variety of callbacks, refer to certain addresses and effect the UI. 
                                 
## 2. Quickstart
|  Quickstart Guide  |
| ------------------ |
|  If you've got access to a Linux you can download and install our CLI by inputting npm install pangea-cli -g. |
|  You can download our dApp template at https://github.com/Bit-Nation/dApp-template. Edit the truffle.js or truffle-config.js as well as app.js and their package.json file in order to build your first dApp. |
|  For more information about Truffle, NPM or es2015 please check out the following links: https://truffleframework.com/docs, https://docs.npmjs.com/, https://babeljs.io/docs/en/learn/.

## 3. Prerequisites

##### Programming
If you are going to develop decentralized applications, you must at least know how to write a program.
http://www.programmingbasics.org/en/

##### JS
If you are going to develop in Solidity you need to know a little Javascript first.
(https://www.udemy.com/the-complete-javascript-course/)
(http://www.learn-js.org/)



We may want to recommend the Udemy course as well. It’s far easier to follow than these docs

We may also want to help people learn how to write JavaScript (the book I recommended) as well as the Udemy course on React Native


##### JSON
We regularly make use of .json files, as does Truffle in order to track build artifacts like package.json. 
(https://www.w3schools.com/js/js_json_intro.asp)

##### React Native
Reactive objects are a core feature of modern JavaScript.
(https://www.udemy.com/the-complete-react-native-and-redux-course/)
(http://bit.ly/react-native-redux)

##### Blockchain
If you are going to develop decentralized applications you should understand the underlying blockchain technology it operates upon.
(https://developer.ibm.com/courses/all/blockchain-essentials/)

Blockchain Applications: A Hands-On Approach:
(https://www.amazon.com/Blockchain-Applications-Hands-Arshdeep-Bahga/dp/0996025553)

##### Solidity
You should be familiar with Solidity in order to program smart contracts.
(https://www.udemy.com/best-solidity-tutorial-course-ethereum-blockchain-development/)
 
##### Smart Contracts
It’s worth further considering how to think about designing smart contracts.
(https://blockgeeks.com/guides/smart-contracts/)

## 4. Tools
The three primary tools we provide for you are our SDK, our CLI and our dApp template. These are what allow you to make the best use of our Pangea Virtual Machine.

### _dApp Template_
The dApp template interacts with the Pangea CLI and our SDK. By incorporating Truffle they build into our system smart contract compilation, linking, deployment and binary management. With this handled for you, you only need to write the smart contracts. They also provide a testing framework and asset pipeline to help make your JS assets more manageable.

The dApp Template is a clean slate for users for using our various tools. The developer writes a program in app.js which is renamed according to the project nature (such as send/receive template) and fills out certain metadata about the program under package.json and configures the Truffle config file.

#### Package.json
In your package.json file, you have the opportunity to fill in the metadata of your app. Find the appropriate headings within the program and fill them out: keywords, author, license, dApp name.

#### Truffle.js/Truffle-config.js
Your truffle.js file allows you to exploit the Truffle framework! Check http://truffleframework.com/docs/advanced/configuration for information about how to configure your truffle.js or truffle-config.js file.

#### App.js
This should be where you build your smart contract. Replace the “app” in “app.js” with the name of your dApp! The beginning of the program includes the code,

```import pangea from 'pangea-sdk'
const {
    setOpenHandler,
    newModalUIID,
    renderModal,
    renderMessage,
    setMessageRenderer,
    Modal,
    Container
} = pangea;
```

Do not remove this from the program. However, you will notice a demonstration program after beginning with declaring a class of “demomodal.” This section can be completely replaced with whichever smart contracts you hope to execute on our blockchain.

### _CLI_
A large set of functions are provided by the CLI (“command line interface”) at once provide test nodes and others declare certain functions like setting passwords or certain keys. The CLI is a larger, more complex program flowing out into the SDK to provide certain functions to dApp developers, and from there into the Pangea VM.

To check out how to use our CLI in the terminal, check out:
(https://github.com/Bit-Nation/pangea-cli)

### _SDK_
Our SDK implements the vmprovider.js in order to provide the ether.js javascript library to the Pangea network. The es2015 transpiler allows a user to implement js smart contracts on the Ethereum network and especially within Pangea through the babelrc file in any dApp. This allows the user to apply es2015 functions and objects to their program. Check out the following link to see how best to use es2015 for your project:
(https://babeljs.io/docs/en/learn/)

## 5. Building Smart Contracts
Owing to the current expense of executing a decentralized application on the Ethereum blockchain, we recommend not designing smart contracts or other dApps which exceed 1 meg. Even then, to execute a single megabyte on the Ethereum blockchain costs $37! When you decide to execute a smart contract on the blockchain, a small and efficient little program and certainty on your return-on-investment will be your primary goals.

Over time it is our intention to build a number of basic smart contracts. This is the section you should regularly check for these new contracts. Our first major idea is a simple "send_to" contract. When initiated, the contract will contact a user in a chat and request their relevant wallet address and name. It will then sign the contract with respect to the conditions sent to the user in the chat.

### _Send/Receive Contract_
 Here is an incomplete example of a send/receive contract. Although we still have to build the selection process you can see here a really simple example of how a send_to dApp could be simply built in a single short smart-contract.

Example "Send To" dApp (technically send/receive but simplified to "Send To")

 [Concept] Send To first determines who the "to" is by querying the chat and accepting input from the receiver in the chat; then deploys the "send" order to the specified wallet, drawing funds from the wallet specified by the user.

 [Requirement] "To" function and adding that information under Receiver.

 [Example "To" specification]
[Upon execution] Send to chat "Receiver agrees to receive contract?"
[Upon "yes"] display text "Please input a single word for your name up to 214 characters and your public key and place a space between them and hit enter." Allow user to submit text
[Upon correct (one name, a space, one public key) input] Create class for "user_name" and give it "public_key", then display text "is your name "user_name" and is your public key "public_key? [Y/N]" and wait for input.
[Upon "Y" or "Yes"]
[Upon error] Display text. "Entry invalid. Please try again." and a repeat of the unfulfilled prompt.

 [Example Send contract]
```contract Sender {
function send(address _receiver) payable {
   _receiver.send(msg.value);
 }
}
contract Receiver {
 uint public balance = 0;
 event Receive(uint value);
 function () payable {
   Receive(msg.value);
 }
}
(contract from “https://medium.com/daox/three-methods-to-transfer-funds-in-ethereum-by-means-of-solidity-5719944ed6e9”)
```

### _Concept Smart Contracts_
1. Transfer cryptoassets
  * Send a cryptoasset (like a cryptokitty) to a specified user.
2. Check Inventory
  * Ping Cryptoassets and display privately to user in chat
  * Proves the legitimate existence of the cryptoasset without leaving the chat.
3. Display Inventory
  * Displays cryptoasset inventory to a user in the chat
4. Display Inventory Asset
  * Displays a single asset
5. Escrow
  * Third user approaches two members of a transaction and offers an Escrow contract to both which allows them to store their assets in a third space, reinforcing trust.
6. Auction
  * A user stores a number of items in an escrow or otherwise displays an inventory of records of physical items. The smart contract sends messages to all users allowing them to bid in the auction. It then updates bidders on changes in the prices of their items.
7. Lending
  * A smart contract authorized to make a payment to a lendee, and then on a specified time is authorized to make a payment from the lendee back to the lender.
8. Donation    
  * A smart contract which requests a small, specified donation, such as the cost of the contract plus enough ETH to make another donation request.
9. Join Nation
  * Submits a request to a user to join a nation. The user doesn’t need to visit the nation page to do this if the dApp is written right. Instead, the user will automatically join the nation if they are convinced to respond “yes” to the request.
10. Census
  * dApp queries all Nation members with Census request.
Users agree or decline census.
dApp sends user to third-party app in order to complete the census.

## 6. Monetize your dApp!
 In the future sharding and plasma may reduce the cost of executing a smart contract from $37,000/gig to $37 per gig. Until then, we have to be frugal and find ways to ensure there is always value coming in to cover the expense of executing a smart contract. Here are a few ideas for developers with regards to ways to generate income through dApps.
### _Gambling_
 By writing smart contracts which run simple gambling games, a share of all winnings can be taken by those who host the gambling operation. Nations and cities around the world are able to provide excellent services owing to honest and well-regulated gambling establishments. Software solutions executed on a blockchain will likely be even more transparent and trustworthy for managing gambling. Any nation can permit particular dApps to be the nations’ accepted modes of gambling and in doing so, may work with dApp developers to make large amounts of money.
### _Service Exchange_
 Service exchange platforms like Freelance and Uber provide income for services and hosting the network of service sellers and buyers. dApp developers should find ways to create ecosystems for skills and abilities and for which skilled and knowledgeable people can sell their services either individually or as a holon to customers. In doing so, nations and dApp designers can gain income for business operating with their dApps or within their nations.
### _Digital Assets Buy/Sell Inventories_
 Using the same collector’s rationale as with modern-day antique and collectable stores and shows, dApp developers might find efficient ways to store and display rare cryptoassets. People who amass large amounts of high-value cryptoassets, they could control the price of rare assets and sell them into markets of interested people. These buy/sell relationships may be able to bring in self-sufficient funding for developers and nations.

## 7. VM Functionality
 Our virtual machine provides you eight powerful functions, one of which bears four subfunctions. We will be expanding our Virtual Machine functionality section with clearer descriptions in the near future. Until then, here is a list of the current functions and subfunctions available to you through our virtual machine.
#### _sendETHTransaction_
 sendETHTransaction: global.sendETHTransaction
(should, params, type, chat the chat, payload, cb)
#### _setOpenHandler_
setOpenHandler: global.setOpenHandler
(payload, cb)
#### _setMessageRenderer_
setMessageRenderer: global.setMessageRenderer
(Ethereum address of this pangea user.)
#### _ethereumAddress:_
ethereumAddress: global.ethereumAddress
(amount, callback)
#### newModalUIID
 newModalUIID: global.newModalUIID
(uiID, layout, cb)
#### renderModal
 renderModal: global.renderModal
 (Database (key => value storage))
#### db:
##### db.put
Global.db.put
(key, value, cb)
##### db.has
Global.db.has
(key, value, cb)
##### db.get
Global.db.get
(key, value, cb)
##### db.delete
Global.db.delete
You might deploy this in the following state:
db.delete("the-key-of-the-value", () => { I will be called after deleting}

## 8. Conclusion
Hopefully by the end of this document you have a pretty clear picture about how designing decentralized applications in our Pangea architecture works. As with all new technologies, developing on Pangea means learning new tricks and tools for your trade. But armed with what we’ve given you, you can go out and develop the next million or billion dollar decentralized application. Questions? Feedback? We would love to hear from you at (insert e-mail address here) or on our telegram at (http://telegram.me/bitnation).

## 9. Relevant Links

##### Bitnation
(https://tse.bitnation.co/)
(https://github.com/Bit-Nation/Pangea-Docs)
(https://github.com/Bit-Nation/Pangea-Docs/blob/master/BITNATION%20Pangea%20Whitepaper%202018.pdf)


##### Githubs
###### Pangea CLI
(https://github.com/Bit-Nation/pangea-cli)

###### Pangea SDK
(https://github.com/Bit-Nation/pangea-sdk/)

###### dApp template
(https://github.com/Bit-Nation/dApp-template)

###### Virtual Machine
(https://github.com/Bit-Nation/pangea-sdk/blob/master/src/index.js)


##### NPM
###### What is NPM?
(https://www.npmjs.com/)

###### NPM Documentation
(https://docs.npmjs.com/)

###### Working With
(https://docs.npmjs.com/getting-started/using-a-package.json)

##### Truffle
###### What is Truffle?
(https://truffleframework.com/truffle)
    
###### Truffle Documentation
(https://truffleframework.com/docs)

###### Configure your Truffle File
(https://truffleframework.com/docs/truffle/reference/configuration)


###### Test your dApp
(https://truffleframework.com/docs/truffle/testing/testing-your-contracts)


##### ES2015 
Learn more about ES 2015 Features, Classes, Enhanced Object Literals and more,
(https://babeljs.io/docs/en/learn/)

##### Additional Resources

###### State of the dApps
A collection of decentralized applications, their trading values and the usage statistics.
(https://www.stateofthedApps.com/)

###### Calculating the Cost of a dApp
Information about the cost of running a dApp.
(https://hackernoon.com/ether-purchase-power-df40a38c5a2f)

###### Smart Contract Templates
Academic Information regarding Smart Contract standards.
(https://arxiv.org/pdf/1608.00771)


