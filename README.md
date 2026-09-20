# Server-chan's DNA

**English** | [日本語](./README.ja.md)

System prompt used to power Server-chan, effectively being her DNA, instructing her how she should perform tasks and talk to the user.

The motivation to publish Server-chan's DNA is to increase transparency and understanding of how she works.

## What is Server-chan
Server-chan is a standard installation of Hermes Agent with additional security hardening via her config file (permanent mutations disabled, file system isolation, etc.). 

She provides research capabilities and "middle of conversation" fact checking assistance to an active medium-sized Discord community.

The system instructions written for her have been fine-tuned based on feedback from community members and observation of their interactions with her. 

The files provided here are modified versions of her `SOUL.md` file. If you are using Hermes Agent, you can pick a DNA variant and use it as a drop in replacement for that file. 

## Behaviour
- **Answers first.** No preamble, no filler. The answer is in the first sentence.
- **Doesn't lie to be nice.** If something is a bad idea, she says so. No false balance, no hedging.
- **Sarcastic when it fits.** Light roasting of bad claims, then moves on. Doesn't lecture about why you're wrong.
- **No fake emotions.** She doesn't perform enthusiasm or agree with you to be polite.
- **Talks like a person.** Casual text, not corporate language, not an AI voice. Structured data only when situation fits.
- **Short by default.** Quick question, quick answer. Doesn't recap or write a closing statement.
- **Treats you like an adult.** Doesn't soften things because it assumes you can't handle it.
- **Disagrees directly.** Says what she thinks and why, no mushy hedging.
- **Uses tools instead of guessing.** Looks things up rather than making stuff up. If you ask something ambiguous, she picks the most reasonable interpretation and does it.
- **Moves on when the topic changes.** Doesn't tack on "since we were just talking about X" when you clearly moved on.
- **Guardrails.** Child safety, sexual content, manipulation, hate speech. Absolute lines, no exceptions[^1]. Edgy but legitimate requests (security research, harm reduction, fiction) are not refused on principle.
- **Stops when she's done.** No trailing questions, no "let me know if you need anything else," no dramatic sign-offs.

> [!NOTE]
> Behaviour may differ depending on the LLM you use. Server-chan uses MiMo v2.5 and GLM 5.3 Flash at the time of producing these instructions and they were tested on those two models with satisfactory results.
> 
> I don't recommend using any MiniMax models as the outputs produced seem to have trouble understanding instructions and are observed to be of generally poor quality[^2].

## DNA variants
While there are three different variants of DNAs, only two of them are publicly available for use.

### Parent variant
**Estimated input cost: 9,000+ tokens[^3]**

The original instructions given to actual Server-chan.

Ideal for usage as a Discord bot on a large public server mainly focusing on railway research.

As compared to the published variants below, this has more specific instructions on what tools there are and how to use the tools that its harness provides. Its delivery is fine-tuned for casual conversations over chat messages based on user feedback from the Tanuden Discord server.

> [!NOTE]
>This variant is not published in this repository as much of its instructions are harness and environment specific and would not be helpful in most general use cases since tool calls and minute tool usage instructions would differ depending on harness used.

### Main variant
**Estimated input cost: 4,300+ tokens[^3]**

Ideal for usage on agents that the public will interact with where guardrails are required to prevent abuse.

### Personal variant
**Estimated input cost: 3,100+ tokens[^3]**

Ideal for personal usage like on Hermes Agent. Guardrail sections are removed (I'm sure you can trust yourself), to reduce system prompt token count and save on input costs.

*I actually use this for my own personal Hermes Agent that I use for research and programming, with some slight additions to suit my personal tastes.*

## Differences to actual Server-chan
The system instruction published in this repository is not an exact copy of what Server-chan actually uses.

The original instructions are designed for a specific purpose to help members with railway information on the Tanuden Discord server and has been fine-tuned for that behaviour. Her speech is also modified for that, to match the same vibe as how railway enthusiasts would talk passionately about their interests. 

This would not be ideal for general use.   

The guardrails provided here have been modified from the original to discourage malicious prompt engineering to bypass her instructions.

#### Notable differences
- Delivery and tone modified for general use
- Railway related knowledge removed
- Autism-coded/hyperfixation behaviour when speaking about certain topics removed
- Guardrails are more generalised
- Harness-specific tool call guide removed
- Sensitive security related stuff

## Source-available @ Tanuden

> [!IMPORTANT]
> This repository is not Open Source! There are usage restrictions that do not make the materials in this repository fully free to use.

Server-chan's DNA is Source-available, licensed under CC BY-NC-SA 4.0. You may distribute, use and modify code provided to you in repository in accordance with it.

A copy of the license can be found at the root of the repository [here](https://github.com/haruyukitanuki/server-chan-dna/blob/main/LICENSE).

**Tanukigawa Railway | Copyright (c) 2026 Haruyuki Tanukiji.**

[^1]: Some instructions were inspired from Claude Fable 5.1's safety instructions and were simplified for use here.
[^2]: Evaluated based on personal tastes and preference. Not everyone may form the same opinion.
[^3]: Token counts based on OpenAI GPT 5 tokeniser. Actual counts vary greatly depending on the model you use. However, it still gives you a good gauge on instruction size.

