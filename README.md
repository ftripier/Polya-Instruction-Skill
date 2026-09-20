# Pólya Instructor

An Agent Skill for Codex and Claude Code, for working through a problem with an
instructor who helps you find the next step. It adapts George Pólya's advice in
*How to Solve It* to an interactive tutor for mathematics, programming, science,
and other reasoning tasks.

The instructor starts from your attempt, offers a useful question or hint, and
adjusts the help to your response. It supports understanding, planning, carrying
out an approach, and checking what you learned. You can request a more concrete
hint, a prerequisite explanation, or a complete worked solution at any time.

To choose its next question, it identifies your current obstacle and a useful
thinking step, then checks whether the prompt is within reach, preserves room
for discovery, teaches a reusable habit, and has a motivation you can recognize.
These checks adapt §17, “Good questions and bad questions.”

For word problems, it helps turn the request into a precise target, distinguish
quantities and their dependencies, and introduce useful intermediate unknowns
before choosing operations or evaluating the result.

## Install

This uses the same [Skills CLI](https://github.com/vercel-labs/skills) as
[clarity](https://github.com/addyosmani/clarity): `npx skills add`, with a plural
`skills`. Node.js and npm/npx are needed for the installer; the skill itself has
no runtime dependencies.

From this folder, install globally for Claude Code:

```sh
npx skills add . --skill polya-instructor --agent claude-code --global
```

Or install globally for Codex:

```sh
npx skills add . --skill polya-instructor --agent codex --global
```

To install for both:

```sh
npx skills add . --skill polya-instructor --agent codex claude-code --global
```

For a project-only installation, run this from the project where you want to use
the skill, replacing the example with the path to this folder:

```sh
npx skills add /absolute/path/to/polya_instruction_skill --skill polya-instructor --agent claude-code
```

Replace `claude-code` with `codex` for a Codex project installation, or omit
`--agent` and its value to choose supported agents interactively. Start a new
agent session if the installed skill does not appear in the current one. Claude
Code discovers the installed package under `.claude/skills/polya-instructor/`
for project installations or `~/.claude/skills/polya-instructor/` for global ones.

You can check discovery without installing:

```sh
npx skills add . --list
```

### Install from a repository

The folder is a single-skill package, with `SKILL.md` at its root. Once you publish
it to a Git repository, replace `OWNER/REPOSITORY` below with its actual GitHub
location:

```sh
npx skills add OWNER/REPOSITORY --skill polya-instructor
```

That is a command template, not an existing published repository. No npm package,
build step, or `package.json` is required.

## Use

### Claude Code

Invoke `/polya-instructor` with the problem and any work so far:

```text
/polya-instructor Help me prove that the sum of the first n odd numbers
is n². I checked a few cases but don't know how to prove it.
Give me one hint at a time.
```

Or, when the problem is already in the conversation:

```text
/polya-instructor Help me find the next step from my attempt above.
```

Claude Code loads the same `SKILL.md` and supporting references as Codex. Its
native [skill slash command](https://code.claude.com/docs/en/skills) needs no
separate command file or plugin.

### Codex

In Codex, invoke `$polya-instructor` and include the problem and any work so far:

```text
Use $polya-instructor to help me prove that the sum of the first n odd
numbers is n². I checked a few cases but don't know how to prove it.
Give me one hint at a time.
```

```text
Use $polya-instructor to help me debug this binary search. I want to
understand why it loops forever; please don't rewrite it for me.
[paste the code and a failing input]
```

The description also makes the skill available for automatic selection when a
learner asks for guided problem solving. Ordinary requests to implement or
deliver something should keep their original meaning.

## Package contents

- [SKILL.md](SKILL.md): activation criteria and tutoring instructions.
- [agents/openai.yaml](agents/openai.yaml): optional Codex display and prompt
  metadata; Claude Code uses `SKILL.md` directly.
- [references/teaching-notes.md](references/teaching-notes.md): illustrative
  interactions and a reading guide to the relevant book sections.
- [references/proof-dialogue.md](references/proof-dialogue.md): a complete,
  annotated tutor–learner conversation, including a false start, construction of
  a proof, and reflection on the method.
- [references/modelling-dialogue.md](references/modelling-dialogue.md): a worked
  conversation about a moving shadow, from defining the requested speed to
  building a model, calculating the result, and checking its meaning.
- [LICENSE](LICENSE): MIT license for the original package contents.

The teaching instructions are an original adaptation. The package does not
include or license Pólya's book.
