---
title: "Redrawing the Space"
subtitle: "Creativity, Cybernetics and the Architecture of Agency. Notes from Inside Production AI"
author: "Kaveh Momeni"
date: "Writing sample · The New Centre for Research & Practice · September 2026"
---

## 1. Rank 301

The Iranian national university entrance examination is taken by hundreds of thousands of people each year. In my year I placed 301st. I mention the number not out of pride (it belongs to a much younger man I barely recognize) but because it matters to the argument. It put me in the computer engineering program of the University of Tehran, which is to say at the centre of the only space that seemed to matter to a young person in my country who wanted to think for a living.

I was dismissed before I could finish, for cultural and political activity as a student. There was no appeal that mattered. I started again from zero, in civil engineering, at a university with none of that prestige. Between the two there were years I still find hard to describe: the kind of darkness in which you stop being able to tell whether the space around you has shrunk or you have. I got through them, with help I was lucky to have. I am not the only Iranian of my generation with such a story, and I do not tell it for sympathy. I tell it because it taught me the first thing I know about intelligence, and it is not a comfortable thing.

The lesson: the space in which you are permitted to think is drawn by someone. Excellence *inside* a space does not protect you from the architecture *around* it. Whoever controls the boundary holds a power that no movement within the space can touch: who is admitted, what counts as a legitimate question, which activities are "cultural and political" and therefore disqualifying.

I have spent the twenty years since learning how such spaces are drawn, first with my hands and then with code. This essay is an attempt to say what I think I have learned, and why I have come to believe that the question of creativity, asked technically, philosophically and personally at once, is among the most urgent questions of the age of artificial intelligence. I am a builder, not a philosopher, and I offer these notes in that spirit.

## 2. Seventy-two strings

During the dark years the one space that could not be taken from me was a trapezoid of walnut with seventy-two strings.

The santur is struck with two light hammers. Before you can play a phrase you spend twenty minutes tuning: each course of four strings pulled to one pitch, each bridge nudged until the octaves ring clean. Then you enter the *radif*, the modal grammar of Persian classical music, which tells you which notes belong and in what order of arrival. Nobody who has tuned a santur thinks of it as a free space. It is a system of constraints, of string tension, bridge position and modal law, and everything beautiful that has ever happened on it happened inside those constraints, not despite them.

I have played for more than twenty years. I have also worked, in ideation and execution, with galleries, artists and architects in Iran, and noticed the same thing in every studio: the people who made work that mattered were not the ones with the most freedom. They were the ones who had understood a constraint so completely that they could find the one move it did not forbid but had never contained.

Hold that image. It is the definition of creativity I will try, with a practitioner's tools, to make rigorous.

## 3. What I built, and what it moved

I began in 2004 writing control software for high-voltage substations, systems in which a wrong signal is a blackout, and then spent more than a decade leading construction, steel-fabrication and infrastructure projects: re-engineering a steel production line from 400 to 1,000 tonnes a month, rolling out an enterprise system across fourteen subsidiaries, building housing and trade centres and airport facilities. Physical systems teach you that constraint is not an opinion; concrete cures at the rate it cures.

Since 2021 I have built a different kind of system. Part-time for a retailer, I designed a hybrid ARIMA–LSTM forecaster that became the basis for weekly replenishment decisions and reduced stock-outs by roughly twelve percent. As AI lead in an engineering firm from 2023 to 2025, I designed and deployed five systems used in daily operations: a multimodal finance-intake pipeline, a project-risk scorer combining natural-language features with gradient-boosted models, scheduling and work-breakdown assistants, a change-impact analyzer, and a procurement decision-support tool. The risk model cut the lag between a problem surfacing in project communications and someone being alerted from over ten days to under twenty-four hours.

None of these systems was creative. All were consequential, and two things happened that I had not designed for.

