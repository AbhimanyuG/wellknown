# Wellknown

What is this?

This is a directory of AI Plugins as defined by https://openai.com/blog/chatgpt-plugins#browsing

With the release of chatGPT plugins, developers can now publish `ai-plugin.json` manifest files alongside their APIs which chatGPT and other LLMs can use to interact with the api in natural language.

This enables ai modesl to use 'tools' to fetch and store data, take actions and listen for events.

# Goals

The main goal for this project is to be like npm for ai agents.

LLM's will eventually need to be able to find the right tools to complete a task, even if they haven't been installed by the user.

This app will provide a search api and a admin ui for managing plugins.

# Submitting a plugin

1. open a pr with your ai-plugin.json file in the `plugins` folder
2. for now, i'll review it and add it to the list

# API

To fetch plugins from wellknown.ai, use the following api endpoint:

`GET https://wellknown.ai/api/plugins`

Response schema

```
{
    name: string
    manifest: object // the ai-plugin.json file as json
    openAPI: object // the openapi json description json
}

```

# Closed Plugins

- https://instacart.com/.well-known/ai-plugin.json
- https://www.kayak.com/.well-known/ai-plugin.json
- https://opentable.com/.well-known/ai-plugin.json
- https://apim.expedia.com/.well-known/ai-plugin.json

# Plugin Templates

ChatGPT Retrieval Plugin Template:
https://github.com/openai/chatgpt-retrieval-plugin
