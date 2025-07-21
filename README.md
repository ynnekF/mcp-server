# Model Context Protocol (MCP) Server

The Model Context Protocol (MCP) Server is a server implementation that adheres to the Model Context Protocol. It is designed to facilitate communication between clients and models in a standardized way, enabling seamless integration and interaction.

Reference [MCP Python SDK](https://github.com/modelcontextprotocol/python-sdk)

This project aims to **provide an example of a simple custom MCP server** that can be used locally with tools like Copilot Chat. It demonstrates how to set up a server that can respond to requests and manage context information for clients.

## Features

- **Context Management**: The MCP Server manages context information for each client, allowing models to access relevant data and state information.
- **Protocol Compliance**: The server strictly follows the MCP specifications, ensuring compatibility with other MCP-compliant clients and services.
- **Extensibility**: The server is designed to be easily extensible, allowing developers to add new features and capabilities as needed.

## Getting Started

To get started with the MCP Server, follow these steps:

**Install UV**
 Trying out UV instead of pip for this project: [UV install methods](https://docs.astral.sh/uv/getting-started/installation/#installation-methods)

`curl` to download the script and pipe it to `sh`:
```bash
$  curl -LsSf https://astral.sh/uv/install.sh | sh
```

Add `$HOME/.local/bin` to your `PATH`:
```bash
$ source $HOME/.local/bin/env
```

Create a uv-managed project:
```bash
$ uv init .
```

Add MCP to the project dependencies:
```bash
$ uv add "mcp[cli]"
```

**Test the MCP Server**
You can test the MCP Server by running the following command:
```bash
$ uv run mcp dev main.py
```

## Run the MCP Server

For integration with Copilot Chat, we need to create `.vscode/mcp.json` in the project root with the following content to the `servers` section
```json
"mcp-server": {
    "type": "stdio",
    "command": "<uvPath>",
    "args": [
        "run",
        "main.py"
    ]
}
```

Then you can add the MCP resource to Copilot chat.. after that Copilot will have access to the defined resources and tools.

Here is an example of Copilot interacting with the greeting tool.
```
Hello, Ken! 🎉

I can see your MCP server is working beautifully - it just provided me with a 
personalized greeting for you! It's fantastic to see your Model Context 
Protocol server in action, dynamically generating content based on context.

Your MCP server setup looks solid with UV package management, and it's clearly
functioning well if it's able to serve up dynamic greetings through the protocol. 
This is exactly the kind of extensible, context-aware functionality that makes MCP 
so powerful!

What would you like to explore or build next with your MCP server, Ken? Whether 
it's adding more dynamic resources, enhancing the greeting functionality, or 
working on other features, I'm here to help! 🚀
```

To run the MCP Server manually, use the following command:
```bash
// With Claude
$ uv run mcp install main

// Else
$ uv run main.py
```


## API Reference

The MCP Server exposes a RESTful API for communication with clients. Refer to the API documentation for detailed information on available endpoints, request/response formats, and authentication requirements.

## Contributing

Contributions to the MCP Server are welcome! If you would like to contribute, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes and commit them with descriptive messages.
4. Submit a pull request for review.

## License

The MCP Server is licensed under the MIT License. See the LICENSE file for more information.