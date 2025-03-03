## AI Info VSCode Extension Issues

An extension for Visual Studio Code that allows you to generate a single markdown file of your entire repo and also query Gemini 2.0 flash to create tasks for other AI Agents. This repository is for Github issues only.

This extension supports 3 main features:

- Ingesting a repo into a single markdown file (no need for Gemini API Key)
- Querying Gemini 2.0 flash to list out the files involved in a task (requires Gemini API Key, returns json of files only)
- Querying Gemini 2.0 flash to rewrite a task into a technical task with repo file context for Cursor agent to work on (requires Gemini API Key, returns markdown of task to copy/paste into Cursor or other Agentic AI coding tool)

![Demo Gif](./aiinfopanelreadme.gif)

### Why?

Cursor & other agentic AI tools require you to provide a lot of context for the AI to work on a task. As your codebase becomes larger, you don't want to manually have to provide all of this context. Some AI Tools can attempt to read associated files, but this extension effectively passes your entire repo to Gemini 2.0 flash to generate the right query context for you. Pass this information to the agentic tool for a much more accurate response with minimal typing.

### How?

This tool generates an "ingestion file" for your entire repo (ignoring things inside of .gitignore and common lockfiles like package-lock.json). It then passes this context to Gemini 2.0 flash with your task to generate the right query context for you. You can then copy/paste this markdown into Cursor or other agentic AI tools to get a more accurate response.
