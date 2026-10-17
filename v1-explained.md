# Coding Agents 1.0

**Coding Agents 1.0** is a set of assumptions that took hold during the initial popularity of coding agents in the AI Gold Rush. The design can be seen as a series of enhancements to the 2022 ReAct architecture. This includes CodeAct (2024), SWE-Agent (2024), and products that followed. There were also social assumptions shaped by funding incentives and AGI (Artificial General Intelligence) ideology.

## Terms 

A **Coding Agent** is typically an LLM chat loop that calls tools, where the tools are relevant to software development. Tool capabilities include reading, editing, searching, and execution.

**Context** is a view of the current conversation history that the agent loop sends to the LLM at every turn to decide the next step. It included prompts, messages and tool calls. As the conversation gets longer, the **Condenser** creates the shorted view through abbreviation and summarization since the LLM has a limited context window.

**Context Management** is the user behavior of organizing prompts and other context in order to optimize the LLM's useful signal or reduce cost.

**Prompts** are user messages entered interactively or stored in a reusable place such as stored in source control. Prompts are auto-loaded for various scopes using conventions like `agents.md` and `skill.md`.

**Headless** (aka background) agents start with an initial task prompt and "chat" with the tools instead of the user to complete the task.

**Hooks** are user-configured scripts that intercept tool calls and add a  to limit or adapt the tools behavior.

**Sub-agents** allow an agent to invoke a tool that starts a headless agent conversation and reports back.

## Social assumptions

Vendors present coding agents as directly analogous to developers (people) and on the verge of surpassing them, feeding these assumptions:

* Agents as virtual employees
* Generating more code or spending more tokens is considered better (Tokenmaxxing).
* Adoption by fear or force is accepted ("AI is inevitable").
* Difficulties are blamed on the user ("skill issue").

Consequences of the "Agents as virtual employees" assumption:

* Marketing an agent as an "AI Software Engineer".
* Agents are judged by whether they seem overall "better" or "worse" than a person, not by fitness as a tool.
* Abstraction by delegation.
* Prompts as Specs.

By simultaneously presenting tools as *for* developers *and* developer replacements, vendors create a confusing adversarial relationship. User feedback is dismissed as replacement anxiety. Speed is used as evidence of superiority, hence "more is better".

Abstraction by delegation disconnects the user from the process, requiring them to wait for rare (but vital) moments of feedback and anticipate failure modes that their interface doesn't expose.

## Design assumptions

* All behavior driven by the 2022 ReAct loop architecture.
* User controls mainly with prompting (though chat and text files)
* State is conversation history with a lossy condenser.
* Improved by model training and user configuration.

# Coding Agents 1.1

Coding Agents 1.0 is deprecated as of January 1st, 2027 with end of life May 1st, 2027 (Mayday).

The *minimum* supported version will be 1.1, which is a one-line patch on 1.0.

* Remove: "Adoption by fear or force is accepted"
* Adopt: "Consent matters (Right of refusal)"

Please apply your patches.