# Kavian proposal

**22 September 2026, aligned with the deck**  
The working proposal, aligned with [`proposal-deck.html`](./proposal-deck.html). It is not software, and it does not claim a running system. The service definition remains in the [English concept](../concept/kavian-concept-en.md); the design circulation remains in the [stitched architecture](./01-stitched-architecture.md). This document binds those to the personal path, the meaning of the name, and the role of small decision models. The published deck is [`index.html`](../index.html).

## 1. The proposal

Kavian is a public infrastructure that helps people — first, people in Iran — understand a collective problem, see how power acted, recognize the cost and consequence of the options, and decide for themselves.

The unit of work is a living dossier. News, documents, data, and people's experience enter it and become reviewable artifacts: a claim and its evidence, conflicting accounts, a timeline, open questions, or a sheet of options. A network of advisers, from different fields and viewpoints, responds to those artifacts. People who are directly affected have their own door; being heard does not require the title of adviser. Meaningful disagreement stays visible in the public view. Publication, and any advocacy, has a named human owner.

Artificial intelligence extends this circulation. Language models draft, translate, and explain. A smaller kind of model only answers a fixed question and says how sure it is. Jev, hosted by TypeSafe, is one. Laya, with open weights, is another. The ability matters. The name of the model does not. None of them chooses in people's place.

## 2. Why the work is personal

This section is the origin of the proposal. It is not evidence inside a dossier.

Cultural work has run since university, in a political atmosphere that was always inflamed. What happened at the university is not retold here. What remains is presence: in the streets in 1401, and again during the events of 1404. What was happening to people was seen at close range. That encounter makes the motive for Kavian sharper, and the project more personal.

The presentation voice is the narrative of a path. The experiences of these years, and what stood in front of them, are a source of inspiration. The date and the neighborhood of that day stay covered on the slides, and no casualty figure is added. Inside each dossier, sources, claim type, and a route of challenge still have to be visible. Otherwise the founder's memory quietly becomes the only frame.

## 3. The name

Apart from private meanings, the **Derafsh-e Kaviani** — Kaveh's banner — is itself the subject of the name.

In the *Shahnameh*, Kaveh rises against Zahhak, a darkness that feeds on people's lives. His leather apron becomes the people's standard. With Fereydun, that domination is brought down. Kaveh does not then seek the throne. He returns to his own life. The name Kavian carries that ethic: struggle against darkness, and then the return of life to the people who live it.

The symbol also contains a warning. Fereydun takes the kingship, and the plain banner is later jeweled into a royal standard. The name is a commitment, and a name cannot guarantee itself. This proposal reads the commitment as follows: Kavian may make the darkness of a decision visible, and then it gives the power of choice back to the person whose life is at stake. If advisers, a model, or the founder sit down in the throne's place, the banner has become a flag of power again.

## 4. What a person receives

When the proposal is working, the public view of a dossier shows:

- which evidence currently supports which claim
- whether a disagreement is about data, interpretation, or values
- who benefits, who pays, and who is still missing
- the options, with their assumptions and how sensitive the comparison is to those assumptions
- what would revise the account, and where a challenge enters
- if an action is proposed, which person owns it

Success is not a count of reports. The question is whether understanding became more possible, an error was corrected, harm was reduced, or an institution became more answerable.

## 5. The structured judgment

The ability is a model that reads a short situation and returns a typed answer with a probability, not a paragraph. Jev and Laya both work this way. Three shapes are enough. A Choice picks one of a defined set. A Noul gives the probability that a stated condition holds. A Score places a situation on ordered levels. Independent questions about one input are asked together. The rule of the proposal composes the answers. Low confidence does not mean a middle value. It means the step belongs with a person.

