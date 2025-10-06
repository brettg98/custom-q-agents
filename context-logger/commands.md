# Context Agent Commands

## Common Usage Patterns

### Initialize Project Context
"Create a new context file for [event/session name]"

### Add Information
"Add to context: [information]"
"Record decision: [decision details]"
"Add note about [topic]: [details]"

### Retrieve Information
"Show me the recent context files"
"What decisions have been made?"
"Show me notes about [topic]"

### Update Context
"Update context with: [new information]"
"Add follow-up to [date] context: [details]"
"Create new context file for [session/event]"

### Search Context
"Find information about [topic]"
"Show me context files related to [keyword]"

### Comprehensive Context Creation
"Document today's work on [topic]. Include the specific files changed, the approach we used, what's completed vs. remaining, and reference any related requests in .orbit/requests/"

"Create context for [session] including before/after comparison, decision rationale, and next steps for the team"

"Log this work session with technical details: file paths modified, commands executed, current state vs. remaining work, and cross-references to related requests"

## File Organization
- Context files use format `YYYY-MM-DD-context-name.md`
- Stored in `.orbit/context/` directory
- Use timestamps for decision tracking
- Organize information in clear sections
- Use markdown formatting for readability
