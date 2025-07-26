# Extending the Base Profile

Use this checklist when creating a new specialized profile:

## Pre-Setup
- [ ] Identify the target development scenario (e.g., "TypeScript + NextJS", "Python + Data Science")
- [ ] Create a new directory: `vscode/profiles/{scenario-name}`
- [ ] Copy all files from the base profile to the new profile directory

## Settings Configuration (`settings.json`)
- [ ] Review base settings and identify any that need language-specific overrides
- [ ] Add language server configurations (e.g., TypeScript, Python, Rust analyzer)
- [ ] Configure language-specific formatting settings
- [ ] Add file associations for specialized file types
- [ ] Set default formatters for the target languages
- [ ] Configure language-specific IntelliSense settings
- [ ] Add any framework-specific settings (e.g., Next.js, Django, React)

## Extensions (`extensions.json`)
- [ ] Add language-specific extensions (e.g., Python, TypeScript, Rust)
- [ ] Add framework-specific extensions (e.g., Next.js, React, Vue)
- [ ] Add debugging extensions if needed (e.g., Python Debugger, C/C++)
- [ ] Add testing framework extensions (e.g., Jest, pytest)
- [ ] Add linting extensions (e.g., ESLint, Pylint, Clippy)
- [ ] Add language-specific productivity extensions
- [ ] Remove any base extensions that conflict or are unnecessary

## Key Bindings (`keybindings.json`)
- [ ] Add language-specific shortcuts (e.g., run Python file, compile Rust)
- [ ] Add framework-specific shortcuts (e.g., Next.js dev server)
- [ ] Add testing shortcuts (e.g., run tests, debug tests)
- [ ] Add build/compile shortcuts
- [ ] Override any base shortcuts that conflict

## Tasks (`tasks.json`) - Create New File
- [ ] Create `tasks.json` file
- [ ] Add "Install Dependencies" task (npm/pip/cargo install)
- [ ] Add "Build" task appropriate for the language/framework
- [ ] Add "Test" task for running unit tests
- [ ] Add "Lint" task for code quality checks
- [ ] Add "Format" task for code formatting
- [ ] Add "Start Dev Server" task if applicable
- [ ] Add "Deploy" or "Publish" tasks if needed
- [ ] Configure appropriate problem matchers for each task

## Launch Configurations (`launch.json`) - Create New File
- [ ] Create `launch.json` file
- [ ] Add "Launch Current File" configuration
- [ ] Add "Launch Application" configuration
- [ ] Add "Debug Tests" configuration
- [ ] Add "Attach to Process" configuration if needed
- [ ] Add framework-specific debug configurations (e.g., Next.js, Django)
- [ ] Configure environment variables if needed
- [ ] Set up source maps if applicable (TypeScript, etc.)

## Snippets
- [ ] Create language-specific snippet files in `snippets/` directory
- [ ] Add common language patterns (e.g., Python classes, TS interfaces)
- [ ] Add framework-specific snippets (e.g., React components, Flask routes)
- [ ] Add testing snippets (e.g., test functions, mock setups)
- [ ] Add documentation snippets specific to the language/framework
- [ ] Update global snippets if needed for the specific use case

## Documentation
- [ ] Create or update README.md for the specialized profile
- [ ] Document the target development scenario
- [ ] List all included extensions and their purposes
- [ ] Document any special setup requirements
- [ ] Include usage examples and common workflows
- [ ] Document any custom key bindings or tasks
- [ ] Add troubleshooting section if needed

## Testing & Validation
- [ ] Test the profile in a sample project
- [ ] Verify all extensions install correctly
- [ ] Test all custom key bindings
- [ ] Run all defined tasks to ensure they work
- [ ] Test debugging configurations
- [ ] Verify code formatting and linting work
- [ ] Test IntelliSense and language server features
- [ ] Validate that snippets render correctly

## Finalization
- [ ] Clean up any unused or conflicting settings
- [ ] Optimize performance settings for the specific use case
- [ ] Update the main profiles documentation to include the new profile
- [ ] Consider creating installation/setup scripts if complex
