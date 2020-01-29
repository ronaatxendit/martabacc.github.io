---
layout: post
title: The Right Haystack
---


I cannot wrap this problem to something lighter, so I'll just write it vanilla.

Software engineering right, it evolves as time past by. It grows from something Gadogado*, everything mixed and all complexities put in a big bucket - to Nasi Padang, where complexities diversified and distributed according to its responsibilities.

I came to the field where the Nasi Padang era tuck in, an era where people despise Gadogado due to its massive complexity and terrible scalability. It becomes a buzzword - everyone talks about its glory and whatnot.

But that doesn't mean Nasi Padang offer simpler architecture, or a peace of mind. It just splits haystacks, but the size of _all_ haystacks isn't become any smaller.

**Now you don't have one big haystack, but numerous amount of small haystacks.**

Instead of a big massive monolithic server, you have small microservices that talks with each other.

Then comes the time to find a needle. A bug.

Instead of swarming an enormous haystack, you allocate several resources to flock small haystacks with regard to find the needle faster.

It's good though, now we have smaller complexities to swallow.

**However, we may not have spacious pool of resources in one time.** Or maybe the haystacks is not well-designed so some things not placed properly.

Simply put: you looked for a spoon in a kitchen (because it supposed to be there, right) but you found it under the bed. *That spoon does not belong to be under the bed*.

That's what happened to me last week. There was a bug, a simple one, but I cannot find the root cause. It weighs on me so much because I know the haystack inside and out, the possible suspect, but I still couldn't find it.

So the bug is about a flow involves several microservices, and I traced each microservice involved. I trace it bottom up (from inner/deepest microservice to outermost one). I cannot find it, it was irreproducible.

But my coworker found it in a flash - two hours after he was assigned, he created a pull request.

How come?

I spoke to him and asked how he could find it. *He traced it first from the outermost one*. And there's where the bug is. At the outermost one.

Damn, I was looking at the wrong microservice the entire time. I spent my precious time looking at the wrong haystack.

So that's it, folks. Microservices doesn't make your architecture any simpler, they bring another level of complexity which is *a holistic view of the system*.

**Once the team lost holistic perspective of the system, you are doomed.**



**Technical Glossary:**

- *Gado-gado: Monolithics
- **Nasi Padang: Microservices
- Haystack: a microservice
- needle: a bug, feature or anything that forces your system to change

