# Petstore on Sokie

[Swagger's public Petstore API](https://petstore3.swagger.io) as an MCP server, hosted on [Sokie](https://sokie.sh). Each endpoint is a tool, written as a Markdown file in `tools/`, and `sokie.json` says where the spec is and how calls reach the API. `skills/adopt-a-pet` tells an agent how to find a pet and order it.

Pushes to `main` deploy the server. Each pull request gets a preview server of its own, and Sokie comments on it with the address. See [Link a repository](https://sokie.sh/docs/link-a-repository).

The Petstore asks each caller for an API key. The demo takes any key; Swagger's docs use `special-key`.