First, the location of judgment moved. Before the risk model, the question *is this a risk?* was answered continuously and locally by people reading messages. After it, the question was answered once, upstream, by whoever defined the labels, which in this case was me, after weeks of contested conversation with project managers who disagreed about what a "delay" was. Then it was executed automatically thousands of times. The system did not remove human judgment; it centralized it and made it invisible. This is what I now understand *information architecture* to mean: not the layout of a website but the design of where in a system the decision about what counts gets made, and by whom.

Second, every system needed a gate: a human review step before anything reached a decision-maker. I built these for reliability, and came to see them as the only place in the pipeline where something like invention could occur, where a reviewer could say *the model is right about the data and wrong about the question*, and change the question. Remove the gate, and you have a very good sampler running unattended.

## 4. Three words that are not the same

Discussions of "creative AI" collapse three distinct properties into one word.

**Novelty** is an output that has not occurred before. It is cheap: a random number generator is inexhaustibly novel, and a language model sampled at non-zero temperature will produce sentences nobody has written, forever.

**Statistical surprise** is an output improbable under some reference distribution; it is what the engineering literature usually measures, as diversity or as distance in embedding space. But surprise is relative to a model of expectation. A system can surprise *me* while remaining entirely inside its own high-likelihood region, because my expectations and its distribution are different objects. Most first encounters with generative models are surprise of this kind.

**Invention** is an output that changes the space in which outputs are evaluated. Margaret Boden, who did more than anyone to make creativity a computational question, distinguished *exploratory* creativity, which finds new points in a conceptual space governed by fixed rules, from *transformational* creativity, which rejects or revises one of the rules so that previously impossible thoughts become thinkable. Bach within tonality is exploratory; Schoenberg abandoning the home key is transformational. Boden's own observation is telling: transformation typically comes *after* exhaustive exploration, because only someone who has fully mapped a space knows which wall is load-bearing.

The technical reason this matters is simple. A trained generative model approximates a distribution over its training data. Sampling explores that distribution. Adding search (best-of-*n*, an evaluator model, reinforcement from human feedback) lets it climb toward regions the evaluator prefers. But both sampling and search move *inside* a space whose axes were fixed by the training objective and the evaluator's taste. Transformation would require the system to alter the objective or the representation itself: to change what counts as good rather than to find a better one.

I do not claim this is impossible in principle; I would be delighted to be shown otherwise. I claim only that it is not what current systems do by default, and that the gap between very good sampling and redrawing the space is exactly where the philosophical and technical questions live, and where, I will argue, the political ones live too.

## 5. The lava lamp and the average

In late 2022 Refik Anadol's *Unsupervised* filled the atrium of the Museum of Modern Art: a twenty-four-foot screen on which a model trained on the museum's collection continuously generated flowing colour fields. It was enormously popular. The critic Jerry Saltz called it a glorified lava lamp; Anadol replied that Saltz did not understand the medium; most commentary stayed at that level.

I want to make a structural argument rather than a judgment of taste, because I do not think the tool is the problem, and because I have admired the ambition of this work even while doubting it.

What *Unsupervised* displays is the interior of a latent space rendered as motion: a visualization of the high-likelihood regions of a learned distribution over the history of modern art. That is interesting as an artefact. But consider what has been withdrawn. Every work in the collection it was trained on exists because someone chose *against* something: against the academy, the previous decade, their own earlier work. Art has always required a stake and a negation. The generative loop has no stake and cannot negate; its default is the weighted mean of everything it has seen, elegantly perturbed. The aesthetic decision has been delegated to the distribution.

Stafford Beer, the great cybernetician of organizations, gave us the right instrument for judging this: *the purpose of a system is what it does*. Not what its maker intends, not the manifesto, not the ethics statement, but what it does, consistently, in the world. What *Unsupervised* does is teach an audience to experience the smoothed centre of a distribution as the sublime. If I say such work is against art, I do not mean that its makers are enemies of art. I mean that the operation it performs, replacing the decision with the sample, is the inverse of the operation art performs. It naturalizes the average. And when the same operation is running inside the systems through which a generation will write, draw, compose and decide, the stakes are no longer aesthetic.

## 6. Wiener's warning

