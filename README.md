# Claude Community Marketplace

> **Note**: This is the marketplace structure template. These files should be copied to the separate `smitaiyer/Twtai_siyer` repository.

A community-driven marketplace for sharing Claude agents, skills, tools, and prompts.

## Overview

The Claude Community Marketplace is a collaborative platform where developers share reusable Claude Code resources with the community. Whether you're building skills for quick tasks, agents for complex workflows, MCP servers for integrations, or prompt templates—this marketplace makes it easy to discover, share, and use.

## What's Available

### Skills
Focused, reusable skills for specific tasks. Run with `/skill-name`.

- **code-review** — Review code for bugs, security, and performance
- **api-docs** — Generate comprehensive API documentation
- [See all skills →](./plugins/community-skills/skills/)

### Agents
Specialized agents for complex, multi-step tasks. Invoke with `/agent-name`.

- **migration-expert** — Plan and execute database migrations
- **security-auditor** — Comprehensive security vulnerability analysis
- [See all agents →](./plugins/community-agents/agents/)

### Tools & MCP Servers
Integration tools and MCP servers for extending Claude's capabilities.

- **github-tools** — Manage GitHub repositories, issues, and PRs
- **database-tools** — Query and manage databases
- [See all tools →](./plugins/community-tools/tools/)

### Prompts
System prompts and prompt templates for common scenarios.

- [Explore prompts →](./prompts/)

## Getting Started

### Install the Marketplace

```bash
claude plugin marketplace add smitaiyer/Twtai_siyer
```

### Browse Resources

```bash
claude plugin discover
```

Search for resources by name or category.

### Install a Resource

```bash
# Install a skill
claude plugin install code-review@community-skills-plugin

# Install an agent
claude plugin install migration-expert@community-agents-plugin

# Install a tool
claude plugin install github-tools@community-tools-plugin
```

### Use a Resource

```bash
# Use a skill
/code-review

# Use an agent
/migration-expert

# View help
/skill-name help
```

## Contributing

We welcome contributions from the community! See [CONTRIBUTING.md](./CONTRIBUTING.md) for detailed instructions on:

- How to create a skill, agent, or tool
- Submission process and guidelines
- Code quality standards
- Review process

### Quick Start for Contributors

1. **Fork the repository** and create a feature branch
2. **Create your resource** using templates in `SKILL_TEMPLATE.md`, `AGENT_TEMPLATE.md`, or `TOOL_TEMPLATE.md`
3. **Test locally** with `claude plugin marketplace add ./`
4. **Submit a pull request** with clear documentation
5. **Get feedback** from the community and maintainers

### Creating Your First Contribution

#### New Skill
```bash
mkdir -p plugins/community-skills/skills/my-skill
cp plugins/community-skills/SKILL_TEMPLATE.md plugins/community-skills/skills/my-skill/SKILL.md
# Edit SKILL.md with your implementation
```

#### New Agent
```bash
mkdir -p plugins/community-agents/agents/my-agent
cp plugins/community-agents/AGENT_TEMPLATE.md plugins/community-agents/agents/my-agent/AGENT.md
# Edit AGENT.md with your implementation
```

#### New Tool
```bash
mkdir -p plugins/community-tools/tools/my-tool
cp plugins/community-tools/TOOL_TEMPLATE.md plugins/community-tools/tools/my-tool/README.md
# Create your tool implementation
```

## Repository Structure

```
.
├── MARKETPLACE_README.md           # Marketplace overview (rename to README.md in marketplace repo)
├── MARKETPLACE_CONTRIBUTING.md     # Contribution guidelines (rename to CONTRIBUTING.md in marketplace repo)
├── .claude-plugin/
│   └── marketplace.json            # Marketplace configuration
├── plugins/
│   ├── community-skills/           # Reusable skills
│   │   ├── SKILL_TEMPLATE.md
│   │   └── skills/
│   ├── community-agents/           # Custom agents
│   │   ├── AGENT_TEMPLATE.md
│   │   └── agents/
│   └── community-tools/            # Tools and MCP servers
│       ├── TOOL_TEMPLATE.md
│       └── tools/
└── prompts/                        # Prompt templates
    ├── README.md
    └── [categories]/
```

## Community Guidelines

- **Be respectful** — Treat others with kindness and professionalism
- **Be helpful** — Provide constructive feedback and assistance
- **Be clear** — Document your contributions thoroughly
- **Be collaborative** — Work with maintainers on improvements
- **Be secure** — Never include credentials or secrets

## Support

- **Questions?** Open an issue with the `question` label
- **Bug Report?** Create an issue with the `bug` label and reproduction steps
- **Feature Request?** Start a discussion or open an issue
- **Documentation** — See [CONTRIBUTING.md](./MARKETPLACE_CONTRIBUTING.md)

## License

All resources in this marketplace are licensed under MIT unless otherwise specified in the resource's LICENSE file.

## Maintenance

**Owner**: Smita Iyer ([@smitaiyer](https://github.com/smitaiyer))

**Maintainers**: The Claude community

## Resources

- [Claude Code Documentation](https://code.claude.com/docs)
- [Claude Plugins Guide](https://code.claude.com/docs/en/plugins)
- [MCP Documentation](https://modelcontextprotocol.io/)
- [Claude API Reference](https://platform.anthropic.com/docs)

## Acknowledgments

This marketplace is built by and for the Claude community. Thank you to all contributors who share their skills, agents, and tools!

## What's Next?

- Explore the [marketplace resources](./plugins/)
- Read the [contribution guide](./MARKETPLACE_CONTRIBUTING.md)
- Submit your own contributions
- Help review and improve community resources

---

**Share your Claude resources with the world!** 🚀
