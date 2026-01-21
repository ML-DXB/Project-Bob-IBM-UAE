# Bootcamp Builder Mode - Installation and Usage Guide

## 🎯 Overview

The **Bootcamp Builder** mode is a custom Bob mode that guides you through creating customized bootcamps for clients. It provides:

- **Interactive Q&A** to gather client information
- **Automatic validation** to ensure completeness
- **Smart customization** of labs and materials
- **Quality assurance** checks before delivery

## 📦 Installation

The Bootcamp Builder mode is already included in this template! The mode configuration is in the `.bobmodes` file at the root of this project.

### Verify Installation

1. Open this project in VS Code with Bob installed
2. Look for the mode selector in Bob's interface
3. You should see "🎓 Bootcamp Builder" in the list of available modes

### If the Mode Doesn't Appear

If you don't see the Bootcamp Builder mode:

1. **Reload VS Code Window:**
   - Press `Ctrl+Shift+P` (Windows/Linux) or `Cmd+Shift+P` (Mac)
   - Type "Reload Window" and press Enter
   - Bob will reload and detect the `.bobmodes` file

2. **Check the .bobmodes file:**
   - Ensure `.bobmodes` exists in the workspace root
   - Verify it contains the `bootcamp-builder` mode configuration

3. **Restart Bob:**
   - Close and reopen VS Code
   - Bob should detect the custom mode on startup

## 🚀 Quick Start

### Step 1: Switch to Bootcamp Builder Mode

1. Open Bob in VS Code
2. Click the mode selector (shows current mode like "💻 Code" or "❓ Ask")
3. Select "🎓 Bootcamp Builder" from the list

### Step 2: Start Creating a Bootcamp

Once in Bootcamp Builder mode, you can:

**Option A: Create from Scratch**
```
Help me create a new bootcamp for [Client Name]
```

**Option B: Start from an Example**
```
I want to create a bootcamp based on the Financial Services example
```

**Option C: Customize Existing Config**
```
Customize the labs for the client in bootcamp-config.yaml
```

### Step 3: Answer the Questions

Bob will guide you through a series of questions:

1. **Client Information**
   - Company name and industry
   - Primary contact details

2. **Technology Stack**
   - Programming language
   - Frameworks and tools
   - Infrastructure (AWS, Azure, etc.)

3. **Lab Technology Preference**
   - Should Labs 1 & 2 (basic Bob features) use the same technology as the client?
   - Or use generic examples that work across languages?
   - This helps ensure labs are relevant to the client's daily work

4. **Use Cases**
   - What problems to solve
   - Priority levels
   - Time estimates

5. **Schedule**
   - Total duration (3, 6, or 12 hours)
   - Date and timezone
   - Timing preferences

6. **Participants**
   - Team size
   - Roles and skill levels
   - Prerequisites

### Step 4: Review and Validate

After gathering information, Bob will:
- Generate `bootcamp-config.yaml`
- Validate completeness
- Check for consistency
- Offer to customize labs

### Step 5: Customize Materials

Choose what to customize:
- **Lab 1:** Basic operations for their tech stack
- **Lab 2:** Advanced workflows for their tech stack
- **Lab 3:** Client-specific scenarios based on use cases
- **Schedule:** Detailed agenda with timing

### Step 6: Save Your Bootcamp

Once everything is complete and validated, Bob will ask how you want to save the bootcamp:

**Option 1: Export to New Directory (Recommended)**
- Creates a clean, standalone bootcamp in `../{client-name}-bootcamp/`
- Optionally removes template files (.bob/, .bobmodes, examples/)
- Ready to initialize as a new git repository
- Perfect for client delivery

**Option 2: Prepare for New Repository**
- Creates a branch with your changes
- Asks for target repository URL
- Provides exact git commands to push
- Optionally cleans up template files

**Option 3: Create Branch in This Repo**
- Keeps bootcamp with template for easy updates
- Creates branch like `bootcamp-acme-corp`
- All bootcamps in one repository
- Easy to switch between clients

**Option 4: Commit to Current Branch**
- Simple commit to current branch
- You handle git workflow manually
- Good for quick iterations

## 📋 Common Workflows

### Workflow 1: Complete New Bootcamp Setup

```
User: "Create a new bootcamp for Acme Financial Services"

Bob will ask about:
1. Industry and contact info
2. Tech stack (Java, Spring Boot, etc.)
3. Lab technology preference:
   "Should Labs 1 & 2 use Java/Spring Boot like your client work,
    or generic examples? Using client tech makes labs more relevant
    but takes more customization time."
4. Key use cases (API development, security, etc.)
5. Duration and schedule
6. Team composition

Then Bob will:
- Generate bootcamp-config.yaml
- Customize labs based on technology preference
- Ask about code generation preference:
  * Generate both starter code and solutions (recommended)
  * Generate starter code only
  * No code generation (manual creation)
- Create Lab 3 scenarios
- Validate everything
```

### Workflow 2: Customize Labs Only