In Kavian this ability labels a structured step. It is not the brain of truth, and it is not the brain of the public. Jev is a licensed hosted service. [Laya](https://huggingface.co/convaiinnovations/laya) publishes open weights under Apache 2.0, so the same step can run where the text must stay. Open weights are not an audit of Kavian.

| The judgment | Shape | What the proposal does with it |
|---|---|---|
| The main question type: fact, estimate, value, action, or mixed | Choice | A guiding label, when confidence is sufficient |
| Whether each question type is also present | One Noul per type | A subject may contain several question types |
| Which artifact would help review | One Noul per form | Several artifacts may open together |
| Which kind of review is needed | Nouls for public accounts, operations, public language, lived experience, rights and harm | An invitation to examine, not a verdict |
| Whether the text itself shows two incompatible accounts | Noul | The disagreement stays visible |
| Whether publishing this text as written would expose someone | Noul | A low threshold; a false negative is costly |
| How far the text already makes a factual claim inspectable | Score | Coverage of what is shown, not the probability that the claim is true in the world |

English is where these models are described most clearly. Persian, including Kavian’s civic text, has not been tested on either. Until that test, a Persian label is a first pass. Claims about speed, cost, and calibration remain each maker’s claims until they are measured on Kavian’s work.

Jev’s three shapes are described in TypeSafe’s docs as of 22 September 2026: [System One](https://docs.typesafe.ai/concepts/system-one.md), [the three question types](https://docs.typesafe.ai/primitives.md), [confidence](https://docs.typesafe.ai/confidence.md), and [models](https://docs.typesafe.ai/models.md). Laya’s card describes the same three shapes — choice, noul, score — and states that the model does not generate text: [convaiinnovations/laya](https://huggingface.co/convaiinnovations/laya).

## 6. The rule that limits the model

This rule is part of the proposal. It is not an implementation.

- The credibility of a fact moves by source and method. A probability from the decision model does not take its place.
- An estimate under uncertainty may draw on structured judgment when the assumptions and the range stay visible.
- Whether a distribution of cost and benefit is fair belongs to people. The decision model does not score it.
- A proposed action has a human owner, reasons, possible harm, and a path of correction.
- Publication always passes through a human steward. If the chance of identifying or endangering a person crosses the cautious threshold, the text waits for redaction.
- Low confidence on the question type, or a Noul in the middle band, does not harden a label. A steward confirms it.
- The numeric thresholds have not been tuned on Kavian's data. Until then they are precautions, not a scientific law.

Advisers enter after this gate. They do not replace it. Policy Delphi, structured elicitation, multi-criteria comparison, and sensitivity analysis are methods worth testing for their deeper judgment. None of them is assumed to be built, and none of them turns expert weight into a public choice.

## 7. What the proposal says about the rest of the technology

The founder has described a multi-agent layer: LangChain and LangGraph for the flows, LangSmith and Langfuse for observability, execution on Vercel, and code on GitHub. That is his account. This folder has not seen the repository or the deployment. In the proposal, a tool's name appears only where it explains a civic capacity: a trace from source to correction, and a part that can be replaced. Open components support a hope of inspection. Kavian's independence has to be shown in its rules, its data, and a way to challenge the people who operate it.

## 8. The presentation

The audience at The New Centre is inferred from the application, not from minutes of the interview. The shared question is what counts as known, and where an objection can sit.

[`proposal-deck.html`](./proposal-deck.html) is the presentation surface: fifteen slides, right to left, set in Rubik. The field is black and white, with gray where a tone is needed. A loud red takes three slides whole — the path, the centre, the closing pause — and elsewhere it is only an effect: the edge of the first slide, the covered date and neighborhood, and the edge of cards that state a machine's limit. The opening image is a drawing. It is not the tattoo photograph. The exact Derafsh mark is a separate file.

| Slide | What it says |
|---|---|
| 01 | The drawing, without a caption |
| 02 | The Derafsh is the only added element. The bodies are from reality. Two girls: struggle and saving, beside the man |
| 03 | Tehran. The connection was cut by the government. No number. Witness: his presence. Corroboration: the writing sample |
| 04 | Silence is an architecture of information: unseen, undocumented, left alone |
| 05 | These years were in front of him: the streets of 1401 and 1404, cultural work since university |
| 06 | Two bronzes in Berlin, and work on AI in the same city |
| 07 | The full first page of *Kāveh*, the name visible, and how it sits in the path |
| 08 | Seminars, classes, and the faculty's thinking serve the precision of this question. A small step in Iran's civil society |
| 09 | Kavian is the proposed form of that question: a dossier people can read |
| 10 | The public view of a dossier |
| 11 | A designed circulation. No box is deployed software |
| 12 | Six capacities, and the limit of each |
| 13 | Fact, estimate, and value stay distinct |
| 14 | A decision model labels. A person chooses |
| 15 | The banner exists so that life returns to people. The question: the smallest architecture of refusal |

This version has no fictional sample issue. The centre has not written down the session's length or form.

## 9. The path, as the deck tells it

The scene is based on reality. The Derafsh is the only unreal element. The two girls correspond to Iran's women's movement: a continuous struggle, a bold presence, and saving alongside men. One is carried. One stands, steadies the other, and raises the flag.

In Berlin two sculptures stood in front of him, and they are not that scene. *Der seltene Fang* (“The Rare Catch”) is by Ernst Herter, 1896, bronze, Viktoriapark: a fisherman pulling a mermaid from a net. *Der Fischer* (“Gerettet”) is by Adolf Brütt: modelled 1887, Gladenbeck bronze 1892, with the Nationalgalerie from 1894. The photographs are by Axel Mauruszat and Hajotthu, on Wikimedia Commons. The rhyme is only the gesture of carrying, in this city.

*Kāveh* was published in Berlin-Charlottenburg from 24 January 1916 to 30 March 1922. The deck shows the full first page, and the name is readable on it. The first period was a wartime paper; from 1920 it turned to culture and history. Kavian is not a continuation of that paper. Beside the street and beside these bronzes, it is part of a path that arrived here: a public language, and a name that does not take the throne.

The work on AI continues in Berlin. The wish is that this craft, with those human motives, reach its most precise use. The seminars, classes, and conditions at The New Centre are useful for that precision: more understanding, more growth, and more participation in the development of Iran's civil society. That sentence is not a thank-you to the centre, and it is not a claim that the centre has endorsed the project.
