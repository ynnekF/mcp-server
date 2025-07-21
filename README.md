# Model Context Protocol (MCP) Server

The Model Context Protocol (MCP) Server is a server implementation that adheres to the Model Context Protocol. It is designed to facilitate communication between clients and models in a standardized way, enabling seamless integration and interaction.

Reference [MCP Python SDK](https://github.com/modelcontextprotocol/python-sdk)

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