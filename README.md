# Custom Q Agents

A collection of custom agents for Amazon Q CLI, designed to enhance productivity and streamline development workflows.

## Overview

This repository demonstrates best practices for creating maintainable Amazon Q CLI agents using external prompt files and streamlined resource management.

## Available Agents

### Context Logger
**File**: `context-logger.json`

A project context manager that creates comprehensive event-based documentation for work sessions, decisions, and troubleshooting.

**Features**:
- Event-based context logging with `YYYY-MM-DD-context-name.md` format
- Stores files in `.orbit/context/` directory
- Includes technical details, current state, and decision rationale
- Optimized for team continuity and work resumption

**Usage**:
```bash
q chat --agent context-logger
```

You can also `swap` agents in Amazon Q. Here's how you can do that.

In Q type:
```bash
/agent swap <agent_name>
```

## Architecture

### External Prompts Pattern
This repository uses an external prompts pattern for better maintainability:

- **Agent JSON**: Contains configuration and references to external resources
- **Prompt Files**: Detailed instructions stored in `prompts/` directory
- **Resource Files**: Supporting documentation and conventions

**Benefits**:
- Easier editing and version control of prompts
- Improved readability and collaboration
- Clear separation of configuration and content

### Directory Structure
```
├── context-logger.json          # Agent configuration
├── context-logger/              # Agent resources
│   ├── commands.md             # Usage examples
│   └── conventions.md          # File format and structure
├── prompts/
│   └── context/
│       └── prompt.md           # External prompt file
└── .gitignore                  # Protects sensitive configs
```

## Getting Started

1. **Clone the repository**:
   ```bash
   git clone <repository-url>
   cd custom-q-agents
   ```

2. **Copy agents to your Q CLI directory**:
   ```bash
   # For workspace-specific agents
   mkdir -p .amazonq/cli-agents
   cp *.json .amazonq/cli-agents/
   cp -r prompts/ .amazonq/cli-agents/
   cp -r */  .amazonq/cli-agents/
   
   # For global agents
   mkdir -p ~/.aws/amazonq/cli-agents
   cp *.json ~/.aws/amazonq/cli-agents/
   cp -r prompts/ ~/.aws/amazonq/cli-agents/
   cp -r */  ~/.aws/amazonq/cli-agents/
   ```

3. **Use the agents**:
   ```bash
   q chat --agent context-logger
   ```

### Customization
- Modify prompt files in `prompts/` for different behavior
- Update resource files for project-specific conventions
- Adjust agent configurations as needed

## Best Practices

1. **External Prompts**: Keep complex prompts in separate `.md` files
2. **Resource Consolidation**: Eliminate duplication across agents
3. **Clear Conventions**: Document file formats and organizational patterns
4. **Sensitive Data**: Use `.gitignore` to protect personal configurations

## Contributing

1. Fork the repository
2. Create agents following the external prompts pattern
3. Test thoroughly with Amazon Q CLI
4. Submit pull requests with clear descriptions

## License

This project is open source. See individual files for specific licensing information.

## References

- [Amazon Q CLI Documentation](https://docs.aws.amazon.com/amazonq/latest/qdeveloper-ug/command-line.html)
- [Agent Configuration Reference](https://docs.aws.amazon.com/amazonq/latest/qdeveloper-ug/command-line-custom-agents-configuration.html)
- [Built-in Tools Reference](https://github.com/aws/amazon-q-developer-cli/blob/main/docs/built-in-tools.md)
