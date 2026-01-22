---
title: "Jeff Huber: Context Engineering"
type: podcast
show: Latent Space
guest: Jeff Huber (Chroma)
source: https://share.snipd.com/episode/e915ab63-dc66-454d-b9b6-af4a4739e72c
---

The founder of Chroma on why "context engineering" is the real job of building AI applications.

---

## Context Engineering

- Abstractions and primitives are incredibly important when a new market is emerging.
- ==AI has many primitives and abstractions that cause developers to not think critically.==
	- #Nihit-Note-Level-1 Need to understand what this mean, AI has many primitives and how to limits devs to think?
- Developers struggle to understand AI, solve problems, and decide where to invest time.
- Jeff Huber dislikes the term RAG because it conflates retrieval, augmentation, and generation, causing confusion.
- RAG is often oversimplified as just single dense vector search, which is inaccurate.

> **Jeff Huber:** And AI, I think like in part of its hype, has also had a lot of primitives and abstractions that have gotten thrown around and have led to a lot of developers not actually be able to think critically about what is this thing? How do I put it together? What problems can I solve? What matters? Where should I spend my time? For example, the term rag, we never use the term rag. I hate the term rag.

---

## Defining Context Engineering

- ==Context engineering is defined as figuring out what should be in the context window at any given LLM generation step.==
- ==It involves an inner loop (setting up the context window for a specific instance) and an outer loop (improving context window selection over time).==
- ==Context rot highlights the need for context engineering because LLM performance degrades with excessive tokens.==
- Jeff Huber believes context engineering is crucial for AI startups, determining their success.

> **Jeff Huber:** Context engineering is the job of figuring out what should be in the context window, any given LLM generation step. And there's both an inner loop, which is setting up the, you know, what should be in the context window this time. And there's the outer loop, which is how do you get better over time at filling the context window with only the relevant information?

> **Jeff Huber:** This is what, frankly, most AI startups, any AI startup that you know that you think of today that's doing very well, like what are they fundamentally good at? What is the one thing that they're good at? It is context engineering.

---

## Context Rot Research

- ==Jeff Huber and his team researched agent learning by giving agents access to prior successes and failures to boost performance.==
- ==They observed that with multi-turn agent interactions, the number of tokens explodes quickly.==
- ==Instructions were being ignored, highlighting the problem of context rot.==
- Labs often pick benchmarks they perform best on, leading to marketing that doesn't fully represent a model's limitations.
- Their research found that Claude performs better than GPT-4 and Gemini Flash in terms of context length for a particular task.

> **Jeff Huber:** We started seeing interesting patterns where like on sort of multi-turn agent interactions, we were giving it the whole conversation window, like the number of tokens explodes extremely quickly. And instructions that were clearly in there, like we're being ignored and we're not being enacted upon. And we're like, oh, that clearly is a problem.

> **Jeff Huber:** There was a bit of like this sort of implication where like, oh, look, our model is perfect on this task, needle in a haystack. Therefore, the context window you can use for whatever you want. There was an implication there. And well, I hope that that is true someday. That is not the case today.

> **Jeff Huber:** There is a certain amount of love that developers have for Claude. And like, maybe those two things are correlated. If this is true, that's a big explanation for why. You follow my instructions, you know, like there's a clear baseline thing people want.

---

## Evaluating Retrieval Methods

- ==Create small, golden datasets of desired queries and expected chunk returns.==
- ==Use these datasets to quantitatively evaluate retrieval methods.==
- ==Regex or vector search may suffice for certain applications.==
- ==If someone claims to know the best method, ask to see their data.==
- Without data, their claims are unsubstantiated.

> **Jeff Huber:** People should be creating small golden datasets of what queries they want to work and what chunks should return. And then they can quantitatively evaluate what matters. Maybe you don't need to do a lot of fancy stuff for your application. It's entirely possible that, again, just using regex or just using vector search, depending on the use case, that's maybe all you need. I guess, again, anybody who's claiming to know the answer, the first thing you should ask is, let me see your data. And then if they don't have any data, then you have your answer already.

---

## Transformer Architecture Decoupling

- The original transformer architecture was an encoder-decoder.
- Now, most transformers are decoder-only, but embedding models are encoder-only.
- This decouples the transformer: encoding with encoder-only models and decoding with LLMs.
- Vector databases like Chroma store the encoded information.

> **Swyx:** So in some sense, we sort of decoupled the transformer into, first we encode everything with the encoder-only model, put it into a vector database like Chroma. And Chroma also does other stuff, but you know. Then we decode with the LLMs. And I just think it's like a very interesting meta learning about the overall architecture.

---

## Future Retrieval Systems

- ==Current methods of encoding and decoding with transformers are crude and will seem outdated in the future.==
- ==Passing embeddings directly to models, instead of reverting to natural language, will likely become the norm.==
- ==Future retrieval systems will likely operate entirely within latent space.==
	- #Nihit-Note-Level-1 this is a meta point worth noting and understanding
