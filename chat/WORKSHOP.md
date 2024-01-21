# Copilot Chat

Remember to **DISCONNECT VPN**.

## Agents and Commands

* `@workspace` - Ask about your workspace
	* `/explain` - Explain how the selected code works
	* `/tests`- Generate unit tests for the selected code
	* `/fix`- Propose a fix for the problems in the selected code
	* `/new`- Scaffold code for a new workspace
	* `/newNotebook` - Create a new Jupyter Notebook
* `@vscode` - Ask about VS Code
	* `/search` - Generate query parameters for workspace search
	* `/api` - Ask about VS Code extension development
* `@terminal` - Ask how to do something in the terminal
* `/help` - General help about GitHub Copilot.
* `/clear` - Clear the session.

## sherlock

Go to `cd chat/sherlock` directory and run the application. **Objectives:** Figure out how to work with the project.

```
@workspace what is sherlock?
@workspace how to install sherlock locally?
@workspace how to install sherlock with docker?
```

Open [run.py](sherlock/app/run.py) file. **Objecives:** create unit test.

```
# Select recommend and alive functions
@workspace /tests only with pytest module.
```

Open [Dockerfile](sherlock/Dockerfile) file. **Objectives:** apply best practices to Dockerfile. Find difference between GPT gpt-3.5-turbo vs gpt-4

```
# Select FROM instruction `Ctrl + I`
What is the lates python image that I can use?

# Ports
Expose port
Expose port but use variable syntax

# Rootless
Make Dockerfile rootless
Secure Dockerfile with nobody and nogroup user
Explaing user and group id ranges in Linux. Show results as a table

# Select RUN apk add curl
Remove application chache an cache dir

# HEALTHCHECK
Implement application HEALTHCHECK with default intervals
```

Open [run.py](sherlock/app/run.py) file. **Objectives:** refactor application.

```
# Select whole file
Does this code violates SOLID principles?

# Select recommended and alive functions
Refactor

# Select recommend functions
Implement a decorator to handle errors
```

Open [rengine.py](sherlock/app/rengine.py) file. **Objectives:** refactor application.

```
# Select all
Propose a better variables name

# Select all
Refactor this code to more generic implementation

Add pep8 docs string

Use Python annotations to document methods in this code

Comment every line in the recommend method with time complexity. Estimate the total time complexity of the recommend method.
```

## Links

- https://www.desmos.com/calculator/xpfyjl1lbn
- https://victoria.dev/blog/a-coffee-break-introduction-to-time-complexity-of-algorithms/
- https://docs.github.com/en/copilot/configuring-github-copilot/configuring-github-copilot-in-your-environment?tool=vscode
- https://learn.microsoft.com/en-us/visualstudio/ide/visual-studio-github-copilot-chat?view=vs-2022