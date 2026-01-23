---
title: "I Lean-ed into Formalization first time"
seoTitle: "I Lean-ed into Formalization"
seoDescription: "Discover Lean's journey for formal proof verification and metaprogramming through practical experiences and impactful projects"
datePublished: Fri Jan 23 2026 18:19:33 GMT+0000 (Coordinated Universal Time)
cuid: cmkr7gjz3000502js2ars3nm9
slug: i-lean-ed-into-formalization-first-time
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1769192101145/51dd5fdc-1673-4e68-b96a-5f4cef494e01.png

---

I was fascinated when one of my Professors, [Siddhartha Gadgil](https://math.iisc.ac.in/~gadgil/) at [Indian Institute of Science](http://iisc.ac.in) gave a talk where he should machines checking proofs. This is not AI. Rather a programming language. I was in my first year in undergrad when I saw this and I was mind blown, it was anyway pre-blown from the beauty of analysis it had seen that year, but it sure got re-blown (xD) after seeing a coding language taking proper care of types and semantics of mathematics, handling structures and can even do induction(WOW!), and it is able to proof ANYTHING in mathematics if done correctly.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1769191967336/65affb87-f24b-4e99-bc18-a205c28fc24f.png align="center")

Yes, this language was called(still called that) [**Lean**](https://lean-lang.org). This beautiful language is able to verify proofs while writing and gives us goals to complete. As an amateur I was just hearing the talk and totally believed that it was some AI business hidden somewhere(and yes I was an amateur to use the word “AI” for this). Why AI came in? Cause they talk also said AI models are good enough to win IMO Gold medal which was pretty shocking(though I didn’t care cause I am still gonna think about problems instead of hands-up OH lord GPT solve this…). I got to know about a new “Field” that way.

## First Summer - AutoTA

My interest in this topic didn’t go rather I became more curious on how it works. I just wanted to try proving math using computers, cause if they prove it then it is correct! Goal Accomplished 🎉! Thanks to God’s Grace, I got a project under Professor Gadgil. As a first year undergrad, I was tasked to develop an auto checker of students proof using AI like GPT, Gemini, etc. by giving the student’s proof to a model to give a JSON structure breakup, and then passing it to evaluate correctness and giving feedback. This involved lots of software Engineering rather than Lean, but the goal was to automatically write their proof in Lean and check it for us.

To my surprise and horror(and Professor’s yet another meeting’s comment), that was not easy since we would need an autoformalizer, which means automatically convert math proofs to Lean. Professor was developing his tool called [**LeanAide**](https://github.com/Siddhartha-Gadgil/LeanAide)**,** more about in next section.

Closing to my first year summer, the results were good in terms of AI evaluating math proofs(undergraduate level) written by students, although formalization part couldn’t be done, and curtains closed.

## LeanAide - Autoformalization of Proofs

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1769192004899/14feac0a-c3c9-4e63-80b2-9671b7d77c7a.png align="center")

LeanAide is an autoformalization tool which (still under-progress) uses the power of Lean’s powerful automation and AI to convert proofs and definition into Lean. This is not an ML model like you see like Aristotle, but queries AI in it’s architecture for small purposes(not ask to generate the whole thing either). It has been carefully designed to give correct proofs everytime but with sorries if unable to proof. It’s a GENIUS’s work. You can generate definitions and theorem statements in lean from your English query, generate Lean4 proofs of your theorems from English proofs, and many more functionalities.

I started my research intership under Professor Gadgil since the following Winter Break(2024 December) and worked on tasks like debugging, finding examples which LeanAide is buggy in and help in ideating. I also made a Streamlit Website for easy usage of the LeanAide server, and other Software Engineering stuff, which if you know me, I do that too. But I wanted to work on actual Lean code but I was still a young caterpiller.

Lean has mainly 2 powers, formalization into mathematical proofs and MetaProgramming. Metaprogramming is a type pixie dust not a lot of fairies possess today, although under hard training anyone can learn how to(not magic). It allows you to create your own system and proof theorems around it. The powerful part about it is that once you create a system, you can prove with an utter guarantee your system is correct since you PROVED IT’S CORRECT!!! Like correctness of Algorithms, things in any CS architecture, writing English which is Lean(mapping syntax), the power is unlimited. Lean’s metaprogramming is truly extensible!

But I didn’t know metaprogramming, but I started my quest to learn it! But before that I needed to learn proper Lean language and formalizing proofs too.

## Proofs and Programs, & LeanHuffmanCoding

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1769166073870/bc318618-7821-4bbc-9649-469a9529761c.png align="center")

I took a course offered at IISc, under Professor Gadgil in Spring 2025, called **Proofs and Programs: MA207** where he taught us formalization in mathematics and basic Lean from scratch till our own formalized proofs and projects. I really learnt the power of Lean, its powerful Type System, automatation, simp-ing, and proving lots and lots of theorems. Back then **grind** wasn’t there.

I successfully proved Uniqueness and Correctness of Huffman Encoding Algorithm as course project. Check it out here: [**AnirudhG07/LeanHuffmanCoding**](https://github.com/AnirudhG07/LeanHuffmanCoding)**.** I have yet to prove optimality, but that’s on my TODO list for sometime I am free. I edited the proofs later on to use **grind** which shortened the proofs significantly. But the older versions exist too.

## Back into LeanAide and Lea(r)n-ing

I have been continuing my internship under Professor for LeanAide since then(and even now ongoing) and we have made significant progress in correctness of proofs. Now as **grind** came about and improvement in Lean’s automation, LeanAide works faster and better. I created a cool NextJS website for LeanAide serving purpose of querying, showing responses, documentation, and made a fork of lean4web to host LeanAide. The website isn’t publicly out yet, but hopefully will be when LeanAide is production ready. I am also be working on Benchmarking LeanAide on Mathematics Datasets used for ML training or particularly for formalization. This it to publish a paper soon on LeanAide and show this amazing project’s power!

```plaintext
import LeanAide.TheoremElab
import Mathlib

-- Translating a theorem
#theorem "There are infinitely many odd numbers"

-- Translating a definition
#def "A number is defined to be cube-free if it is not divisible by the cube of a prime number"
```

I learnt how to design systems which are extendible, by this I mean design choices even in mathematics that you can carry forward and generalize rather than a fixed use case. Extendible systems aren’t just Systems in Tech that need to be extensive, but a way to represent an entity in such a fashion to allow it expand itself on its own, letting it unfold its properties simply and adding any features to expend system would naturally occur like dissolving ink in ice. Choices in structure representation is important in Lean, rather everywhere and they show the way you look at the world. Very philosophical but true.

I had my teammates, undergrads and PhD’s from IISc, and working alongside them was amazing. A level of trust develops when you see their results and you can work on your part trusting their’s will be correct. Growth mindset in any project, may it be in your tiny project, is important which I saw in Professor for this project to be usable by any mathematician or student. The ability to be able to expand it a way anyone can use, access and seemlessly use it is very important.

## Understanding how to Lean into Lean

As my learning into this amazing world of formalization grows, I am taking more and more projects. Currently I am working in company which is trying to use Lean4 for it’s software correctness and pipelines(sorry no more info), and I am learning MetaProgramming to create the system and prove guarantees and equivalences of systems to prove correctness. This increases the reliability of auto generated codes for a system by (say) AI. Actually, this is a fascinating application to check correctness to outputs from AI which are based on some mathematical model, which you can multiple generate and check correctness.

Many other Lean Autoformalization tools exist, which include Aristotle from Harmonic, a prominent figure in this field which is based on ML model trained on Lean4 data and logic, carefully designed to help AI gives correct outputs everytime thanks to Lean. I am amazed by the power of Aristotle but I am honestly more surprised by LeanAide, which proves theorems without training a model. No comparisons here…

I attended a workshop by professor which was **“Lean4 for Software Engineers”** where he should the power of Lean4, to create a DSL between Lean4 and your system/language like Python or even controlled English, using metaprogramming. You can create games like tic-tac-toe, Tower of Hanoi, Rubics Cube, and many more. This has vast applications and I believe the future can guarantee’s atleast correctness for newer automated systems using Lean4 and other formalizers. Check out the repository [LeanLangur](https://github.com/Siddhartha-Gadgil/LeanLangur) for more fun examples.

## I just started Lean-ing and will Lean into it more!

I am going to continue to Learn Lean and grow my skillset to MetaProgramming, which I am have started. Hopefully I get to work with amazing people in this area and become someone I can be proud of in future. The best part of Lean is not only the beauty of the language, but the amazing and helpful community of Lean on Zulip, which doesn’t think you are a newbie or an expert but helps you grow and understand Lean more and more!

If you read this blog and want to know how to possibly apply Lean4 in your projects, which could be any industrial application not just mathematics, you could contact anyone from the Lean Community or me(contacts on my website: [anirudhg07.github.io](https://anirudhg07.github.io)). Hope you got to know a glimpse of Lean(oh by the way, that’s actually a project to learn Lean: [PatrickMassot/GlimpseOfLean](https://github.com/PatrickMassot/GlimpseOfLean)) and appreciate this ongoing work to formalize this world into a correct place xD.