- Retrieval should become continuous during generation, not just a one-time event.

> **Jeff Huber:** I think there's some intuition there, which is the way we do things today is very crude. And we'll feel very caveman in five or ten years. Why aren't we just, why are we going back to natural language? Why aren't we just like passing the embeddings like directly to the models who are just going to functionally like re-put it into latent space, right?

> **Jeff Huber:** So I think like there's a few things that I think might be true about retrieval systems in the future. So like number one, they just stay in latent space. They don't go back to natural language. Number two, instead of doing like, this is actually starting out to change, which is really exciting, but like for the longest time, we've done one retrieval per generation. If you retrieve, and then you stream out a number of tokens. Like, why are we not continually retrieving?

---

## AI Instruction and Memory

- Imagine training an AI by instructing it for a short period, similar to training a human.
- After this training, the AI should perform the task with human-level reliability.
- Memory, easily understood, represents the benefit of this process.
- Context engineering is the underlying tool that enables this 'memory' by feeding the AI the right information.

> **Jeff Huber:** The idea of being able to like take an AI, sit down next to an AI and then instruct it for 10 minutes or a few hours and kind of just like tell it what you want it to do and it does something and you say actually do this next time the same that you would with a human. At the end of that 10 minutes, at the end of those few hours, the AI is able to do it now and the same level of reliability that a human could do it. Like is an incredibly attractive and exciting vision. I think that that will happen.

> **Jeff Huber:** Memory is the term that like everybody can understand. But what is memory under the hood? It's still just context engineering, I think, which is the domain of how do you put the right information into the context window. Memory is the benefit. Context engineering is the tool that gives you that benefit.

---

## Continuously Improving AI Systems

- Continuously improving AI systems involves re-indexing data, merging/splitting data points, and rewriting content.
- Extract new metadata and analyze application performance to identify if the system remembers the correct information.
- Offline compute and inference significantly contribute to this continuous self-improvement.

> **Jeff Huber:** It's sort of re-indexing, yeah. You're taking data, you're like, oh, maybe those two data points should be merged. Maybe they should be split. Maybe they should be, like, rewritten. Maybe there's new metadata we can extract from those. Like, let's look at the signal of how our application's performing. Let's try to figure out, like, are we remembering the right things or not.

---

## Generative Benchmarking

- Use a golden dataset with a list of queries and corresponding relevant data chunks.
- Measure retrieval strategy effectiveness by assessing the percentage of relevant chunks returned for given queries.
- Consider cost, speed, and API reliability alongside retrieval performance.
- If developers have data and answers but lack queries, teach an LLM to generate good queries from data chunks to create chunk-query pairs.

> **Jeff Huber:** Having a golden data set is really powerful. What a golden data set is, is you have a list of queries and you have a list of chunks of those queries should result in. And now you can say, okay, this retrieval strategy gives me for these queries, gives me 80% of those chunks. Whereas if I change the embedding model, now I get 90% of those chunks. That is better.

---

## Prioritize High-Quality Labeled Data

- Prioritize creating a small, high-quality labeled dataset for machine learning, as the returns are very high.
- Don't assume you need millions of examples; a couple hundred high-quality examples can be extremely beneficial.
- Organize a data labeling party with your team to bootstrap the process; even a few hours can make a significant difference.

> **Jeff Huber:** Everybody thinks you have to have a million examples or whatever. No, just like a couple hundred, even like high quality examples is extremely beneficial. And customers all the time, I say, Hey, what you should do is say to your team Thursday night, we're all going to be in the conference room. We're ordering pizza and we're just gonna have a data labeling party for a few hours. And that's all it takes to bootstrap this.

> **Swyx:** Google does this, OpenAI does this and Anthropic does this. You are not above doing this.

---

## Founder's Values and Company Output

- Founders imprint their values on the company's output, reflecting what they deeply care about.
- Society suffers when individuals only live for themselves, highlighting the importance of a broader purpose.
- Building for future generations is essential, even if one doesn't directly benefit.

> **Swyx:** People should believe in something bigger than themselves and build for plant trees under which they will not sit.

> **Jeff Huber:** Going back to the Conway's law thing, like you ship your work chart, you ship what you care about as a founder in some sense. And like I do care deeply about this aspect of what we do and so I think it does come from me in some sense.

---

## Proxies for Identifying Skilled Engineers

- Rust, deterministic simulation testing, Raft, Paxos, and TLA Plus are indicators of the type of engineer Chroma is looking for.
- These technologies act as proxies for the kind of work and engineering mindset Chroma values.

> **Jeff Huber:** A useful encapsulation of this is, like, if you care deeply about things like Rust, or deterministic simulation testing or Raft, Paxos, TLA Plus, Consensus... These are like proxies. You would like the work that we do here.

---

[Listen to the episode](https://share.snipd.com/episode/e915ab63-dc66-454d-b9b6-af4a4739e72c)