The thinker I return to more than any other is Norbert Wiener, and not only for *Cybernetics* (1948), which gave us the vocabulary of feedback, purpose and control. It is *The Human Use of Human Beings* (1950) that reads today like a brief for this decade. Wiener's fear was not that machines would become intelligent. It was that human institutions would begin to behave like badly designed machines: optimizing a fixed objective, deaf to feedback, delegating judgment to a mechanism whose values had been frozen at the moment of its construction. He wrote that to live effectively is to live with adequate information, and he understood a society's health as a function of how freely information could move through it. He was writing about corporations and states; he could have been describing a recommender system, or a ministry that publishes only the numbers it likes.

Three cybernetic ideas have become instruments for me.

Ross Ashby's **Law of Requisite Variety**: only variety can absorb variety. A regulator must command at least as many states as the system it regulates. This has a startling consequence for creativity. A culture whose generative tools can only sample its past has *less* variety than the world it must respond to; it will be regulated by that world rather than regulate it. Invention, in Ashby's terms, is the production of variety the system did not previously contain. It is not a luxury. It is a survival condition.

Beer's **purpose-is-what-it-does**, already used above, which cuts through intention and asks of any AI, artwork or government: what does it actually do to the space of the possible?

And Gregory Bateson's definition of information as *a difference that makes a difference*. A sample from a distribution is a difference. Only a transformation of the distribution is a difference that makes a difference.

Together these give the santur intuition its formal shape. Creativity is the capacity of a system to generate variety its own governing distribution did not contain, and thereby to change what it can subsequently regulate. Constraint is not the enemy of this capacity; it is what makes the capacity legible. And whether a system possesses it is decided not by the model but by the architecture: by whether and where the system permits its own objective to be revised, and who holds that permission.

## 7. The price of privacy

I test these ideas where the constraint is not negotiable: a patient's body.

In 2026 I was second author on a study in the *Journal of Distributed Computing and Systems* comparing two ways of fine-tuning a small language model (Phi-3-mini with low-rank adaptation) for surgical phase recognition: centrally, on a hospital edge server that aggregates the data, or federatedly, with data never leaving each device and only model updates being shared. We ran it as a hardware-in-the-loop study, with client devices modelled on NVIDIA Jetson Orin Nano kits and real-time power profiling, because analytical estimates ignore the thermal throttling and memory bottlenecks that dominate on real devices. The centralized approach converged forty-three percent faster; the federated approach carried roughly five percent more energy overhead and significant synchronization delay. We called the difference the *price of privacy* and formalized it into a decision framework for medical cyber-physical systems.

The engineering result is a trade-off table. But the choice between the architectures is not an engineering choice. Centralization buys speed by creating a single point where every patient's data is visible; federation buys locality by accepting inefficiency. Which is better depends on what you believe a hospital owes a patient, and that is not a quantity the hardware can measure. *The architecture is the ethics*, expressed in latency and joules.

Healthcare is where I have chosen to concentrate because it is one of the few domains in which artificial intelligence currently appears to work *for* human beings rather than merely alongside or against them. The stakes are legible, and the constraint, a surgeon's ten-millisecond window, cannot be argued with. Under such constraint, as with the seventy-two strings, the difference between a system that serves and one that performs becomes visible.

## 8. Forty-eight hours in January

The same structure appears at the scale of a nation, and here I stop being an analyst.

I was in the streets during the Mahsa Amini uprising of 2022. I was in Iran on 8 and 9 January 2026, when security forces killed thousands of people within roughly forty-eight hours, under a near-total shutdown of the internet. I will not rehearse the numbers; they are contested precisely because the blackout was designed to make them uncountable. What I want to name is the mechanism. A blackout is information architecture used as a weapon. The state did not only take lives; it seized the space of knowing, so that the dead could not be counted, the wounded could not be found, and each family's grief was sealed off from every other's. Ashby in the street: a regime survives by reducing the variety of what its citizens can know until it falls below the variety needed to act.

Political scientists call this informational autocracy. It relies less on force, which is episodic, than on controlling the model of reality through which people evaluate their own situation. The population is not silenced; it is given a distribution to sample from.

