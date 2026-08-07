# Contributing to the Claude Community Marketplace

> **Note**: This is the contributing guide template. This file should be renamed to `CONTRIBUTING.md` in the separate `smitaiyer/Twtai_siyer` repository.

Thank you for your interest in contributing! This marketplace is built by the community for the community. We welcome contributions of skills, agents, tools, and prompts.

## What Can You Contribute?

### Skills
Reusable Claude Code skills for specific tasks (code review, documentation, testing, etc.)
- **Location**: `plugins/community-skills/skills/[your-skill-name]/`
- **Template**: See `SKILL_TEMPLATE.md`
- **Example**: `skills/code-review/` or `skills/api-docs/`

### Agents
Specialized agents for solving complex, multi-step tasks
- **Location**: `plugins/community-agents/agents/[your-agent-name]/`
- **Template**: See `AGENT_TEMPLATE.md`
- **Example**: `agents/migration-expert/` or `agents/security-auditor/`

### Tools & MCP Servers
Custom tools and MCP servers for integrating external services
- **Location**: `plugins/community-tools/tools/[your-tool-name]/`
- **Template**: See `TOOL_TEMPLATE.md`
- **Example**: `tools/github-tools/` or `tools/database-tools/`

### Prompts
System prompts and prompt templates for common use cases
- **Location**: `prompts/[category]/[prompt-name]/`
- **Format**: Markdown with usage examples

## How to Contribute

### 1. Fork the Repository

```bash
git clone https://github.com/smitaiyer/Twtai_siyer.git
cd Twtai_siyer
```

### 2. Create a Feature Branch

```bash
git checkout -b add/your-skill-name
# or
git checkout -b add/your-agent-name
git checkout -b add/your-tool-name
```

### 3. Create Your Resource

#### For Skills
1. Copy the template: `SKILL_TEMPLATE.md`
2. Create directory: `plugins/community-skills/skills/[your-skill-name]/`
3. Create `SKILL.md` with your skill implementation
4. Add any supporting files (scripts, utilities, etc.)

Example structure:
```
plugins/community-skills/skills/my-skill/
├── SKILL.md                    # Main skill file
├── reference.md                # Optional: detailed reference
└── examples/                   # Optional: example implementations
    └── example-usage.md
```

#### For Agents
1. Copy the template: `AGENT_TEMPLATE.md`
2. Create directory: `plugins/community-agents/agents/[your-agent-name]/`
3. Create `AGENT.md` with your agent implementation
4. Include any supporting files or configuration

Example structure:
```
plugins/community-agents/agents/my-agent/
├── AGENT.md                    # Main agent file
├── instructions.md             # Optional: detailed agent instructions
└── config/                     # Optional: configuration files
    └── defaults.json
```

#### For Tools
1. Copy the template: `TOOL_TEMPLATE.md`
2. Create directory: `plugins/community-tools/tools/[your-tool-name]/`
3. Create `README.md` with comprehensive documentation
4. Include source code, configuration files, and setup instructions

Example structure:
```
plugins/community-tools/tools/my-tool/
├── README.md                   # Comprehensive documentation
├── src/                        # Source code (if applicable)
├── config/                     # Configuration templates
└── examples/                   # Usage examples
```

### 4. Test Locally

```bash
# Navigate to the marketplace root
cd Twtai_siyer

# Test your contribution
claude plugin marketplace add ./
claude plugin install [your-plugin-name]

# Verify it works
/your-skill-name
# or
/your-agent-name
```

For tools, ensure all setup instructions work:
```bash
# Follow setup steps in your tool's README
# Test that all documented functionality works
```

### 5. Document Your Contribution

Your contribution should include:
- Clear, descriptive title and description
- Usage examples and expected behavior
- Input and output format documentation
- List of requirements and dependencies
- Relevant links or references
- Any special configuration or setup needed

### 6. Create a Pull Request

```bash
git add .
git commit -m "Add [type]: [resource name] — [brief description]"
git push origin add/your-skill-name
```

Create a PR with:

**Title**: `Add [skill/agent/tool]: [resource name] — [brief description]`

**Description**:
```markdown
## What this contributes
Brief description of what you're adding.

## Type
- [ ] Skill
- [ ] Agent
- [ ] Tool/MCP Server
- [ ] Prompt

## When to use
When should someone use this resource?

## How to test
Step-by-step instructions to test this locally.

## Requirements
- Dependency 1
- Dependency 2
- External service requirements (if any)

## Examples
Show usage examples or a sample run.

## Checklist
- [ ] Documentation is clear and complete
- [ ] Tested locally with `claude plugin marketplace add ./`
- [ ] No credentials or secrets included
- [ ] Follows naming conventions (kebab-case)
- [ ] All dependencies documented
```

## Guidelines

### Naming
- Use kebab-case for directories and resource names
- Be descriptive and specific (e.g., `security-auditor` not `auditor`)
- Avoid generic names like `helper`, `utility`, or `tool`
- Keep names short but meaningful (max 30 chars)

