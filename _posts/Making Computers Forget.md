# Making Computers Forget

Human memory is imperfect. Many experiences are hard to remember. They change shape. They become lost to us. It’s part of the reason we forgive past transgressions and also part of the reason we make the same mistakes over and over.
Computers don’t forget. Not in the human sense of forgetting. If the data is deleted or overwritten or the physical media is destroyed, the information is lost. Digital information is only ever truly forgotten when all copies ever made of it are deleted and all of the persons exposed to it finally forget it.

This has had both a great and terrible impact on all of our lives.
You can find out that, 10 years ago, a coworker with whom you enjoy working had political leanings that repulse you. It doesn’t matter whether that person has since changed completely - you will now see them differently.
You can see how your old flame from high school is doing and re-stoke the long-dead embers of your love for her. You will feel that pinch in your heart and sniff away a tear, why are you doing this to yourself, you should have moved on by now.
A company you’ve never heard of may legally build an entire profile of your personality and track your every move online with impunity. You don’t know about it, you won’t know about it. It’s by design. That’s the point.

It doesn’t really matter why we do this to ourselves, as persons, as a society. Money, ego, it really doesn’t. It’s within reach and we do.

## What now?

Society finds ways. It’s built defensive mechanisms. People now have an online personal brand to care about. One misstep and you’ll be memed by complete strangers on the other side of the planet for decades. Compound that with not always knowing or controlling whether something you do goes online and that has a chilling effect on interactions. Most just stop caring.

Lawmakers around the world are also starting to see this as an issue. In some parts of the world, they have stepped in with initiatives like the GDPR. In other parts, events like the Cambridge Analytica scandal are serving to force some hands.

Being a software developer I’m not looking to attack any of these angles. What I’d like to explore is a technical question which has been bothering me:

**How can we make computers forget like people do?**

## The groundwork

Let’s start with a few assertions:

1. The nature of digital information is that unless the people behind those systems want or have to, they won’t make their computers forget. Entire businesses and ecosystems have been built around this inability to forget.
In this post I’ll make the assumption that some act outside the system, for instance as legislation or economic force, has forced their hand.

2. Nobody knows exactly how we remember and forget. This question has been on the minds of many for millennia. There is a lot of research into this, but we won’t go into it.

## Short and long term memory

*TODO: Expand this part*

I’ll start with the easiest thing to implement, because it’s already there. Short term memory is RAM, long term memory is disk. RAM can hold less information and is volatile, while committing to disk makes for long-term storage, but is more costly in terms of time (write to disk) and money (cost of disks).

## Making it hard to remember

Once we’ve committed a certain memory to our long-term memory, there are a few action we can take to help us recall it easily. The one we’ll focus on is continuous recall - the more you try and recall a memory, the fresher it will stay in your mind and it’ll be easier to recall. Once you’ve left a memory alone for a long time, it’ll be far harder to recall. You may not even be able to recall it at all.

Our problem is now reduced to making it harder for computers to recall its least accessed information.

What does "harder" mean in this context? What is hard for computers when accessing data? In the pure case it’s a long calculation, something that is computationally expensive.
But how do we make data access computationally expensive?

Imagine a 100-byte file. It’s limited to a single block on the physical media and a pointer to that from the filesystem’s table of contents.