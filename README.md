# DAO.Casino Protocol

The objective of Dao.Casino protocol is to enable a sustainable model which benefits all the parties involved in the online gambling business process. (i.e it should be more profitable for the developer to use Dao.Casino protocol, rather than work on its own, and less costly for a casino operator to provide better service for the players. Players should have access to more diverse range of games from independent game developers while having a higher level of security than in traditional online casinos).

**The goal is to allow independent participants: casino operators, developers, players, refferers etc to co-exist and cooperate without trusting each other, and to get rewarded for their contributions**

Single points of failure - processes of value transfer where trusted third party would be required in a conventional online gambling business is replaced by code consistently executed by Ethereum network - a system of smart contracts. These contracts are, simply speaking, just escrows that can be triggered by particular actions performed by the participants and nothing else. 

These actions correspond to the value that the participants add to the ecosystem. When there is no human actors with administrator permissions that can change value distribution processes there is no risk of such actors would become corrupt and make changes in their favour. This consistency of code is a pretty useful feature in the context of gambling business. 
 Security of the system is achieved through transparency, consistency and cryptographic verifiability of software used to automate processes otherwise involving trust, and economic incentive mechanisms for it’s human participants. 
 
 ** Main components of DAO.Casino protocol**
 
 * **Reward System**
 * **Random Generation**
 * **Interoparable Games**
 * **Front-end Platforms** 
 
 
DAO.Casino protocol still has a fee system, but the distribution of fees is a hard coded reward system for all the participants described below. There is no hidden fees. Dao.Casino distributes tokens accumulated by a particular game contract as follows: 

Game Developer - 25%
Casino Operator * - 25% 
Referrer - 25%
Bankroll backers - 25%
 
*Casino operator / platform and a Referrer can be one entity

Despite of Gas cost that is required for Ethereum powered software to run, the fees should remain lower than in traditional server based online gambling. This is because the gas is paid per operation, and only for the operations and storage that is used. 
Game’s front end can be stored either on the server or on the network using decentralised file storage systems such as IPFS or Ethereum’s native Swarm. Using Swarm will also allow to program the game to pay for it’s own front-end storage.

### Dao.Casino Protocol Goals:

* Remove the need in a trusted party in all aspects of online gambling industry, therefore:
* Reduce operational costs of online gambling therefore provide higher payouts
* Reduce a risk of fraud
* Remove the need and responsibility from online casino operators to maintain player’s account balances
* Enable game developers to monetise their work while maintaining their IP
* Enable game developers to access bankroll for their game without extra responsibility for managing it
* Enable an open ecosystem of provably fair interoperable online casinos

Integrate a system of replicable templates and incentivised audit to allow game developers not familiar with Solidity to benefit from a new value transfer paradigm that Ethereum offers.


## 2.1. Roles

System Participants. During initial design we identified a number of roles that are needed for the system to develop and to function. Some are common roles from the traditional online gambling industry i.e. casino operators, game developers, other roles have been added to a decentralised architecture. 
<ol>
 <li>Game developers</li>
 <li>Casino Operators / Platforms</li>
 <li>Referrers</li>
 <li>Random Number Providers</li>
 <li>Bankroll Backers</li>
 <li>Players</li>
 <li>Autonomous Agents</li>
 <li>DAO.Casino core team/creators*</li>
</ol>

*Creators include not just a current research and implementation core team, but all the early contributors i.e initial security auditors and the first 30 game dev teams who integrated their test games with the DAO.Casino protocol.

## 2.1.1. Developers

Developers refers to both: game developers and contract developers. Whoever provides a functional piece of software automatically receives tokens to their EOA by the DAO.Casino system proportionally to the usage of this software. Independent game developers should be able to collaborate with casino operators easier and retain their IP in the game. 

A front-end developer who is capable of creating a good game doesn’t have to developer a gambling game smart contract, but use existing ones. In this case automatic developer’s rewards will be split between the creator of the contract and the creator of the front-end. 

For the past 1.5 years we have seen growth of gaming and gambling on Ethereum. However we cannot expect that every good game creator will learn how to program for EVM, while there is a lot of talent amongst independent game devs. To leverage existing game design and development skills tested smart contract templates can be used by several game dev teams. Ethereum ecosystem allows teams to share backend without compromising security.   

