---
name: migration-expert
description: Specialized agent for complex database and schema migrations
---

# Migration Expert Agent

## What it does
This agent specializes in planning and executing complex database migrations. It analyzes your current schema, understands your target structure, and creates safe, tested migration paths.

## How to invoke
```
/migration-expert
```

Provide details about your migration needs, current schema, and constraints.

## Example prompts
- "Migrate my PostgreSQL schema from v1 to v2 without downtime"
- "Convert this table structure to support multi-tenancy"
- "Plan a migration strategy for adding a new column to a 100M row table"

## Capabilities
- Analyzes existing schemas and migrations
- Creates step-by-step migration plans
- Generates safe SQL migration scripts
- Tests migrations in controlled environments
- Handles zero-downtime migrations
- Manages rollback strategies
- Validates data integrity throughout

## Input
- Current database schema (SQL/DDL)
- Target schema design
- Database constraints and size info
- Availability requirements
- Timeline and resource constraints

## Output
- Migration strategy document
- Step-by-step execution plan
- Tested SQL migration scripts
- Rollback procedures
- Data validation scripts
- Post-migration verification checklist

## When to use
- Planning schema changes
- Zero-downtime migrations
- Complex structural changes
- Data transformation requirements
- Multi-version compatibility needs

## Tips
- Provide complete schema information for best results
- Test recommendations in staging first
- Use for any migration touching production data
- Always have a rollback plan ready
