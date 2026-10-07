---
name: writing-for-humans
description: A style guide for writing technical material that a human reader can actually follow. Use this skill whenever you are writing up technical work for a person, including research summaries, proofs or proof sketches, derivations, algorithm descriptions, reports, papers, or explanations of what you or other agents found. Use it especially for the final write-up at the end of a long research or problem-solving session, even if the user doesn't ask for a "write-up" by name.
---

# Writing for humans

**Default audience:** ARC researchers. You can assume a decent familiarity with math and TCS, and with terms that appear many times in the ARC corpus. *(If you're adapting this guide, edit this line to describe your own readers.)*

In short: work out what your reader already knows, lead with the main idea, keep your terms and symbols clear and consistent, and organize the document so that a reader who skips around can still follow it. The rules below are grouped by theme.

## Know your reader

1. You need to know who you're writing for. In particular, what do they already know, and what do they want to learn? The most common failure here is to assume the audience already knows everything: if you already know the field, why doesn't your audience?
2. It might not be obvious what background the reader has. In technical writing, it is good to err on the side of including more background, but silo it in a section with a clear marker.
3. Connect your explanation to what the human is already familiar with. 'Algorithm X is like Y but with Z different' is extremely useful context to see as early as possible.
4. Relatedly, try to conform with existing conventions. Use the same letters people are already using for things.

## What to include

5. Focus carefully on what a human would think are the important steps here. Making connections to obscure parts of the literature might be trivial to you, but a human won't know what you're referring to. Explain that carefully, and talk less about boilerplate calculations.
6. Consider the use of visual aids. If there's a complicated function, show a graph. If there's a literal graph, definitely show a graph. If you ever have to communicate more than five numbers, find a way to make it either a table or a chart. If we are discussing a tensor network, a causal diagram, a circuit, or some other mathematical object that humans have chosen to associate with images, show me that image. It's possible to overdo this, but if you don't have an image for every four pages of text you're probably underdoing it.
7. Likewise, consider examples. This is another case where it's possible to go too far. When selecting an example, you should focus on picking the right level of abstraction: 'a polytope', 'a simplex', 'a three-dimensional simplex' and 'a three-dimensional simplex with vertices at such-and-such coordinates' are all different. Consider whether added detail is making things more concrete, or just bogging things down.

## Terms and symbols

8. Make sure your terminology is clear. You don't have to define everything (see the default audience above), but terms you invented, or obscure terms from the literature, should be defined before use. Likewise, every symbol should either be a standard in the field you expect your reader to know, or else be defined explicitly the first time it is used.
9. Before you introduce a new concept or term, ask yourself if it makes the overall explanation easier or harder to follow. A rough heuristic is to only introduce the term if you plan to use it three or more times (or if you think most of the audience already knows it).
10. Keep your notation consistent. Each symbol should mean one thing throughout the document, and each thing should have one symbol: don't call a quantity $n$ in one section and $N$ in another, don't use $\alpha$ for an exponent in one section and a step size in another, and don't drift between $Q(n)$ and $Q_n$. When you choose which symbol to settle on, use the field's conventional one wherever there is one (see rule 4): a reader who knows the field will read a familiar letter correctly without checking its definition, and an unfamiliar letter for a familiar object makes them wonder whether you mean something different. Notation your reader is already attached to counts as a convention too, and it takes precedence over the field's, even when it isn't standard: if the user introduced or settled on notation earlier in the conversation, or in a closely related piece of work or conversation you can see, keep using it rather than switching to the textbook version. If it differs from the field's standard, you can mention the standard notation once, for readers who know it, but write in the user's. If your sources use conflicting notation, pick one convention, say which, and translate everything into it. Consistency breaks most often when a document is assembled from pieces written at different times or by different agents. Before finishing, list every symbol and what it stands for, and check each use against that list. If there are more than a handful of symbols, include the list in the document as a notation table.

## Structure for readers who skip around

11. Humans are fickle and impatient creatures. Open with a brief abstract, or a discussion of what the body of the work contains. If it's an algorithm, give a quick discussion of the main ideas; if it's a proof, give a proof sketch. If it's both, you should probably focus on the algorithm.
12. Technical writing is a rare form of writing where the reader is expected to skip around, and almost nobody will consume the full paper end-to-end. This has several implications.
    1. For anything longer than 2000 words, you want to give your reader an outline early on. In physics, the convention is to have a 'structure of this paper' subsection at the end of your introduction, but a good old table of contents works just as well.
    2. Skipping-around culture adds the complication of guessing which part of your paper your reader has already seen at a given time. You can usually guess they've read the abstract, and probably the introduction. If they're reading an appendix, they've probably read whatever part of the body refers to that appendix. In a lot of ways, you should view writing a technical paper as less like writing a narrative and more like creating a wiki. There are lots of disjoint parts, with clear signposts saying 'if you're confused about this, read section 4'.
    3. If anything in your paper is important, it should be mentioned more than once: in the abstract or introduction, again where it is derived, and again wherever it is used. Don't repeat everything everywhere, though; repetition tells the reader that something matters, and it stops working if you overuse it.

## Process

13. A particularly useful trick for AI agents: the agent that produces the final draft shouldn't have the context of the agent that solved the problem. This means the final draft is being written by something that hasn't spent subjective days thinking over the problem and building hard-to-communicate mental edifices. If you can spawn subagents, do this literally: give a fresh subagent the results, the intended audience, and this guide, and have it write the draft.
14. After writing something, give it a readthrough from the audience's perspective and check that they can understand everything, including the checks on terms and symbols above.
