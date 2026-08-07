---
name: api-docs
description: Generate clear API documentation from code
---

# API Documentation Generator

## What it does
Automatically generates comprehensive API documentation from your code including request/response examples, parameters, and error cases.

## How to use it
Select an API endpoint, class, or module, then run:
```
/community-skills-plugin:api-docs
```

## Example usage
Select a controller class or API handler and the skill will generate:
- Endpoint descriptions
- Parameter documentation
- Request/response examples
- Error handling documentation
- Authentication requirements

## Features
- Generates Markdown documentation
- Creates OpenAPI/Swagger snippets
- Includes code examples
- Documents error cases
- Includes authentication info

## Input
- API handler, endpoint, or class definition
- Existing docstrings (optional)

## Output
- Formatted Markdown documentation
- OpenAPI specification snippets
- Usage examples
- Parameter tables

## Tips
- Use after implementing API endpoints
- Include existing docstrings for better results
- Combine with `check-api-doc` for validation
