TODO: Can each paragraph have possible future as a topic sentence?


I'm sorry to be the VC who says he's been interested in AI for awhile, but I've been interested in AI for awhile. And fortunately, I have the git timestamps to prove it. But I certainly wouldn't consider myself early (I remember being skeptical around 2012 when Roy, Karin, and James at Bloomberg Beta and Matt at Firstmark told me should focus on it as an engineer.) Nor could I really claim to be a real practicioner. I'm more of an AI script kiddie if we're being honest.

But building my first toy neural network in Matlab, and later in Python, really blew my fucking mind. The idea that I don't really instruct the computer to do what I want, so much as instruct it to create an empty model architecture, and then how to train itself on data - that the final product would be a function that I didn't really write so much as teach - was, and still is, totally nuts. And it could do things I never thought a computer could do - recognize images, and reason about unstructured, messy data.

As an investor, we have had a few investments in AI-related startups both as an angel and as a professional investor.

But even being bullish on AI as a category of technology, the really hard part is figuring out how to invest in it. For me, this is because there are many possible futures in AI, and some of them are mutually exclusive. I suppose what I intend to do is place bets on many of the possible futures, so despite being another VC with more AI takes, this writing is as much for me as it is for you.

Hardware
---
It seems that the easiest way to invest in the hardware stack of AI is to buy NVIDIA, Microsoft, Alphabet, Amazon, Apple, and maybe Meta. But there are a number of possible futures that present opportunities to startups.