```
User: "Customize all labs for the client in bootcamp-config.yaml"

Bob will:
1. Read the existing config
2. Update Lab 1 with client's tech stack
3. Update Lab 2 with client's tech stack
4. Ask about code generation preference
5. Generate sample code if requested
6. Create Lab 3 scenarios from use cases
7. Validate consistency
```

### Workflow 3: Validate Existing Bootcamp

```
User: "Validate the bootcamp materials"

Bob will:
1. Read all bootcamp files
2. Check required fields
3. Verify timing calculations
4. Ensure tech stack consistency
5. Detect placeholders
6. Report findings
7. Offer to fix issues
```

### Workflow 4: Adjust Schedule

```
User: "We only have 4 hours instead of 6, adjust the schedule"

Bob will:
1. Read current config
2. Recalculate timing
3. Prioritize high-value use cases
4. Suggest what to skip
5. Update schedule
6. Validate new timing

### Workflow 5: Save Completed Bootcamp

```
User: Bootcamp is complete and validated

Bob will first ask:
"Would you like to update external resources and contact information?"

Options:
1. I'll edit them myself (default)
   - Bob provides file locations and line numbers
   - You manually update placeholders

2. Have Bob update them
   - Bob asks for documentation URLs
   - Bob asks for support contact info
   - Bob updates both files automatically
   - Handles unknown items (placeholder/delete/skip)

3. Skip for now
   - Keep template placeholders
   - Update before delivery

Then Bob will ask:
"How would you like to save it?"

Options:
1. Export to new directory (../acme-corp-bootcamp/)
   - Creates clean, standalone bootcamp
   - Optionally removes template files
   - Provides git init instructions

2. Prepare for new repository
   - Asks for target repo URL
   - Creates branch and commits
   - Provides exact push commands

3. Create branch in this repo
   - Branch: bootcamp-acme-corp
   - Keeps with template
   - Easy to maintain multiple clients

4. Commit to current branch
   - Simple commit
   - Manual git workflow
```

**Example: Update Resources with Bob**
```
Bob: "Would you like to update external resources and contact information?"
User: "Have Bob update them"

Bob: "What are your Bob documentation URLs?"
User: "Main docs: https://docs.bob.com, API: https://api.bob.com"

Bob: "Do you have company-specific resources to add?"
User: "Yes, internal wiki: https://wiki.acme.com/bob"

Bob: "What are the after-bootcamp support contact details?"
User: "Email: bob-support@acme.com, Slack: #bob-help, Office hours: Mon-Fri 2-4pm EST"

Bob will:
1. Update resources/external-links.md with documentation links
2. Add company resources to external-links.md
3. Update resources/troubleshooting.md with support contacts
4. Report what was updated and any remaining placeholders
```

**Example: Export to New Directory**
```
Bob: "Should I remove template-specific files?"
User: "Yes, create a clean bootcamp"

Bob will:
1. Create ../acme-corp-bootcamp/
2. Copy bootcamp files
3. Remove .bob/, .bobmodes, examples/
4. Provide git commands:
   cd ../acme-corp-bootcamp
   git init
   git add .
   git commit -m "Initial bootcamp for Acme Corp"
   git remote add origin [your-url]
   git push -u origin main
```

**Example: Prepare for New Repository**
```
Bob: "What's the target repository URL?"
User: "https://github.com/myorg/acme-bootcamp.git"

Bob: "Remove template files?"
User: "Yes"

Bob will:
1. Create branch bootcamp-acme-corp
2. Remove template files
3. Commit changes
4. Provide commands:
   git remote add acme https://github.com/myorg/acme-bootcamp.git
   git push acme bootcamp-acme-corp:main
```
```

## 💡 Tips for Best Results

### 1. Be Specific
Instead of: "Create a bootcamp"
Try: "Create a bootcamp for a healthcare client using Python and Django"

### 2. Use the Suggestions
Bob provides 2-4 suggestions for each question - use them to save time!

### 3. Start from Examples
If your client is similar to an example, start there:
- Financial Services → `examples/sample-config-fintech.yaml`
- Healthcare → `examples/sample-config-healthcare.yaml`

### 4. Choose Lab Technology Wisely
**Use client technology for Labs 1 & 2 when:**
- Client uses a specific, less common language/framework
- Team is new to their tech stack and needs practice
- You have time for full customization
- Examples in client's tech will be more engaging

**Use generic examples when:**
- Client uses common languages (Python, JavaScript, Java)
- Time is limited (3-hour bootcamp)
- Focus is on Bob concepts, not language specifics
- Team is experienced with their stack

### 5. Code Generation Options
**Generate both starter code and solutions (recommended) when:**
- You want a complete, ready-to-deliver bootcamp
- Facilitators need reference implementations
- Participants benefit from seeing working examples
- Time allows for code review and customization

**Generate starter code only when:**
- You want participants to build solutions during the bootcamp
- Focus is on learning by doing
- Facilitators are comfortable creating solutions on the fly

**Skip code generation when:**
- You have existing code samples to use
- Labs will use client's actual codebase
- You prefer to create code manually

