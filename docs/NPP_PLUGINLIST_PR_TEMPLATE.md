# nppPluginList PR Template

Use this when submitting `AI-Assistant` to the official Notepad++ plugin list.

## Suggested PR Title

Add AI-Assistant x64 plugin entry

## Suggested PR Body

### Summary

This PR adds the `AI-Assistant` plugin to the Notepad++ Plugins Admin list for `x64`.

### Plugin Overview

- Plugin name: `AI-Assistant`
- Display name: `AI-Assistant`
- Version: `0.1.0.0`
- Architecture: `x64`

### Project Description

AI-Assistant is a lightweight AI assistant plugin for Notepad++ with:
- visible prompt preview
- single-turn request behavior
- dynamic model loading
- context menu actions for selected text workflows

### Release Information

- GitHub repo: `https://github.com/Jcfunk/AI-Assistant`
- Release tag: `v0.1.0`
- Release asset:
  `https://github.com/Jcfunk/AI-Assistant/releases/download/v0.1.0/AI-Assistant-0.1.0.0-x64.zip`

### Packaging Notes

- The DLL name matches the folder name: `AI-Assistant.dll`
- The zip places the DLL at the root level
- Documentation is included under `doc/AI-Assistant/`

### Entry JSON

```json
{
  "folder-name": "AI-Assistant",
  "display-name": "AI-Assistant",
  "version": "0.1.0.0",
  "id": "2C94E42609E9A49F9B9840D617CD345635E6E9F7FCF4F5975884C355554F955E",
  "repository": "https://github.com/Jcfunk/AI-Assistant/releases/download/v0.1.0/AI-Assistant-0.1.0.0-x64.zip",
  "description": "Lightweight AI assistant plugin for Notepad++ with visible prompts and single-turn behavior.",
  "author": "AI-Assistant Contributors",
  "homepage": "https://github.com/Jcfunk/AI-Assistant"
}
```

### Checklist

- [x] Final GitHub repo URL replaced
- [x] Final release asset URL replaced
- [x] SHA-256 updated from final uploaded zip
- [ ] Entry added to the correct architecture file