It seems that the Big Tech companies that are traditionally known for software are leading GPU development internally. Some of this quite public, and some of it is opaque to us on the outside, but it's pretty easy to guess what's happening, as it's been happening for years now. The enormous dependency of Big Tech on compute for AI is manifesting in really crazy purpose-built hardware that isn't necessarily about transistor density anymore. Power consumption matters, as a main cost driver for training and inference. Bus speed between CPU and GPU matters now. And some of these companies are building hardware (Google's TPUs, likely Meta) that are specialty GPUs for ML frameworks like TensorFlow and Pytorch.

They're using this hardware internally, and they're also selling access to it on their public clouds. The service wrappers on top of this hardware is pretty good! Could it be better? Maybe. But the cost structure of reselling GPU compute is not great. And one trend reversal I think we've seen in devtools broadly since the days of Heroku, is that reselling cloud services, with notable exceptions, suffers from a lower margin (and therefore revenue multiple) than businesses without this "cost-plus" pricing strategy. But still. There is a possible future of better services on top of public cloud GPUs. And there are ways around the cost-plus pricing structure.

This relatively small number of companies building their own compute is growing. We may see it grow even further, including more AV companies and other more traditional tech firms looking to sell cloud offerings. Big Tech, and overseas fabs, have had cornered resources on chip design and fab for so long. But now the industry is critical, and smart employees are graduating, leaving, and taking their skills with them.

Big Tech owning hardware is an important trend for a few reasons.
1. You'll never sell hardware to these companies.
1. You'll likely never beat them on cost.
1. You'll likely never beat then on speed of development.
1. Specialized silicon, even when superior in certain domains, may lag behind the incredibly fast development cycles of the more generalized GPU silicon

Of course, outside of Big Tech, is the NASDAQ's latest $T company - NVIDIA. Some companies may find value in owning their own hardware and running it. Right now, we see plenty of AI startups using their first check to buy $20,000 GPU rigs and plopping them on the office floor. Long term, total cost of ownership, this may be cheaper. I wonder if there is opportunity to build software on top of these (tools that might be analogous to Terraform, Kubernetes, or Pivotal Cloud Foundry.) I wonder if there is a possible future of data centers for tech companies again. The public cloud will always try to make itself more economical than this, but this could also depend on trends in hardware availability and cost. Even crazier - I wonder if companies with fine tuned or specialty models at the edge might have GPU mainframes in the office for data privacy. Again, the trend of public cloud offerings would be to support privacy and security in the cloud instead of this. Still. Possible future.

Hardware for edge training and edge inference are both very interesting, for certain applications. I wonder at what point company concerns about data privacy, both risk to hackers that is outside their control, and risk that their AI service providers have a conflict of interest with them (Amazon, Google, Microsoft,) forcing them to run models at the edge. Could this be physical hardware (or edge workers like from Cloudflare or Fastly?) There may be other reasons to train at the edge. Imagine a personal model in a hardware device that is fine tuning and doing transfer learning at the edge. People imagine this is what Amazon Alexa does (it is not.) But with a number of technical barriers knocked down, Alexa or other devices like this, could potentially do that. Would there be any benefit? I also wonder about low power, low cost devices at the edge that want to run inference, maybe with low power, maybe without an internet connection. And regulation around customer data, data privacy, and AI/AGI accelerates all of this.

As of this writing, access to GPUs is extraordinarily constrained. But I wouldn't necessarily assume that continues. Supply and demand have this interesting relationship, and shortages are often followed by gluts. We have seen this before. Even with GPUs! One enormous monkeywrench in this possible future is China/Taiwan relations, as Taiwan houses TSMC. The Biden administration intends to incentivize onshoring chip fab. It would be good for the country and indeed the world, to have redundancy, so let's hope it works.

Foundational models
---
A number of companies like OpenAI and Cohere are building foundational models and selling access to them via API. Right now, these businesses are indespensible, and they are driving the rapid adoption of LLMs by programmers of all skill levels, and non-programmers. There is a possible future where they are totally dominant. The combination of their cornered talent resources, unique experience, relatively cheap access to compute, relatively cheap capital, and possibly soon - regulatory capture, means that perhaps they have built something of a moat.

There is another possible future where anyone can build their own foundational model. Some companies such as Adept are doing this for their own use cases. Today, the reasons you might do this rather than fine tune or transfer learn are esoteric, and it's only a tiny sliver of the market that really has this need. That could change in the future if people discover new narrow use cases, the costs and talent requirements drop, or Open Source models become more and more available and more and more capable. Today, some of these OSS models are performing say 80% as well as the leading tech inside the black box of OpenAI's APIs, but that will likely change (by how much?,) and/or there will likely be use cases where this tradeoff is acceptable. If this future comes to pass, companies that act as hubs for models like HuggingFace are riding some seriously strong tailwinds. As will any tools that help more companies do this, and better.

There is yet another possible future where both of these things exist. Some segment of companies is building their own models, while others are building on top of third parties or accessing their APIs. To me, this is the most likely, but the question is what is the segmentation? This dictates the kind of company you'd build. Maybe big banks want to do what OpenAI does. In which case, there may be companies who want to sell OpenAI's superpowers and tools to them. Maybe it's startups, which might suggest there's a powerful developer bottoms-up approach to be had. Time will tell.

LLMs and other Transformers
---
ChatGPT is probably the best demonstration of the power of general purpose transformers. But it seems the same architecture is useful for a number of things that are not natural language. Programming languages (Copilot,) images (Dall-E, Midjourney, Stability.) I think that fundamentally the most interesting part of ChatGPT is the GPT, not the Chat.

A lot of people are very excited about natural language as an interface to software. So am I! But I"m also interested in applications of large models where natural language isn't the input, and/or where natural language isn't the output. When I was in college (I am old,) and we played around with NLP, there was a distinction between a regular langauge and a natural language, and NLP only applies to the latter. Today, that's not true - Codex was replaced by ChatGPT! I wonder what other applications we will find for this novel architecture that is NOT natural language.

AIs Writing Code!
---
I contend that Copilot is the highest value use case of ChatGPT today. Given the install base and the amount of code written by Copilot that GitHub says is being committed, programmers are clearly integrating this AI tool into their workflows already. That makes sense. We are early adopters by nature. The things that Copilot is writing are often repetitive and rote. And the user interface is perfect. Since Copilot is an autocompleter, it's a drop-in replacement for our existing tools, and is 100x better. Instead of completing words, it completes lines of code. The cost of bad prediction is essentially zero, as I can hit escape and keep typing.

Another example of where I think the demo and the most exciting part are different. Copilot's whiz-bang demo is turning comments into code, but most engineers are using the VSCode plug-in for autocomplete instead.

Still, there is an obviously interesting possible future for the natural language to code pipeline. Will LLMs that write code finally bring the promise of no-code? In the short term this maybe looks like people being able to build things that they could previously build in Bubble, Retool, Weebly, Squarespace, Shopify, Zapier etc. - all in one - and maybe some additional things that were never well-supported by those tools. In the long term, it could be the death of the programmer. In Star Trek, characters often instruct the computer to create Holodeck and other programs by telling it an event-driven thing to do, and then saving it. You can imagine a lot less code getting written by hand if anyone can tell a computer what they want to do.

I am personally bearish on that future. Automation eliminates tasks, not jobs. We've seen this many times before in the software engineering field. Quantum leaps in higher level languages have often come with fears that programmer jobs will be destroyed (or offshored.) And yet, here we are. Paying engineers $1M/year to build neural networks at Google, using those same higher level tools we were told would eliminate their jobs. I see LLMs that write code as augmenting the programmer. They may also function as the greatest leap forward in "raising the floor" that we've ever seen.

But code-generating AI doesn't have to replace programmers to be big. There could be a huge category of people making signficant, valuable applications with either a natural language interface, or some hybrid of natural language, traditional user interfaces, and code. In this possible future though, I might argue that the people doing this are still engineers. The first, most valuable lesson I learned about engineering in undergrad was that engineering is about solving problems for people.

Who captures this stuff?
---
Incumbents
Startups

The Death of SaaS?
---

Tools!
---
