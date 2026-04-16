# Codex Skill for Gemini CLI 🔄🤖

A specialized skill that teaches Gemini CLI how to delegate code reviews, adversarial design checks, and complex tasks to the OpenAI Codex CLI.

*Version: 1.0.0*

## 📖 Origin Story & Credits
This project was born out of pure workflow habit and a love for AI synergy. I originally got so used to the practicality of the Codex plugin inside Claude Code that I decided to cross the streams. First, I brought Gemini CLI to Claude Code ([gemini-claude-plugin](https://github.com/madciapka/gemini-claude-plugin)). Then, I realized I desperately needed Codex's specific review capabilities back inside the Gemini CLI.

Full credit for the core concept goes to the original [codex-plugin-cc](https://github.com/openai/codex-plugin-cc)—this project is simply adapting that fantastic idea for a new home.

*Fun fact: This skill was written by Gemini, inside the Gemini CLI, using code reviews delegated to this very same Codex skill.*

## ✨ Features
- **Smart Code Reviews**: Automatically gathers git diffs and pipes them directly to Codex.
- **Adversarial Analysis**: Specialized prompts for security flaw and edge-case hunting.
- **Autonomous Delegation**: Allows Gemini to seamlessly ask Codex for implementation help when it needs a second opinion.
- **Background Support**: Handles long-running Codex tasks via Gemini's native backgrounding.

## 🛠️ Prerequisites
- [Gemini CLI](https://github.com/google-gemini/gemini-cli) installed.
- [Codex CLI](https://github.com/openai/codex-plugin-cc) installed and authenticated (`codex login`).

## 🚀 Installation

### Option 1: Install from URL (Easiest)

```bash
gemini skills install https://github.com/madciapka/codex-gemini-skill.git --scope user
/skills reload
```

### Option 2: Install from Source
Clone the repository:

```bash
git clone https://github.com/madciapka/codex-gemini-skill.git
cd codex-gemini-skill
```

Install the skill:

```bash
gemini skills install ./codex.skill --scope user
/skills reload
```

## 💡 Usage
Once installed, simply ask Gemini:

- "Ask Codex to review my uncommitted changes."
- "Have Codex perform an adversarial review of this branch."
- "Delegate the implementation of the login logic to Codex."

For more details on the underlying workflows, see the technical [SKILL.md](./SKILL.md) instructions.

## 🤯 The LLM Inception
If you are wondering how deep the rabbit hole goes, here is an actual excerpt from the creation of this skill:

**Me:** It's funny though, I created a gemini skill inside claude to call you because I like the original skill for claude which calls codex, now I am creating a codex calling script for gemini in gemini with codex reviews :D

**Gemini:** ✦ It's pure LLM Inception.

You basically built a circular firing squad of productivity:
1. You taught Claude how to call Gemini.
2. You used Gemini to teach itself how to call Codex.
3. You had Codex meta-review the code Gemini wrote to enable the calling of Codex.

We've officially closed the loop! You now have a "Trinity" of agents that can all delegate to each other. If one model gets stuck on a logic puzzle, you can just ask it to pipe the problem to the next one in the chain until someone finds the bug.

Now that the Codex Skill is global, you're only one step away from asking Gemini to ask Codex to ask Claude for a third opinion.
