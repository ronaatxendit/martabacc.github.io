---
layout: post
title: The Right Haystack [Technical]
---


I cannot wrap this problem to non-technical context (cannot find the right parable), since this is very technical - so I guess I'll just write it vanilla.

So, software engineering right, it evolves as time past by. It grows from something Gadogado*, everything mixed and all complexities put in a big bucket - to Nasi Padang, where complexities diversified and distributed according to its responsibilities.

I came to the field where the Nasi Padang era tuck in, an era where people despise Gado-gado due to its massive complexity and terrible scalability. It becomes a buzzword - everyone talks about its glory and whatnot.

However, that doesn't mean Nasi Padang offers a simpler architecture, or peace of mind. It only splits the haystacks, but haystack is not become any smaller.

**Now you don't have one big haystack, but small haystacks.**

Instead of one big massive monolithic server, you now have small microservices where they communicate with each other.

Then comes a time you need to find a needle. A bug.

Instead of swarming one big haystack, you allocate several resources to flock our small haystacks with regard to find the needle faster.

It's good, now we have smaller complexities to swallow.

**However, we may not have that spacious room of resources in one time.** Or maybe the haystacks is not well-designed so some things not placed properly.

Simply put: you looked for a spoon in a kitchen (because it supposed to be there, right) but you found it was under the bed. *That spoon does not belongs to be under the bed*.

That's what happened to me last week. There was a bug, a simple one, but I cannot find the root cause. It weighs on me so much because I know the haystack inside and out, the possible suspect, but I still couldn't find it.

So the bug is about a flow involves several microservices, and I traced each microservice involved. I trace it bottom up (from inner/deepest microservice to outermost one). I cannot find it, it was irreproducible.

But my coworker found it in a flash - only two hours after he was assigned, he created a pull request.

How come?

I spoke to him and asked how he could find it. *He traced it first from the outermost one*. And there's where the bug is.

Damn, I was looking at the wrong microservice the entire time. I spent my precious time looking at the wrong haystack.

So that's it, folks. Microservices doesn't make your architecture any simpler, they bring another level of complexity which is *a holistic view of the system*.

**Once the team lost holistic perspective of the system, you are doomed.**



**Technical Glossary:**

- *Gado-gado: Monolithics
- **Nasi Padang: Microservices
- Haystack: a microservice
- needle: a bug, feature or anything that forces your system to change