## 2.1.2. Casino Operators

DAO.Casino system can accommodate multiple front-end platforms customised for different user groups and regions. They remain independent while using the same governance and value exchange protocol. The platform layer of the system is therefore federated. Platforms receive tokens to their EOA accounts proportionate to the usage. If the platform attracts new players to the game it becomes a Referrer and receives Referrer’s reward (see 2.1.3)

Front-end platforms built on top of DAO.Casino system do not have to have additional account balance systems, since the balances and the balance history is stored in Ethereum blockchain. 
Existing online casino operators can create front-end platforms to interface with the token system. We can estimate that as the system evolves, independent game developers teams will be able to form groups and become casino operators with appropriate authorisation.

In a federated model casino operators still provide value to their customers by customising platforms for a particular user group, creating their own ranking and recommendation systems. It is up for the operator to conduct KYC procedures required in their jurisdiction and securely store sensitive user data in compliance with personal data protection laws. User accounts in the whole system are EOAs the only data which is recorded on the blockchain is their balances and tx history. 
Front-end platforms are, as in the traditional online gambling industry, are used for game discovery, rating and as a human interface. However, instead of the server based backend, they run on Ethereum.

They might also integrate user wallets to store small amounts of BET. It is recommended not to store larger amounts of BET in browser based platforms. 
Initial Test Platform. At least one platform is needed for the system to function. DAO.Casino core team is implementing a test frontend platform with a number of games that will be integrated with DAO.Casino governance & reward system on Ethereum mainnet.  See section 4. Maintenance of this platform, future research and testing will be conducted by a non profit foundation.

## 2.1.3. Referrers 

The Referrer  is a member of the affiliate program who brought a referral. The Referral is a participant of the affiliate program who signed up under the recommendation of another participant. 

If you decentralise all the things how do you know where things are? In a decentralised system discovery can be facilitated by economically incentivized participants. Affiliate programs are commonly used for promotion of products and services. The only difference in DAO.Casino system is that referrers, same as all other active participants, are rewarded automatically, and can be sure that they will get rewarded. Another difference is that the rewards depend on whether the referral in question is an active player, to make sure that the affiliate system is sybil proof and the game creator doesn’t share the funds generated by the game with the referrer for nothing. 

Referrers receive 20% of the tokens generated by the game they help promoting while their referral is actively using it. If the referrer is absent, and the player came to the platform on its own through the platform’s own channels, then the platform itself is considered the referrer, which means that it receives the reward. A player willing to top up their BET balance can become a referrer. It applies to other participants. 

## 2.1.4. Random Number Providers *

Random Number providers provide values to the contract that is then generates a value that determines and outcome of the game and receive tokens in exchange.

In the implemented PRNG version Random Provider and Bankroll Backer are same entity. For the current PRNG see section 3. Future versions may include a hybrid system of economically incentivised oracles:
Participants in incentivised oracles system: in addition to the pseudorandom algorithm, an economic algorithm is needed to ensure that the Random Number Providers cannot exploit their partial access to the data which is used in PRNG so that the outcomes of the games remain equally unpredictable for all parties. Random number provider’s system is a hybrid between generating pseudorandomness on EVM and using authenticated data feeds (oracles). Both methods and their weaknesses are described in a section 3.4.  

To participate as a Random Number Provider a participant is required to a) lock their token in the contract b) send data to the RNG contract from which the PRNG will be generated. Intentional or unintentional , malicious behaviour i.e. an attempt to predict the outcome of the game will result in the locked tokens to be distributed as rewards to other participants.  Because of this staking system Random Number Providers are somehow similar to miners in a PoS system.

## 2.1.5. Bankroll Backers

Any token holder can support any particular game by taking on a role of a bankroll backer. Bankroll Backers locks their token in a game contract of their choice and automatically receive a reward. 
Bankroll Backer behaviour can vary depending on the game contract and what PRNG system is used. In a first implementation Bankroll Backer provides BET tokens to the bankroll of the game and a value from which the the outcome of the game is derived.

