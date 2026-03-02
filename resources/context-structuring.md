# Context Structuring

There are as many recommendations for how to structure/name your context as there are AI agents and tools, we wanted to outline some generic best practices and resources here for people getting started. 

## agents.md vs. claude.md vs...

Most of the AI ecosystems have the concept of a core context file, both at the tool-level and project-level. These can be inclusive of your preferences for different programming languages, interaction patterns, or even instructions for how the agent talks to you. 

If you're using multiple tools or agents, having a generic `agents.md` file seems to be the best approach, but if you're working with a specific toolset, it might be easiest to use the tool's default settings, such as `claude.md`, `.clinerules`, and so on. 

Regardless of the name of the file, they are all going to serve the role of an initial resource or instruction set for the agent you are using to work on your project. Your `agents.md` file should be short and communicate essential information about a project and paths to related information on the project. It should not contain all the context for your project, but it should point to your context sources. 

### Sample `agents.md` content 

```
# agents.md

## Environment setup
- npm install
- npm run build
- npm test
- npm lint

## Project structure
/src
    /components
        /tests
/docs
    /ai

## Context bank
- Testing: `/docs/ai/testing.md`
- Architecture: `/docs/ai/architecture.md`
- Code Standards: `/docs/ai/code-standards.md`

## Github instructions
- Commit format: `[task]: [description of task]`
- PR title format: `[{issue #}]: [description of task]`
- Always run `npm test` and `npm lint` before committing.
```

## Helpful resources on AI context

These articles and resources have been helpful for us as we developed this talk and project, you might find them helpful as well. 

- [AGENTS.md](https://agents.md/)
- [Does AGENTS.md Actually Help Coding Agents? A New Study Has Answers](https://academy.dair.ai/blog/agents-md-evaluation)
- [Progressive Context Building: Why Your AI Should Get smarter Every Time You Use It](https://www.linkedin.com/pulse/progressive-context-building-why-your-ai-should-get-time-khachatryan-zaync/)
