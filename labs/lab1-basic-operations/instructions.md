# Lab 1: Basic Bob Operations

**Duration:** 30 minutes  
**Difficulty:** Beginner  
**Prerequisites:** Bob installed and running

## 🎯 Objectives

By the end of this lab, you will be able to:
- Navigate and read files in a codebase
- Search for specific code patterns
- Make simple code changes using Bob
- Execute commands and verify results
- Understand when to use different Bob tools

## 📋 Setup

Before starting, ensure you have:
- [ ] Bob running in your IDE
- [ ] Access to the sample project (provided by facilitator)
- [ ] Basic understanding of the programming language used

## 🔨 Exercises

### Exercise 1: File Navigation and Reading (5 minutes)

**Scenario:** You've just joined a project and need to understand the codebase structure.

**Tasks:**
1. List all files in the project directory
2. Read the main configuration file
3. Identify the entry point of the application

**Bob Tools to Use:**
- `list_files` - To see directory structure
- `read_file` - To view file contents

**Example Prompt:**
```
Please list all files in the current directory recursively, then read the main configuration file.
```

**Expected Outcome:**
- You can see the project structure
- You understand where key files are located
- You've read at least one configuration file

---

### Exercise 2: Code Search and Discovery (5 minutes)

**Scenario:** You need to find all places where a specific function is called.

**Tasks:**
1. Search for all TODO comments in the codebase
2. Find all files that import a specific module
3. Locate a function definition by name

**Bob Tools to Use:**
- `search_files` - To find patterns across files
- `list_code_definition_names` - To see function/class names

**Example Prompt:**
```
Search for all TODO comments in the src directory. Then list all code definitions in the utils.py file.
```

**Expected Outcome:**
- You've found all TODO comments
- You understand how to search for patterns
- You can locate specific code definitions

---

### Exercise 3: Simple Code Changes (10 minutes)

**Scenario:** You need to update a configuration value and fix a simple bug.

**Tasks:**
1. Update a configuration value in a JSON/YAML file
2. Fix a typo in a function name
3. Add a new import statement to a file

**Bob Tools to Use:**
- `write_to_file` - For complete file rewrites (small files)
- `apply_diff` - For targeted changes (preferred)
- `insert_content` - For adding new lines

**Example Prompt:**
```
In the config.json file, change the "debug" value from false to true. Then in src/app.py, fix the typo in the function name "calcualte_total" to "calculate_total".
```

**Expected Outcome:**
- Configuration value updated correctly
- Typo fixed without breaking other code
- You understand the difference between editing tools

---

### Exercise 4: Command Execution (5 minutes)

**Scenario:** You need to run tests and check the application status.

**Tasks:**
1. Run the test suite
2. Check the application version
3. List installed dependencies

**Bob Tools to Use:**
- `execute_command` - To run CLI commands

**Example Prompt:**
```
Run the test suite using pytest. Then show me the application version from package.json.
```

**Expected Outcome:**
- Tests executed successfully
- You can interpret test results
- You understand how to run commands through Bob

---

### Exercise 5: Multi-Step Workflow (5 minutes)

**Scenario:** Combine multiple operations to complete a task.

**Tasks:**
1. Find a function that needs updating
2. Read the function to understand it
3. Make an improvement to the function
4. Run tests to verify the change

**Example Prompt:**
```
Find the calculate_total function in src/utils.py, read it, then update it to include a 10% tax calculation. After making the change, run the tests to verify it works.
```

**Expected Outcome:**
- You can break down complex tasks
- You understand the workflow: read → modify → verify
- You're comfortable with multi-step operations

---

## 🎓 Key Takeaways

After completing this lab, you should understand:

1. **File Operations**
   - `list_files` for navigation
   - `read_file` for viewing content
   - Always read before modifying

2. **Search and Discovery**
   - `search_files` for pattern matching
   - `list_code_definition_names` for code structure
   - Use regex for powerful searches

3. **Code Editing**
   - `apply_diff` for precise changes (preferred)
   - `write_to_file` for new files or complete rewrites
   - `insert_content` for adding lines
   - Always provide context to Bob

4. **Command Execution**
   - `execute_command` for CLI operations
   - Verify changes by running tests
   - Use commands to gather information

5. **Best Practices**
   - Be specific in your prompts
   - Provide context about what you're trying to achieve
   - Break complex tasks into steps
   - Verify changes after making them

## 💡 Tips for Success

1. **Start Simple:** Begin with read operations before making changes
2. **Be Specific:** Clear prompts get better results
3. **Provide Context:** Tell Bob what you're trying to accomplish
4. **Verify Changes:** Always check that changes work as expected
5. **Ask Questions:** If something isn't clear, ask Bob to explain

## 🐛 Common Issues

### Issue: Bob can't find a file
**Solution:** Use `list_files` first to see the correct path

### Issue: Changes didn't apply correctly
**Solution:** Use `read_file` to see the current state, then try again with exact content

### Issue: Command failed
**Solution:** Check the error message and adjust the command syntax

### Issue: Not sure which tool to use
**Solution:** Ask Bob! "What's the best way to [accomplish task]?"

## 📝 Discussion Questions

1. When would you use `write_to_file` vs `apply_diff`?
2. How can you make your prompts more effective?
3. What's the benefit of breaking tasks into steps?
4. How do you verify that changes work correctly?

## ✅ Completion Checklist

- [ ] Completed Exercise 1: File Navigation
- [ ] Completed Exercise 2: Code Search
- [ ] Completed Exercise 3: Simple Code Changes
- [ ] Completed Exercise 4: Command Execution
- [ ] Completed Exercise 5: Multi-Step Workflow
- [ ] Understand when to use each Bob tool
- [ ] Can write effective prompts
- [ ] Comfortable with basic Bob operations

## 🚀 Next Steps

Once you've completed this lab:
1. Review the solutions in the `solution/` directory
2. Try the exercises again with different scenarios
3. Move on to Lab 2: Advanced Workflows
4. Practice with your own code examples

## 📚 Additional Resources

- Bob Documentation: [Link to docs]
- Tool Reference Guide: See `resources/cheat-sheet.md`
- Troubleshooting: See `resources/troubleshooting.md`

---

**Need Help?** Ask your facilitator or use the dedicated support channel!