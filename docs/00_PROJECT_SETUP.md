# Part 1: Prerequisites and Setup

> **Navigation**: [← Back to Overview](../README.md) | [Next: Part 2 - Monkey MCP Server →](01_MCP_SERVER.md)

## What You'll Need
Before diving into MCP development with Java and Quarkus, ensure you have the following tools installed:

### 1. Visual Studio Code
- Download and install [VS Code](https://code.visualstudio.com/)
- Essential for MCP development and integration

### 2. Java 21
- Install [Microsoft Build of OpenJDK 21](https://microsoft.com/openjdk/) or a Java 21 compatible JDK
- Verify installation: `java --version`
- Ensure JAVA_HOME environment variable is set correctly

### 3. Extension Pack for Java
- Install the [Extension Pack for Java](https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-java-pack) extension
- Provides comprehensive Java development support
- Includes intelligent auto complete, debugging, Maven/Gradle support, and more

### 4. Quarkus CLI
- Install the [Quarkus CLI](https://quarkus.io/guides/cli-tooling)
- Enables quick project creation and development commands
- Verify installation: `quarkus --version`

### 5. Docker Desktop
- Download and install [Docker Desktop](https://www.docker.com/products/docker-desktop/)
- Required for containerized development and deployment
- Verify installation: `docker --version`
- Ensure Docker Desktop is running before starting development

### 6. Ollama LLM Locally
- Install [Ollama](https://ollama.com/) to run LLM models locally
- Pull the `deepseek-r1` model for MCP tooling support
```bash
ollama pull deepseek-r1
```
- Start the Ollama server: `ollama serve`

### 6. Understanding MCP
- What is Model Context Protocol?
- How MCP Servers work with AI assistants
- The client-server architecture with STDIO protocol
- Use cases and benefits for monkey species management

## Environment Verification
- [ ] VS Code installed and running
- [ ] Java 21 installed and JAVA_HOME configured
- [ ] Extension Pack for Java active in VS Code
- [ ] Quarkus CLI installed
- [ ] Docker Desktop installed and running
- [ ] Basic understanding of MCP concepts

## What is Model Context Protocol (MCP)?

The Model Context Protocol (MCP) is an open standard that enables AI assistants to securely access and interact with external tools, data sources, and services. Think of it as a bridge that allows AI models like GitHub Copilot, ChatGPT, or Claude to:

- **Access Real-time Data**: Connect to databases, APIs, and live data sources
- **Execute Actions**: Perform operations like creating files, sending emails, or managing systems
- **Extend Capabilities**: Add custom functionality specific to your needs
- **Maintain Security**: Control what the AI can and cannot access

### Key Benefits for Java Developers

1. **Familiar Technology Stack**: Use your existing Java skills and rich ecosystem
2. **Quarkus Performance**: Optimized for fast startup and low memory usage
3. **Enterprise Ready**: Built-in support for dependency injection, configuration, and async patterns
4. **Type Safety**: Strong typing with compile-time validation
5. **Rich Tooling**: Leverage VS Code Java extensions and Quarkus dev tools
6. **STDIO Protocol**: Simple and efficient communication via standard input/output

### Architecture Overview

```
┌─────────────────┐    MCP Protocol    ┌──────────────────┐
│   AI Assistant  │ ◄─────────────────►│   MCP Server     │
│ (VS Code, etc.) │    (STDIO/JSON)    │ (Java/Quarkus)   │
└─────────────────┘                    └──────────────────┘
                                              │
                                              ▼
                                       ┌──────────────────┐
                                       │  Monkey Services │
                                       │ (Business Logic) │
                                       └──────────────────┘
```

### Use Cases

- **Monkey Species Management**: Provide AI assistants with access to monkey species data
- **Conservation Data**: Connect AI to wildlife conservation databases and statistics
- **Educational Content**: Generate and update educational content about primates
- **Research Assistance**: Help researchers with monkey-related queries and data analysis
- **Interactive Learning**: Create engaging educational experiences about monkey species

### Project Structure

This Quarkus-based MCP server will include:

- **MCP Protocol Implementation**: STDIO-based communication with AI assistants
- **Monkey Data Model**: Java classes representing monkey species and their attributes
- **Service Layer**: Business logic for managing monkey data
- **Tools and Resources**: MCP tools for querying and managing monkey information
- **Configuration**: Quarkus application properties and dependency injection setup

---

> **Next Step**: Now that you understand MCP and have your Java/Quarkus environment set up, let's build your MCP server for monkey species management.

**Continue to**: [Part 2 - Building Monkey MCP Server →](01_MCP_SERVER.md)