### Documentation
Every resource needs clear documentation:
- **Skills**: What it does, how to use it, what it expects, what it produces
- **Agents**: Capabilities, when to use it, example prompts, limitations
- **Tools**: Setup instructions, required credentials, all available tools/functions
- **Prompts**: Use cases, example inputs/outputs, customization options

Include:
- Clear one-line description
- Detailed explanation of functionality
- Usage examples
- Input and output formats
- All parameters or options
- Helpful tips for best results

### Code Quality
- Test thoroughly before submitting
- Follow Claude Code conventions and best practices
- Ensure skills and agents work independently
- Include proper error handling
- Provide helpful error messages
- Don't include debug code or temporary files
- Keep code clean and readable

### Security
- **Never include credentials** — API keys, tokens, passwords, or any secrets
- **No hardcoded values** — Use configuration files or environment variables
- **Validate inputs** — Don't trust user input
- **Handle errors safely** — Don't expose sensitive information in errors
- **Document security** — Explain what credentials or permissions are needed

### Licensing
All contributions are licensed under MIT by default. Include a LICENSE file in your resource if using a different license.

## Resource Guidelines

### Skills
A skill should:
- Be focused and do one thing well
- Be runnable with just `/skill-name` or minimal input
- Provide actionable, clear results
- Complete in reasonable time (under 30 seconds ideally)
- Include helpful tips and best practices
- Work in isolation without depending on other skills

**Example skill anatomy**:
```
---
name: code-review
description: Review code for bugs and security issues
---

# Code Review

## What it does
Detailed explanation.

## How to use
/code-review

## Example
Specific use case and expected output.

## Tips
- When to use it
- What it works best with
```

### Agents
An agent should:
- Handle complex, multi-step tasks
- Make autonomous decisions within its scope
- Ask for approval when needed (especially destructive operations)
- Handle errors gracefully with clear messages
- Document capabilities and limitations clearly
- Explain what tools/resources it needs access to

**Example agent anatomy**:
```
---
name: security-auditor
description: Comprehensive security analysis
---

# Security Auditor

## What it does
Detailed explanation of agent purpose.

## How to invoke
/security-auditor [options]

## Capabilities
- What it can do
- Tools it uses
- Autonomous vs. approval-required actions

## Example prompts
Real prompts users might type.

## When to use
Best use cases.
```

### Tools/MCP Servers
A tool should:
- Integrate Claude with external services or capabilities
- Provide well-designed, documented tool interface
- Include comprehensive setup documentation
- Handle authentication securely (never expose credentials)
- Include rate limiting and error handling
- Support common use cases
- Include examples of actual usage

**Example tool anatomy**:
```
# My Tool

## Overview
What this tool does.

## Installation
Step-by-step setup.

## Configuration
What environment variables or config needed.

## Tools provided
- tool_name — Description
- another_tool — Description

## Usage Example
Real usage by Claude.

## Requirements
Dependencies and versions.

## Authentication
How to set up credentials securely.
```

## Review Process

1. **Automated checks** (GitHub Actions):
   - Validates directory structure
   - Checks for required documentation
   - Verifies JSON/Markdown formatting
   - Scans for exposed secrets

2. **Community review** (Pull request discussion):
   - Other contributors provide feedback
   - Testing and usability feedback
   - Suggestions for improvement

3. **Maintainer review**:
   - Final quality check
   - Ensures consistency with marketplace standards
   - Verifies security and completeness

4. **Merge**:
   - Your contribution is merged
   - Becomes available in the marketplace
   - Added to release notes

## Community Standards

- **Be respectful** — Treat other contributors with kindness and professionalism
- **Be helpful** — Provide constructive feedback and assistance
- **Be collaborative** — Work with maintainers on improvements
- **Be professional** — Keep discussions focused on the work
- **Be responsive** — Respond to feedback in a timely manner

## Maintenance After Submission

After your contribution is merged:

- **Maintain it** — Fix bugs and address issues
- **Keep it updated** — Update for new Claude Code features
- **Respond to feedback** — Help users understand how to use it
- **Document changes** — Update version numbers and changelog

## Questions?

- **Open an issue** with the `question` label for help
- **Check existing issues** to see if your question is already answered
- **Review examples** in the marketplace for reference
- **Contact maintainers** at sbokil@gmail.com

## Tips for Success

1. **Start small** — First contribution? Start with a simple skill
2. **Use templates** — Copy and adapt the templates provided
3. **Test thoroughly** — Your contribution reflects on the marketplace
4. **Document well** — Good documentation makes your contribution shine
5. **Be patient** — Review takes time, feedback is constructive
6. **Iterate** — Be open to improving based on feedback
7. **Have fun** — Share what excites you!

## Recognition

Contributors will be recognized in:
- Repository README and contributors page
- Release notes when your resource is published
- Community acknowledgments and newsletters
- Marketplace featured resources

## Recognition and Attribution

When contributing, you agree that:
- Your contribution will be published under MIT license
- Your name/GitHub username will be credited
- Others can use and build upon your work
- You maintain the right to use your contribution in other projects

---

Thank you for making the Claude Community Marketplace better! Your contributions help the entire community. 🚀