## 2.1.6. Players
Players discover ga
mes through the platforms and use their tokens as an ingame currency. Player can obtain tokens by becoming an active participant such as a Random Provider or a Referrer or support a crowdfunding campaign at launch. A casino operator can also choose to exchange the tokens to and from common cryptocurrencies. 
For the past year we see more and more gambling games projects built for Ethereum. We can expect that early adopters will be Ethereum and decentralisation enthusiasts. Game contracts are accessible through Ethereum clients, but in the ideal situation a player doesn’t need to know anything about Ether or the technology itself to be able to play and discover games. 

## 2.1.7. Autonomous Agents

Autonomous agents are smart contracts that run on Ethereum that perform tasks that usually would require trust. 
We refer to those entities as agents, because a) their role is as important as any human actors in the system (with the only difference is that they can’t cheat and don’t need to be incentivised). b) once designed and deployed they do not have a human owner capable of withdrawing the tokens from the balances of contract accounts or control the contract in other ways. Instead a contract will “decide” whether to reward an EOA in question, according to it’s rules. Rules cannot be changed by a single party. If the contract in question is proved faulty and the rules do not satisfy the needs of human participants, it will be simply abandoned by the majority of human participants or by all of them. In a similar way an entire blockchain can be abandoned by miners. 

All contracts that are considered a part of the protocol should be autonomous agents - controlled by fair and authorised participants behaviour. Contracts that are deployed for crowdfunding and the issuance of BET are not considered a part of the protocol, but a step to design, deploy and improve it, and in this sense are not autonomous - managed by the foundation. Initial contributors are capable of distributing 26% of all tokens to particular addresses of initial contributors and transfer the rights to manage ether funds collected during the crowdfunding campaign to the foundation. 

## 2.1.8. Protocol initial contributors, foundation and core team

26% of all token supply will be distributed amongst initial contributors and the foundation.

Initial contributors:


<ol>
<li>First 30 teams that integrate their games with DAO.Casino protocol (with the reward system and the first source of PRNG (see section 3.5)</li>
<li>Teams that find and implement the most appropriate solution for PRNG </li>
<li> Authors and supporters of this protocol that will document the protocol, develop it further, and onboard new developers.
* Contrary to a conventional server based project developers of the protocol don’t have a control of the system after it has been launch on Ethereum. Their influence stops at a design level. 

16% of all BET will be distributed amongst the contributors in the following way:

* First game development teams will receive 3% of all available tokens 0.1% per team. 1% to the teams providing PRNG solution. 
* 1% of the BET goes to the team that finds and implements the best solution for the calculation of random numbers.  
* 1.5% Advisors and Security audit and 
* 0.5% Community engagement
* 10% will distributed amongst initial contributors who put work in designing, testing and implementing the system, finding resources, working with legal aspects and producing documentation. 
* 10% will be stored on the account managed by the foundation. 

## 2.2. Token System

DAO.Casino internal token called BET is a ERC20 token. It is used as ingame currency for all the game contracts integrated with the protocol and to power DAO.Casino reward system.  Ingame currency and a reward system are complimentary. Since the token can be used by the players, it rewards make more sense rather than a symbolic point system. 
Overtime BET accounts history can be used as a reputation system and for ranking the games and the players. For example most popular games would have more transaction history. 
Keys to the BET can be stored in platform wallets by players and in any Ethereum client or paper wallet by more advanced Ethereum users. It is not recommended to store a large amount of BET in a browser, even though as a subcurrency it might be less prone to theft than widespread and more well known crypto-token such as Ether.

**Ingame currency**
In a traditional gaming and online gambling industry large gaming companies prefer not to have an ingame token that works across the games because it disrupts their business model. However, when it comes down to smaller independent game producers, having interoperable token makes sense, since it eliminates the need to maintain user account balances. Interoperability between games also what makes the token valuable for the players.
Using Ethereum based subcurrency instead of ether reduces the risk of attacks of rational kind on the system after it scales. If the system is compromised by a malicious actor, the token will become worthless, so attacking the system wouldn’t be a rational thing to do.

**Reward system**
As described above all the participants providing value in one form or another are automatically rewarded with BET to their accounts. More games are accessible with this token, more participants would value it since it represents access to the games. 


