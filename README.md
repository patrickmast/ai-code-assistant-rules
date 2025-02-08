# AI Code Assistant Rules

This directory contains the local copy of the AI code assistant rules. These rules are synchronized from the central repository at [github.com/patrickmast/ai-code-assistant-rules](https://github.com/patrickmast/ai-code-assistant-rules).

## Directory Structure

```
.
├── README.md                 # This file
├── task-identification.md    # Core rules for identifying task types
├── read-only-tasks/         # Rules for tasks that don't modify code
│   ├── suggestion-mode.md
│   └── debugging-analysis.md
├── modification-tasks/      # Rules for tasks that modify code
│   ├── enhancement.md
│   ├── bug-fix.md
│   ├── refactor.md
│   └── testing.md
├── documentation-tasks/     # Rules for documentation-related tasks
│   ├── documentation.md
│   └── commit.md
└── transitions/            # Rules for transitioning between task types
    ├── debugging-to-fix.md
    └── enhancement-to-refactor.md
```

## Updating Rules

These rules are maintained in a separate GitHub repository. To update this local copy with the latest rules, ask:

```
"Update the global rules from https://github.com/patrickmast/ai-code-assistant-rules"
```

## Contributing

To contribute to these rules:

1. Fork the main rules repository
2. Make your changes
3. Submit a pull request
4. Once merged, request an update of the global rules using the command above

## Note

Do not modify these files directly. All changes should be made in the central GitHub repository and then synchronized to these local files.