### 6. Validate Before Delivery
Always run validation before considering the bootcamp complete:
```
Validate the bootcamp materials and fix any issues
```

### 6. Iterate as Needed
You can always ask Bob to adjust:
```
The Lab 3 scenarios are too complex, simplify them
Add more time to the API development use case
Change the tech stack from Java to Python
```

## 🎓 Understanding the Mode

### What the Mode Can Do

✅ **Read and analyze:**
- Bootcamp configuration
- Lab instructions
- Schedule files
- Example configs
- Resource files

✅ **Edit and create:**
- `bootcamp-config.yaml`
- Lab instructions (`labs/*.md`)
- Schedule files (`schedule/*.md`)
- Example configs (`examples/*.yaml`)
- Resource files (`resources/*.md`)

✅ **Execute commands:**
- Validation scripts
- File operations
- Testing commands

### What the Mode Cannot Do

❌ **Cannot edit:**
- Files outside the bootcamp template
- System files
- Unrelated project files

❌ **Cannot access:**
- External APIs (unless via MCP)
- Network resources
- Browser actions

### Mode Restrictions

The mode is restricted to bootcamp-related files for safety:
- Prevents accidental changes to other files
- Ensures focus on bootcamp preparation
- Maintains template integrity

## 🔍 Troubleshooting

### Issue: Mode Not Appearing

**Solution:**
1. Verify `.bobmodes` file exists in workspace root
2. Reload VS Code window
3. Check Bob is properly installed and activated

### Issue: Bob Asks Too Many Questions

**Solution:**
- This is intentional! The mode gathers complete information upfront
- Use the suggestions to answer quickly
- You can provide multiple answers at once:
  ```
  Client: Acme Corp, Financial Services
  Tech: Java, Spring Boot, PostgreSQL
  Use cases: API development, security compliance, testing
  ```

### Issue: Generated Config Has Errors

**Solution:**
1. Ask Bob to validate: "Validate the bootcamp materials"
2. Bob will identify and fix issues
3. Review the validation report

### Issue: Labs Don't Match Tech Stack

**Solution:**
```
The labs still use Python but our client uses Java. 
Please update all labs to use Java and Spring Boot.
```

### Issue: Timing Doesn't Fit

**Solution:**
```
We have 4 hours instead of 6. Adjust the schedule and 
prioritize the high-priority use cases.
```

## 📚 Additional Resources

### Mode Documentation
- `.bob/rules-bootcamp-builder/1_workflow.xml` - Detailed workflows
- `.bob/rules-bootcamp-builder/2_validation_rules.xml` - Validation rules
- `.bob/rules-bootcamp-builder/3_best_practices.xml` - Best practices

### Template Documentation
- `README.md` - Main template documentation
- `.bob/instructions.md` - General Bob instructions
- `schedule/detailed-agenda.md` - Schedule template
- `resources/cheat-sheet.md` - Bob quick reference

### Examples
- `examples/sample-config-fintech.yaml` - Financial services example
- `examples/sample-config-healthcare.yaml` - Healthcare example

## 🎯 Success Checklist

Before delivering a bootcamp, ensure:

- [ ] `bootcamp-config.yaml` is complete (no placeholders)
- [ ] All labs use client's tech stack
- [ ] Lab 3 addresses client's use cases
- [ ] Sample code generated (if requested)
- [ ] Starter code exists in labs/*/starter/ directories
- [ ] Solution code exists in labs/*/solution/ directories (if requested)
- [ ] README files exist in starter directories
- [ ] Generated code matches client's tech stack
- [ ] Timing calculations are correct
- [ ] Schedule matches available time
- [ ] All materials are consistent
- [ ] Validation passes with no errors
- [ ] Examples are specific to client
- [ ] No generic placeholders remain

## 🤝 Getting Help

### During Bootcamp Preparation

Ask Bob directly:
```
How do I customize Lab 2 for a Django project?
What's the best way to structure Lab 3 scenarios?
Can you explain the validation errors?
Generate sample code for Lab 1 using Python and Flask
Should I generate solutions or just starter code?
```

### After Bootcamp Delivery

- Review participant feedback
- Update template based on learnings
- Share improvements with team
- Document lessons learned

## 📞 Support

If you encounter issues with the Bootcamp Builder mode:

1. **Check this guide** for common solutions
2. **Review the mode documentation** in `.bob/rules-bootcamp-builder/`
3. **Ask Bob for help** - it can explain its own capabilities
4. **Contact support** - [your support channel]

## 🎉 You're Ready!

You now know how to:
- ✅ Install and activate the Bootcamp Builder mode
- ✅ Create new bootcamps from scratch
- ✅ Customize labs and materials
- ✅ Validate bootcamp quality
- ✅ Troubleshoot common issues

**Next Step:** Switch to Bootcamp Builder mode and create your first bootcamp!

```
Help me create a new bootcamp for [Your Client Name]
```

---

**Version:** 1.0.0  
**Last Updated:** 2026-01-15  
**Template:** Bob Client Bootcamp Starter