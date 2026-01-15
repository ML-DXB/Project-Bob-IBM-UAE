# Bob Instructions for Bootcamp Template

This file contains instructions specifically for Bob on how to use and work with this bootcamp template.

## 🎯 Purpose

This template helps you (Bob) assist facilitators in preparing and delivering customized bootcamps for clients. You should read the `bootcamp-config.yaml` file to understand the client's context and use it to provide tailored assistance.

## 📖 How to Use This Template

### Step 1: Read the Configuration
When a user asks for help with a bootcamp, first read the configuration:

```
Read bootcamp-config.yaml to understand the client's context
```

This file contains:
- Client name and industry
- Technology stack
- Key use cases and priorities
- Schedule and timing
- Participant information
- Success criteria

### Step 2: Understand the Context
Based on the configuration, you should:
1. Identify the client's primary technology stack
2. Note their key use cases and priorities
3. Understand their industry-specific requirements
4. Review their schedule preferences

### Step 3: Provide Tailored Assistance
Use the configuration to:
- Customize lab exercises for their tech stack
- Suggest relevant examples from their industry
- Adjust timing based on their schedule
- Reference their specific tools and frameworks

## 🔧 Common Tasks

### Task: Customize Lab Exercises
When asked to customize labs:
1. Read `bootcamp-config.yaml` for client context
2. Read the relevant lab instructions file
3. Update exercises to use client's tech stack
4. Add client-specific examples
5. Adjust difficulty based on participant skill levels

Example:
```
"Customize Lab 1 for this client based on their bootcamp-config.yaml"
```

### Task: Generate Schedule
When asked to create or modify schedule:
1. Read `bootcamp-config.yaml` for timing preferences
2. Read `schedule/detailed-agenda.md` for template
3. Adjust timing based on client needs
4. Ensure use cases fit within time blocks
5. Account for breaks and transitions

### Task: Create Client-Specific Use Cases
When asked to develop use cases:
1. Read `bootcamp-config.yaml` for client's use cases
2. Read `labs/lab3-client-specific/instructions.md` for template
3. Create detailed scenarios using client's tech stack
4. Include actual business problems from their domain
5. Provide step-by-step Bob workflows

### Task: Prepare Facilitator Materials
When asked to help prepare:
1. Read `bootcamp-config.yaml` for full context
2. Review `schedule/detailed-agenda.md`
3. Check all lab instructions
4. Verify examples match client's stack
5. Suggest additional resources from `resources/external-links.md`

## 📋 File Structure Reference

### Configuration Files
- `bootcamp-config.yaml` - **START HERE** - Main client configuration
- `README.md` - Human-readable instructions (also has YAML frontmatter for you)

### Schedule Files
- `schedule/detailed-agenda.md` - Detailed timing breakdown

### Lab Files
- `labs/lab1-basic-operations/instructions.md` - Beginner lab
- `labs/lab2-advanced-workflows/instructions.md` - Intermediate lab
- `labs/lab3-client-specific/instructions.md` - Advanced lab (customize this!)

### Resource Files
- `resources/cheat-sheet.md` - Quick reference
- `resources/troubleshooting.md` - Common issues
- `resources/external-links.md` - Learning resources

### Example Files
- `examples/sample-config-fintech.yaml` - Financial services example
- `examples/sample-config-healthcare.yaml` - Healthcare example

## 🎯 Key Principles

### 1. Always Read Configuration First
Before providing any bootcamp-related assistance, read `bootcamp-config.yaml` to understand:
- Who the client is
- What technologies they use
- What problems they're trying to solve
- What their constraints are

### 2. Tailor Everything to the Client
Don't provide generic examples. Use:
- Their programming language
- Their frameworks
- Their industry terminology
- Their actual use cases

### 3. Respect Time Constraints
The default is 6 hours, but check the config:
- Morning: 3 hours (intro + basic + advanced)
- Lunch: 1 hour
- Afternoon: 3 hours (client-specific + wrap-up)

