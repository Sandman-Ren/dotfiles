# VS Code Base Profile

This is the foundational profile for all development scenarios. It provides essential settings, extensions, and configurations that are useful across all programming languages and frameworks.

## What's Included

### Core Settings (`settings.json`)
- **Editor Configuration**: Font settings (JetBrains Mono with ligatures), line numbers, rulers, formatting
- **Terminal Integration**: PowerShell as default shell with proper font settings
- **File Handling**: UTF-8 encoding, auto-save, trim whitespace, final newlines
- **Git Integration**: Smart commit, auto-fetch, decorations
- **Performance Optimizations**: File watching exclusions, search exclusions
- **Security Settings**: Workspace trust configuration
- **IntelliSense**: Optimized suggestion settings

### Key Bindings (`keybindings.json`)
- **Terminal Management**: Create new terminal, focus terminal
- **File Navigation**: Quick open, command palette, symbol search
- **Editor Management**: Split editors, close tabs, navigate between editors
- **Multi-cursor Editing**: Insert cursors, select occurrences
- **Code Actions**: Quick fix, format, organize imports, rename
- **Git Operations**: Source control view, commit, push, pull
- **Debugging**: Start, stop, step through, breakpoints

### Essential Extensions (`extensions.json`)
- **AI & Productivity**: GitHub Copilot, Copilot Chat
- **Git & Version Control**: GitLens, GitHub Pull Requests
- **Code Quality**: Prettier, EditorConfig, Error Lens, TODO Tree
- **File Support**: YAML, XML, Markdown, CSV
- **Development Tools**: Thunder Client (API testing), Live Server
- **UI Enhancements**: Better Comments, Bookmarks, Indent Rainbow

### Code Snippets
- **Global Snippets**: Header comments, function documentation, TODO/FIXME/NOTE comments, common code patterns (try-catch, async functions, classes, imports/exports)

## How to Use

1. **Apply to VS Code**: Copy the contents of this directory to your VS Code user settings
2. **Customize**: Modify settings as needed for your preferences
3. **Extend**: Use this as a base for language-specific profiles

## Profile Extension

When creating specialized profiles (e.g., TypeScript, Python, Rust), you should:
1. Copy this base profile as a starting point
2. Add language-specific extensions and settings
3. Override any base settings that need customization
4. Add specialized tasks, launch configurations, and snippets as needed for that specific development scenario

## Installation

To use this profile:
1. Open VS Code
2. Go to File > Preferences > Profiles
3. Create a new profile or import these settings
4. Install the recommended extensions
5. Restart VS Code

## Notes

- Font ligatures require a compatible font (JetBrains Mono, Fira Code, etc.)
- MCP (Model Context Protocol) servers can be configured as needed
- Language-specific tasks, debug configurations, and snippets should be added in specialized profiles

This base profile provides a solid foundation while remaining flexible enough to extend for any development scenario.

## Reference

### Extending the Base Profile

For a comprehensive checklist and detailed steps on creating specialized profiles from this base, see:

📋 **[Extending the Base Profile Guide](./extending-the-base-profile.md)**

This guide provides an exhaustive checklist covering all aspects of profile extension including settings configuration, extensions, key bindings, tasks, launch configurations, snippets, documentation, testing, and finalization.
