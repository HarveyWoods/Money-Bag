![Harvey Woods Logo](https://scontent.fbed1-2.fna.fbcdn.net/v/t1.0-9/24174133_764322140422909_6972766862639196128_n.jpg?_nc_cat=0&oh=eef91b4ac6b28ef1eb92fc577ca9a23b&oe=5C26CD11)
# Tomshwom's Advanced Crypto Advanced Security Guide
### Part 1 - Privacy, Security, and Trust

###### <i>Tomshwom is a well-versed security figure in the block chain community and it is recommended that everyone reads his Advanced Crypto Security Guide. If you found his contribution useful, please take a moment to follow his Steemit Account [@tomshwom](https://steemit.com/@tomshwom) and/or donate Ether to tomshwom.eth</i>

### Preface
I've been working on this guide intermittently for the past couple weeks, and I've decided to break it into parts for easier consumption. The guide is meant to be a more holistic view of security that goes beyond the "just get a hardware wallet" advice everyone is so content with. Instead, I want to present to you some critical analysis and reasoning on many of the crypto dos and don'ts that you will find on popular youtube channels and subreddits. Security isn't something you can sum up in a 10 minute video, and entertainers aren't the best source for people interested in advanced technical topics.

In this introductory part, I'm going to talk about myself some. Not just because I'm conceited, but because I believe it's important to know where the content you're reading is coming from. Why should you trust some no-name blogger on Steemit, especially when it comes to something as important as security? If that's not the thought that crossed your mind when you read the title of this post, then here...

### Takeaway I: Trust No One. 

I will also be going over security, privacy, trust, how they apply to cryptocurrencies, and why it's important to understand these fundamentals before moving forward to implementing a secure system.

Part 2 will go into the existing security measures present in cryptocurrency today. It will be a deep dive into the differences between software, hardware, and paper wallets, hot & cold storage, access control, and defense in depth concepts.

The last part will be the actual guide for creating a secure wallet that meets all of the criteria defined in these prefatory posts, but the content of these initial writings is arguably even more important than the final wallet guide. UPDATE: part 3 is done and can be found here

This first part of the guide is really an informational piece, so be prepared for a lot of text. I could've filled it with stock images of locks and PCB traces connected to words like "secure" and "privacy", but we're all beyond that...right?

### Why Do You Care About What I Say?
With any sort of informational writing, the source is equally as important as the content. While I do not claim to be an expert in security, I would consider myself a professional. I have a BS in Computer Engineering from Virginia Tech with additional minors in mathematics (focusing on cryptography and combinatorics) and cybersecurity (focusing on intrusion detection and modern cryptosystems). I'm currently employed at an industrial computing and cyber security company.

While at VT, I was fortunate enough to learn under industry experts like Randy Marchany, Wu Feng, and Gang Wang, among others. I've also been an avid follower of Bruce Schneier since I read Applied Cryptography back in 2014. Without a doubt, security is something I'm passionate about.

My first experience with cryptocurrency was in December 2013 after China's central bank banned Bitcoin transactions and the price dropped. I picked up my very first .25 BTC and have been constantly learning about and trading cryptocurrencies since.

Still, I believe that my personal opinion alone on these matters should carry little weight, so I will be framing the content of this guide in terms of the security mindset, as described by Bruce Schneier, and principles of the defense in depth concept.

### What Exactly Is <b>Security</b> and <b>Privacy</b>?
Security often gets confused with privacy. Though they are closely related, there's significant nuance to both. There are many important discussions to be had about general privacy, especially ones about the nothing to hide argument, but this guide is focused on cryptocurrencies. With that in mind, privacy can be thought about as the ability to be free from undesired observation, and security is the ability to negate unauthorized actions.

While security prevents your sensitive data from being stolen, maintaining privacy can keep people from even trying. The perceived security one has is directly affected by how they go about privacy, and this can be extremely effective as a real security measure. It comes down to risk tolerance, something that is great to understand, but very difficult to implement.

### How Does It Apply To Cryptocurrencies?
Most blockchain technology is inherently public. The addresses, balances, and transaction history are available to anyone who desires to look. This presents a unique situation in terms of privacy, and understanding it will help you grasp the reasons why certain simple actions are inadvisable. You've probably heard that you shouldn't tell others how much cryptocurrency you have, especially if it's a lot. The core issue is the risk of associating yourself with your wallet address. This can be done both intentionally (due to your privacy) or accidentally (due to your security), and the association between the address and yourself can happen in varying degrees.

For instance, MetaMask can be used to associate your IP address with your wallet address, making it possible to potentially geolocate the wallet owner and compromise them through the IP attack vector. 

These attacks include:

* Distributed denial of service (DDoS) attacks
* Brute forcing SSH to gain access to the machine
* Port scanning for vulnerable services to exploit
* Mounting a man in the middle (MitM) attack

While the general risk of these attacks is low, your chances increase depending on how much value you have in your wallets. People with greater funds are at a significantly higher risk in this situation since the attacks would be done in a targeted manner (as opposed to botnet-style exploits where risk/reward is removed from the equation). Additionally, wallets that are 1-2 degrees of transactional separation are more likely to be owned by the same user and could potentially also be stolen in one attack.

<b>It's easy to identify wallets owned by an exchange or non-user address (like an ICO fund), so assessing the risk/reward ratio can be done with a level of confidence.</b>

These risks are based on the IP attack vector, but this isn't the one you should be most mindful of. Associating other personally identifying information with your public address is vastly more risky for a number of reasons. Firstly, more data can be gathered easily with only a small amount of initial information. Gathering enough personal information to exploit a person can be much easier than trying to exploit the systems they use. This means that privacy is directly linked to your security, and you must take care to keep yourself from being vulnerable at the same level you would treat your systems. 

### Takeaway II: Privacy Matters.

Lets use myself as an example. In just this post, I've mentioned the university I attended and degree I earned. Given my username, it's not a far-off assumption to determine my first name. My post history includes a photo of myself and other much more revealing information, and all of this is stored on a permanent, public blockchain. I have linked 2 or 3 of my wallets in various posts while fervently asking for donations, and the transaction history on the Ethereum blockchain will link these addresses to even more that I own. There's actually much more information you could dig up, but I'll let that be an exercise for you (feel free to leave anything interesting you find in the comments though).

You may be thinking "so what if I know some useless information now", but this is not the proper mindset to have in the security world. In fact, there's more than enough information to attempt a decent spear phishing attack to try and get me to accidentally download some malware or share sensitive information. Perhaps there's already sensitive information out there that you could leverage as blackmail, or even something that lets you bypass me altogether and gain access to my system directly. 

<b>This example shows what it means to think with in the security mindset.</b>

### The Security Mindset
I believe that Bruce Schneier describes the security mindset best when he says:

<i>"Security requires a particular mindset. Security professionals -- at least the good ones -- see the world differently. They can't walk into a store without noticing how they might shoplift. They can't use a computer without wondering about the security vulnerabilities. They can't vote without trying to figure out how to vote twice. They just can't help it."</i>

Those of you with this mindset are already itching to dig through my posts and gather all the information you can find. This mindset lends itself to security professionals... or nefarious hackers, but the curiosity and drive to exploit things isn't what differentiates the two, it's how you end up going about it.

Those of you who couldn't care less about exploiting vulnerabilities are probably not suited for this type of work, but it's actually you who needs to pay more attention right now. You need to understand that even though you would never think to try and steal somebody's stuff, there are those who do, many of them. Whether it's out of need, greed, or simply for sport, 

### Takeaway III: You Are At Risk Because Of These People.

Do I really care though? The difference between really giving a damn or not about whether people are snooping on you comes down to two things:

1. Your Awareness of People Looking
2. The Effect of What Happens When They Find Something
Ignorance is the bread & butter of most governments and organizations when it comes to privacy. It's an intentionally over-complicated and obfuscated subject so that people have a difficulty grasping exactly how not private their life actually is. In a sense, this mass lack of awareness is important to keeping order while our government "protects" us and our Facebooks "serve" us. 

<i>Hint: If it's free, you are the product.</i>

There is no such excuse in cryptocurrency. Frankly, you don't need to be into crypto, and if you choose to be, you are personally responsible for incurring the risk of being ignorant. That means it's your responsibility to research and understand what you're doing, and nobody owe's it to you.

### Why can't governments/companies just be honest about what they're doing?
We humans actually value privacy. You may not think you do, but if you use doors with locks, ever close the blinds, or have passwords on your devices, you do value privacy. Even if you truly find yourself not doing these things, there's plenty of reasons why you want to control your privacy so that others do not intentionally frame you for things you didn't do.

You may not mind anybody in the world seeing your Facebook profile, but would you mind if I tagged you in a status claiming that we had just stolen a car together, kicked a baby, and thought The Matrix Revolutions was the best of the trilogy? Again, you <i>do</i> value privacy.

Fortunately, there are people like myself who care about the security of others, and want to help for the betterment of the ecosystem as a whole. Unfortunately, trust is required.

### Trust
Some people say that "trust no one" is the first rule of security. Even I made it my first takeaway in this post. I'll fall back to another quote from Bruce Schneier:

<i>"["Trust no one"] might be the first rule of security, but it's the worst rule of society. I don't think I could even total up all the people, institutions and systems I trusted today. I trusted that the gas company would continue to provide the fuel I needed to heat my house, and that the water coming out of my tap was safe to drink. I trusted that the fresh and packaged food in my refrigerator was safe to eat – and that certainly involved trusting people in several countries. I trusted a variety of websites on the Internet. I trusted my automobile manufacturer, as well as all the other drivers on the road."</i>

Should you be trusting me and the content of my posts? The exchange where your money is held? The ICO contract address posted in the comment section?

Although this is just a thought exercise, the level of trust you give me should be proportional to the level at which you already understand what I'm saying, and to a lesser degree, how much faith you have in me and my credibility. Because of this, I choose to reveal some verifiable information about myself that should earn some tiny amount of trust, but ultimately you really shouldn't trust me.

<b>This applies to exchanges, smart contracts, semi-anonymous commenters, and your favorite crypto personalities.</b>

One of the great innovations of blockchain technology is that trustless contracts can be made. It's not wrong to be skeptical and not trust me or others, especially on the internet. In fact, I'm expecting that you will be skeptical if you're truly a cryptocurrency supporter. Trust is earned with consistency, transparency, and discourse. Grant trust to others on a temporary basis if these requirements are not satisfied. This is part of the due diligence you must practice to protect yourself.

"Security exists to facilitate trust," and as I've demonstrated, privacy and security are very closely related. Takeaway IV: be mindful of your existence. This means that taking time to consider your privacy and security helps to build the trust you need to expand your understanding of the systems you're putting money in to.

### Moving forward
If you actually have read thus far, I commend you. Now I'm going to ask for you to do things like leave comments, giving me feedback, and liking this post, but before that I want to stress one final thing.

### Takeaway V: Making Secure Decisions
Security is an opportunity for you to not only protect yourself from future headaches and irreversible loss of money and sensitive information, but also to learn about the systems you use and invest in. 

Information is powerful, and can be overwhelming at first, but putting security at the forefront of your consciousness will help to protect you in everything you do. Like all things, it takes practice and discipline to be good at, but the peace of mind you can get after understanding and implementing security can be very worth it.

### Takeaways Re-Cap
<b>Takeaway I</b>: Trust No One - This refers to the need for skepticism. Never rely on somebody's word at face value. Dig deeper to uncover any bias, vet the source to ensure qualification and integrity, and seek consensus among others in the field.

<b>Takeaway II</b>: Privacy Matters - Many people don't realize what they are actually putting out when they intentionally share small pieces of personal information, and the line between arbitrary and sensitive data can be difficult to determine. Understanding that privacy matters is critical to setting up your personal security.

<b>Takeaway III</b>: You Are At Risk - Regardless of your own personal desire to steal from others, there are those who would steal from you. Malware does not think of morals, and many people don't either. You make yourself vulnerable by projecting personal morals onto things that are difficult to conceptualize (like all the users on the internet).

<b>Takeaway IV</b>: Be Mindful of Your Existence - it's not just something Tich Nhat Hanh would say, it's important to your security too. Think about who is going to see what you put online before you put it there. Consider your actions before you make them. It is difficult to undo some things once you've made a mistake, impossible if blockchain is concerned, so you need to be mindful of all that you do in order to protect yourself.

<b>Takeaway V</b>: Security Isn't A Chore, It's An Opportunity - We often find good security measures to be a burden, but the better mindset to have is one where you view security as an opportunity to bring yourself peace of mind in an uncertain and turbulent world. This is somewhat paradoxical since achieving peace of mind requires first understanding the threats, which often leads to more concern than can be resolved.

<i>Keep an eye out for part 2 of this guide where I analyze the different types of cryptocurrency wallet types and weigh the pros and cons against my own implementation that will be revealed in part 3. Obviously following me would make that easier :) If you'd like to buy me a beer, send some love over to Tomshwom.eth.</i>
