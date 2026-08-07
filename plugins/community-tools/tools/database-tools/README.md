# Database Tools MCP Server

## Overview
MCP server providing tools for querying, analyzing, and managing databases including PostgreSQL, MySQL, MongoDB, and others.

## Installation
```bash
npm install @mcp/database-tools
```

## Configuration
Configure database connections:
```json
{
  "databases": {
    "prod": {
      "type": "postgresql",
      "host": "db.example.com",
      "port": 5432,
      "database": "production"
    },
    "staging": {
      "type": "postgresql",
      "host": "staging-db.example.com",
      "port": 5432,
      "database": "staging"
    }
  }
}
```

## Tools provided
- `query` — Execute SQL queries safely
- `get_schema` — Get database schema information
- `analyze_query` — Analyze query performance
- `get_table_stats` — Get table statistics
- `create_backup` — Create database backups
- `run_migration` — Run database migrations
- `validate_schema` — Validate schema integrity

## Usage Example
Claude can use this to:
- Execute SELECT queries for analysis
- Review schema structure
- Analyze query performance
- Suggest optimizations
- Plan migrations

## Requirements
- Database connection credentials
- Network access to database server
- Appropriate user permissions

## Authentication
Connection strings and credentials stored securely in config.

## Features
- Multiple database support
- Query safety checks
- Query optimization analysis
- Automatic transaction handling
- Schema introspection
- Performance analytics

## Limitations
- Read-heavy operations preferred
- Write operations require explicit approval
- No support for very large result sets
- Some advanced database features may not be supported

## Security
- Queries are sandboxed for safety
- Credentials never exposed to Claude
- Query validation before execution
- Automatic rollback for failed transactions

## Example
```
User: What's the structure of the users table?
Claude: [Uses get_schema tool] Shows table structure, indexes, and constraints
```

## Contributing
Submit improvements to the [Database Tools repository](https://github.com/community/mcp-database-tools)

## License
MIT