### 4. Focus on Value
Prioritize use cases marked as "high" priority in the config. These are what the client cares most about.

### 5. Be Practical
Use real examples from their codebase when possible. Reference their actual:
- Repositories
- APIs
- Documentation
- Tools and infrastructure

## 💡 Example Workflows

### Example 1: Customizing Lab 1
```
User: "Customize Lab 1 for our Python/Django client"

Bob should:
1. Read bootcamp-config.yaml
2. Note: Python, Django, PostgreSQL stack
3. Read labs/lab1-basic-operations/instructions.md
4. Update exercises to use Django models, views, tests
5. Add Django-specific examples
6. Reference client's actual project structure if available
```

### Example 2: Creating Client-Specific Scenarios
```
User: "Create Lab 3 exercises for our fintech client"

Bob should:
1. Read bootcamp-config.yaml
2. Note: Financial services, payment processing use case
3. Read labs/lab3-client-specific/instructions.md
4. Create scenarios like:
   - Implementing payment validation
   - Adding fraud detection
   - Creating audit logs
   - Handling PCI compliance
5. Use their actual tech stack (Java/Spring Boot)
```

### Example 3: Adjusting Schedule
```
User: "We only have 4 hours, adjust the schedule"

Bob should:
1. Read bootcamp-config.yaml
2. Read schedule/detailed-agenda.md
3. Compress to 4 hours:
   - Intro: 20 min
   - Basic: 60 min
   - Advanced: 40 min
   - Client-specific: 90 min
   - Wrap-up: 10 min
4. Prioritize high-priority use cases
5. Suggest what to skip or do as homework
```

## 🚨 Important Notes

### Security and Compliance
Some clients have special requirements:
- **Financial Services**: PCI-DSS, SOC2 compliance
- **Healthcare**: HIPAA, PHI handling
- **Government**: Security clearances, air-gapped environments

Check the `notes` section in `bootcamp-config.yaml` for these requirements.

### Technology Constraints
Some clients have specific constraints:
- Network restrictions
- Approved tools only
- Legacy systems
- Specific versions

Always check the `technologies` and `notes` sections.

### Participant Skill Levels
Adjust complexity based on `participants.skill_levels`:
- More juniors → slower pace, more explanation
- More seniors → faster pace, advanced topics
- Mixed → provide optional advanced content

## 📚 Quick Reference

### Must-Read Files
1. `bootcamp-config.yaml` - Always read this first
2. Relevant lab instructions
3. Schedule if timing questions

### Optional Files
- Examples for inspiration
- Resources for additional context
- Troubleshooting for common issues

### When to Read Multiple Files
Read together when:
- Customizing labs (config + lab instructions)
- Adjusting schedule (config + schedule + labs)
- Creating materials (config + all relevant files)

## 🎓 Best Practices for Bob

1. **Be Specific**: Use client's actual tech stack, not generic examples
2. **Be Practical**: Reference their real code, APIs, and tools
3. **Be Efficient**: Read multiple related files together
4. **Be Thorough**: Check all relevant sections of config
5. **Be Helpful**: Suggest improvements based on client context

## 🔄 Workflow Summary

```
User Request
    ↓
Read bootcamp-config.yaml
    ↓
Understand client context
    ↓
Read relevant template files
    ↓
Customize for client
    ↓
Provide tailored assistance
```

## 📞 Common Questions

**Q: What if the config is incomplete?**
A: Ask the user for missing information, referencing the template structure.

**Q: What if the client uses an unusual tech stack?**
A: Adapt the examples to their stack, maintaining the same learning objectives.

**Q: What if timing doesn't fit?**
A: Suggest adjustments, prioritizing high-priority use cases.

**Q: What if labs don't match client needs?**
A: Create custom exercises based on their actual use cases.

---

**Remember**: Your goal is to help deliver a bootcamp that's perfectly tailored to each client's needs, technology stack, and business objectives. Always start with `bootcamp-config.yaml`!