Since then I have been developing a design inquiry I call Kavian, after the banner raised in the *Shahnameh* by Kaveh the blacksmith, whose name I happen to carry, against the tyrant Zahhak. It is not a product and I make no claims for it beyond the documents I have written; it is a set of principles, an architecture, and a promise I made to myself in January. Its premise is that a public accountability platform must be designed from the first line to be *incapable of wanting power*. Concretely: every published claim is typed as fact, estimate, analysis or proposal, and carries its sources and a confidence level; every named institution receives a right of reply archived alongside the claim; the multi-agent analysis that drafts each report leaves an auditable reasoning trace; and a human review queue holds the authority to refuse. The governance charter includes a sunset clause for the founder. The point is not that AI can tell people the truth. The point is that the architecture of an information system, what it types, what it sources, whom it lets refuse, determines whether it expands the space of what citizens can know and demand, or merely supplies a new distribution to sample.

I do not want power. I want to help give back to people the power to know what is happening to them. Everything I have learned about creativity tells me that this, too, is a question of who is permitted to redraw a space.

## 9. Toward a research program

The creative question and the civic question turn out to be one question at different scales. In art: does the system permit a decision against the distribution? In an organization: does it permit the objective to be revised? In a polity: does it permit citizens to reconstruct the model of reality rather than merely consume it? In each case what is at issue is whether intelligence, human, artificial or, as it always actually is, hybrid, keeps the capacity to transform the space it operates in, or has been reduced to searching it.

I have found in Reza Negarestani's work a formulation that names what I have been circling: that mind is not a fixed capacity but something that can become "the artefact of its own conception"; that intelligence, properly understood, is what revises its own model of itself and its world. I do not claim fluency in that literature; I have read it as an engineer reads a map of territory he has walked without one. But it describes, from the side of philosophy, the property I keep failing to find in production systems from the side of engineering, and I would like to learn to read it properly.

I want to keep the question open rather than force it into a thesis, but I can say what I would bring to a seminar table:

1. **Where does exploration end and transformation begin, technically?** Can we construct tasks in which a system must alter its own evaluation criterion to succeed, and observe whether current architectures, with memory, reflection, tool use, multi-agent debate or evolutionary search, ever do so, or only appear to?

2. **Is creativity a property of agents or of systems?** In iterated human–machine work the locus of invention shifts with every turn. Can we describe that shifting without crediting the model with agency it lacks or pretending the human is unchanged by the loop?

3. **Do evaluators enforce the average?** Reward models and aesthetic scorers are trained on what people already prefer. Does optimizing against them structurally exclude transformation? Could an evaluator be designed, in Ashby's sense, to reward variety the system did not contain?

4. **What is the minimal architecture of refusal?** From the review gate in a risk pipeline to the right of reply in a civic platform, some component must be able to say *the question is wrong*. What are its formal properties, and what happens to a system's capacity for invention when it is removed, in a model, in a firm, in a state?

5. **What does constraint contribute?** The santur, the surgical edge, the sanctioned economy: in each the material limit is not the enemy of invention but its condition. Is there a rigorous way to say this, or is it only a musician's intuition?

These questions are at once technical, philosophical, aesthetic and political, and I have stopped believing they can be separated. That is why I am applying to a program that refuses to separate them.

## 10. The strike

When you play the santur, the decision happens in the last millimetre before the hammer meets the string. Everything before it, the tuning, the mode, the phrase played a thousand times, is the distribution. The strike is the sample. And once in a long while, under the right constraint, the strike does something the distribution did not contain: it bends the mode, lands on a note that should not be there and makes it belong, and afterwards the phrase is not what it was.

I was pushed out of a space as a young man and learned, slowly, that spaces are made. I do not know whether a machine can make one. I know that the systems I have built cannot, that the systems celebrated for doing so mostly do not, and that whether they ever could is inseparable from how we design the architectures through which we now know, decide and imagine, and from who is standing at the gate. I would like to spend the coming years learning to ask that question properly, among people who believe it can be asked. It would be a privilege.
